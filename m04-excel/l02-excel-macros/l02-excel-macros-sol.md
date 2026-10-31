# Lab 4.2 – Lösung: Makros mit Copilot: wiederkehrende Arbeit automatisieren

Copilot erzeugt bei jedem Lauf etwas anderen Code. Der folgende Code zeigt eine vollständige, geprüfte Fassung für den Aufbau aus der Übung.

**Angenommener Aufbau des Blatts `Tickets`:** Zeile 1 Überschriften der Tabelle `TicketsJeMonat` (A1:H13), Zeilen 2–13 Monate Okt 2025 bis Sep 2026, Spalten B–G Kategorien (VPN, Passwort/MFA, Hardware, Software, Onboarding, Sonstiges), Spalte H Summe je Monat, Zeile 14 Summenzeile unter der Tabelle.

## Aufgabe 1: Makro lesen

```vba
Option Explicit   ' jede Variable muss angemeldet werden; Tippfehler fallen sofort auf

Sub MonatswerteFormatieren()
    ' Formatiert die Ticketübersicht im Blatt "Tickets" von nordwind-it-tickets.xlsx

    Const GRENZE As Long = 100   ' Werte über dieser Grenze werden rot
    Dim ws As Worksheet          ' das Arbeitsblatt
    Dim zelle As Range           ' die gerade geprüfte Zelle

    ' Fester Bezug auf das Blatt "Tickets" in dieser Arbeitsmappe
    Set ws = ThisWorkbook.Worksheets("Tickets")

    ' Teil 1: Tausendertrennzeichen, keine Nachkommastellen
    ' (Monatswerte, Spalte Summe und Summenzeile)
    ws.Range("B2:H14").NumberFormat = "#,##0"

    ' Teil 2: Werte über 100 rot, alle anderen in normaler Schriftfarbe
    ' (nur Kategorien B bis G; die Spalte Summe liegt fast immer über 100)
    For Each zelle In ws.Range("B2:G13")
        If IsNumeric(zelle.Value) Then
            If zelle.Value > GRENZE Then
                zelle.Font.Color = RGB(192, 0, 0)               ' Dunkelrot
            Else
                zelle.Font.ColorIndex = xlColorIndexAutomatic   ' Standardfarbe
            End If
        End If
    Next zelle

    ' Teil 3: Summenzeile fett
    ws.Range("A14:H14").Font.Bold = True
End Sub
```

Zuordnung der drei Auftragsteile:

| Auftrag | Stelle im Code |
| ------- | -------------- |
| Tausendertrennzeichen | `ws.Range("B2:H14").NumberFormat = "#,##0"` |
| Werte über 100 rot | Schleife `For Each zelle In ws.Range("B2:G13")` mit `If zelle.Value > GRENZE` |
| Summenzeile fett | `ws.Range("A14:H14").Font.Bold = True` |

**Erklärung in drei Sätzen (wie von Copilot angefordert):** Das Makro stellt alle Zahlen der Übersicht ohne Kommastellen und mit Tausenderpunkt dar. Danach schaut es sich jede Monatszahl der sechs Kategorien einzeln an und färbt sie rot, wenn sie größer als 100 ist. Zum Schluss wird die Zeile mit den Jahressummen fett gedruckt.

Zwei Entscheidungen im Code:

- **Spalte H wird nicht rot markiert:** Jede Monatssumme liegt über 100 (128 bis 232); rot wäre dort jede Zelle und damit keine Information.
- **Zuerst die Prüfung „ist das eine Zahl?":** Steht in einer Zelle Text oder ein Fehlerwert, bricht das Makro sonst ab.

## Aufgabe 2: Eine Zeile erklären lassen

Beispiel:

```text
Erkläre diese Zeile in einfachen Worten: ws.Range("B2:H14").NumberFormat = "#,##0"
```

Erklärung in einem Satz: Die Zeile legt für die Zellen B2 bis H14 fest, dass Zahlen ganz ohne Kommastellen und mit Tausendertrennzeichen angezeigt werden; der Wert selbst bleibt unverändert.

