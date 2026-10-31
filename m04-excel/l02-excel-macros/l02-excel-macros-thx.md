# Lab 4.2: Makros mit Copilot: wiederkehrende Arbeit automatisieren

**Leitfragen:**

<details>
<summary>Welche Excel-Handgriffe wiederholen sich jede Woche?</summary>

Typisch: Zahlen formatieren, Werte über einer Grenze markieren, Summenzeilen hervorheben, Berichte in dieselbe Form bringen. Was jedes Mal gleich abläuft, lässt sich als Makro speichern.

</details>

<details>
<summary>Würde jemand einen Code ausführen, den er nicht lesen kann?</summary>

Besser nicht. Copilot kann den Code aber Zeile für Zeile in Alltagssprache erklären, sodass auch ohne Programmierkenntnisse klar wird, was er tut.

</details>

<details>
<summary>Was kann beim automatischen Ändern einer Datei schiefgehen?</summary>

Ein Fehler trifft alle Zellen auf einmal, ohne Rückfrage, und lässt sich nicht mit Strg+Z zurücknehmen. Deshalb wird jedes Makro zuerst an einer Kopie getestet.

</details>

- Ein Makro speichert Arbeitsschritte, die Excel auf Knopfdruck wiederholt.
- Copilot schreibt und erklärt den Code; getestet wird immer an einer Kopie.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Makro | Gespeicherte Folge von Arbeitsschritten, die Excel auf Knopfdruck wiederholt; wie ein Rezept, das Excel Schritt für Schritt nachkocht. |
| VBA (Visual Basic for Applications) | Die Programmiersprache, in der Excel-Makros geschrieben sind. |
| VBA-Editor | Fenster in Excel Desktop, in dem der Makro-Code steht (Alt+F11). |
| `.xlsm` | Dateiformat „Excel-Arbeitsmappe mit Makros"; eine `.xlsx`-Datei speichert keine Makros. |

## Vom Prompt zum Makro

Der Ablauf hat einen festen Prüfpunkt, bevor der Code auf echte Daten trifft.

```mermaid
flowchart LR
    A["Aufgabe genau beschreiben<br/>Blatt, Bereich, Regel"] --> B["Copilot schreibt<br/>VBA-Code mit Kommentaren"]
    B --> C["Code lesen,<br/>unklare Zeile erklären lassen"]
    C --> D["an einer Kopie testen<br/>(Excel Desktop)"]
    D --> E["erst dann<br/>am Original verwenden"]
```

Ein guter Makro-Auftrag nennt drei Dinge: welches Blatt und welcher Bereich, was genau passieren soll, und wie der Aufbau der Tabelle ist. „Formatiere den Bericht" ist zu vage; „Zahlen in B2:H14 mit Tausendertrennzeichen, Werte über 100 in B2:G13 rot" ist eindeutig.

## So sieht ein Makro aus

Ein kurzes Beispiel; die grünen Zeilen mit `'` am Anfang sind Kommentare für Menschen, Excel ignoriert sie.

```vba
Sub SummenzeileFett()
    ' Zeile 14 im Blatt "Tickets" fett darstellen
    Worksheets("Tickets").Range("A14:H14").Font.Bold = True
End Sub
```

| Teil | Bedeutung |
| ---- | --------- |
| `Sub … End Sub` | Anfang und Ende des Makros; der Name steht hinter `Sub` |
| `Worksheets("Tickets")` | das Arbeitsblatt mit diesem Namen |
| `.Range("A14:H14")` | der Zellbereich |
| `.Font.Bold = True` | die Änderung: Schrift fett |

## Wo Makros laufen

| Umgebung | VBA-Makros |
| -------- | ---------- |
| Excel Desktop (Windows, Mac) | erstellen, bearbeiten, ausführen |
| Excel im Web | weder erstellen noch ausführen noch bearbeiten |

Quelle: [Microsoft Support, „Work with VBA macros in Excel for the web"](https://support.microsoft.com/en-us/office/work-with-vba-macros-in-excel-for-the-web-98784ad0-898c-43aa-a1da-4f0fb5014343), abgerufen am 31.10.2026. Ob Makros im eigenen Unternehmen ausgeführt werden dürfen, legt die IT fest.

## Sicherheit

- **Immer an einer Kopie testen:** Ein Makro ändert viele Zellen auf einmal; Strg+Z nimmt Makro-Änderungen nicht zurück.
- **Keine Makros aus unbekannter Quelle:** Makros können mehr als formatieren, z. B. Dateien löschen oder Daten versenden. Microsoft blockiert Makros in Dateien aus dem Internet deshalb standardmäßig ([Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365-apps/security/internet-macros-blocked), abgerufen am 31.10.2026).
- **Code verstehen, bevor er läuft:** Jede Zeile, die unklar ist, lässt sich Copilot erklären.

> **Merksatz:** Ein Makro wird erst ausgeführt, wenn klar ist, was es tut, und zuerst an einer Kopie.

## Typische Fehler

| Symptom | Ursache | Lösung |
| ------- | ------- | ------ |
| Kein VBA-Editor, Alt+F11 ohne Wirkung | Excel im Web geöffnet | Datei in Excel Desktop öffnen („In Desktop-App öffnen") |
| Makro ist nach dem Speichern verschwunden | als `.xlsx` gespeichert | als „Excel-Arbeitsmappe mit Makros" (`.xlsm`) speichern |
| Fehlermeldung „Index außerhalb des gültigen Bereichs" | Blattname im Code stimmt nicht | Blattname im Code mit dem Register unten vergleichen |
| Makro läuft, aber nichts sichtbar ändert sich | falscher Zellbereich im Code | Bereich im Code mit der Tabelle abgleichen |
| Makros sind deaktiviert | Sicherheitseinstellung des Unternehmens | nur mit Freigabe der IT aktivieren; sonst nur lesen und erklären lassen |

## Ausblick: vom Makro zum Agenten

Ein Agent ist ein gespeicherter Assistent in Copilot mit einem Ziel, festen Anweisungen und eigenem Wissen.

| Makro | Agent |
| ----- | ----- |
| feste Schritte, immer gleich | ein Ziel, die Schritte wählt der Agent |
| kennt nur seinen Code | arbeitet mit Anweisungen und Wissen |
| führt aus, ohne zu fragen | fragt nach, wenn etwas unklar ist |

Über den offenen Standard MCP kann ein Agent später auch Aktionen in anderen Systemen ausführen (Lab 5.3).

## Fazit

- Ein Makro lohnt sich für Handgriffe, die sich regelmäßig gleich wiederholen.
- Copilot schreibt und erklärt den VBA-Code; der Mensch liest ihn und testet an einer Kopie.
- VBA-Makros laufen nur in Excel Desktop, nie aus unbekannter Quelle.

In der Übung erzeugt Copilot ein Makro für `nordwind-it-tickets.xlsx` und erklärt eine Zeile daraus.