Ergänzung: Im Code steht das Format in englischer Schreibweise (`#,##0`). Excel zeigt es in deutscher Einstellung trotzdem mit Punkt an, also `1.907`.

Weitere oft erklärte Zeile: `zelle.Font.ColorIndex = xlColorIndexAutomatic` setzt die Schriftfarbe auf „Automatisch", also die Standardfarbe der Tabelle; so wird ein früher rot markierter Wert wieder normal, wenn er unter 100 sinkt.

## Aufgabe 3 (optional): Test an der Kopie

Ablauf in Excel Desktop:

1. Datei → Speichern unter → Dateityp „Excel-Arbeitsmappe mit Makros (*.xlsm)", Name `nordwind-it-tickets-test.xlsm`.
2. Alt+F11 → Einfügen → Modul → Code einfügen.
3. Cursor in das Makro setzen, F5 drücken; zurück zu Excel mit Alt+F11.

Erwartetes Ergebnis im Blatt `Tickets`:

| Prüfung | Ergebnis |
| ------- | -------- |
| rote Werte in B2:G13 | genau einer: B7, VPN im März 2026, Wert 118 |
| Werte genau 100 oder darunter | normale Schriftfarbe (der zweithöchste Wert ist 64, VPN April 2026) |
| Tausendertrennzeichen | sichtbar nur bei Zahlen ab 1.000, hier bei der Gesamtsumme H14: `1.907` |
| Summenzeile A14:H14 | fett |
| Original `nordwind-it-tickets.xlsx` | unverändert |

Dass nur eine Zahl einen Tausenderpunkt zeigt, ist kein Fehler: Alle anderen Werte liegen unter 1.000.

## Erweiterung: Makro mit Tabellenbezug

```vba
Option Explicit

Const GRENZE As Long = 100   ' Grenze für die rote Markierung, hier an einer Stelle änderbar

Sub MonatswerteFormatierenTabelle()
    Dim ws As Worksheet
    Dim tbl As ListObject        ' ListObject = Excel-Tabelle wie TicketsJeMonat
    Dim zahlen As Range          ' alle Zahlenspalten inkl. Summe (B bis H)
    Dim kategorien As Range      ' nur Kategorien (B bis G)
    Dim summenzeile As Range     ' Zeile direkt unter der Tabelle
    Dim zelle As Range

    ' Blatt und Tabelle suchen, ohne bei Fehlen abzustürzen
    On Error Resume Next
    Set ws = ThisWorkbook.Worksheets("Tickets")
    If Not ws Is Nothing Then Set tbl = ws.ListObjects("TicketsJeMonat")
    On Error GoTo 0

    If tbl Is Nothing Then
        MsgBox "Blatt 'Tickets' oder Tabelle 'TicketsJeMonat' wurde nicht gefunden.", vbExclamation
        Exit Sub
    End If

    ' Bereiche aus der Tabelle ableiten: wachsen mit, wenn Monate dazukommen
    With tbl.DataBodyRange
        Set zahlen = .Offset(0, 1).Resize(, .Columns.Count - 1)
        Set kategorien = .Offset(0, 1).Resize(, .Columns.Count - 2)
    End With
    Set summenzeile = tbl.Range.Rows(tbl.Range.Rows.Count).Offset(1, 0)

    zahlen.NumberFormat = "#,##0"
    summenzeile.NumberFormat = "#,##0"

    For Each zelle In kategorien
        If IsNumeric(zelle.Value) Then
            If zelle.Value > GRENZE Then
                zelle.Font.Color = RGB(192, 0, 0)
            Else
                zelle.Font.ColorIndex = xlColorIndexAutomatic
            End If
        End If
    Next zelle

    summenzeile.Font.Bold = True
End Sub
```

Warum robuster: `B2:G13` gilt nur für genau zwölf Monate. Der Bezug auf `TicketsJeMonat` liest die aktuelle Größe der Tabelle bei jedem Lauf; kommt ein Monat hinzu, wird er ohne Codeänderung mitformatiert. Fehlt Blatt oder Tabelle, erscheint eine Meldung statt eines Laufzeitfehlers.
