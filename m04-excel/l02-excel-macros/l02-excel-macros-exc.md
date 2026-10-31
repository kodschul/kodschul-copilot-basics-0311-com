# Lab 4.2 – Übung: Makros mit Copilot: wiederkehrende Arbeit automatisieren

**Ändert die Nordwind-Projektbasis?** Nein — das Makro läuft höchstens an einer Kopie; `nordwind-it-tickets.xlsx` bleibt unverändert.

## Ausgangslage

Die IT-Leitung von Nordwind Consulting bringt die Ticketübersicht jeden Monat in dieselbe Form: Zahlen mit Tausendertrennzeichen, Werte über 100 rot, Summenzeile fett. Das soll ein Makro übernehmen.

Das Lab wird gezeigt; Mitmachen ist optional. Zum Ausführen braucht es Excel Desktop und die Erlaubnis, Makros auszuführen.

Datei: `nordwind-it-tickets.xlsx`, Blatt `Tickets` (Textfassung: `output/project/nordwind-it-tickets.md`). Aufbau:

| Bereich | Inhalt |
| ------- | ------ |
| Zeile 1 | Überschriften der Tabelle `TicketsJeMonat` |
| Zeilen 2–13 | Monate Okt 2025 bis Sep 2026 |
| Spalten B–G | Tickets je Kategorie |
| Spalte H | Summe je Monat |
| Zeile 14 | Summenzeile (direkt unter der Tabelle) |

### Prompt-Karte 7 – Makro für die Ticketübersicht

**Basis** (zum Kopieren):

```text
Schreibe ein VBA-Makro für Excel für das Arbeitsblatt „Tickets". Aufbau: Zeile 1 Überschriften der Tabelle TicketsJeMonat, Zeilen 2 bis 13 Monate, Spalten B bis G Ticketzahlen je Kategorie, Spalte H Summe je Monat, Zeile 14 Summenzeile. Das Makro soll:
1. die Zahlen in B2:H14 mit Tausendertrennzeichen ohne Nachkommastellen formatieren,
2. Werte über 100 in B2:G13 rot markieren, alle anderen in normaler Schriftfarbe,
3. die Summenzeile A14:H14 fett setzen.
Kommentiere den Code auf Deutsch und erkläre danach in drei Sätzen ohne Fachbegriffe, was das Makro tut.
```

**Profi-Variante:**

```text
Ändere das Makro so, dass es statt fester Zellbereiche die Tabelle TicketsJeMonat verwendet, damit neue Monate automatisch einbezogen werden. Die Grenze 100 soll oben als Konstante stehen. Wenn das Blatt „Tickets" oder die Tabelle fehlt, soll eine verständliche Meldung erscheinen statt eines Fehlers.
```

## Aufgaben

1. Lies mit, wie Copilot mit Prompt-Karte 7 (Basis) das Makro erzeugt, und ordne die drei Teile des Auftrags den Stellen im Code zu (Format, rote Markierung, fett).
2. Wähle eine Zeile, die unklar ist, und lass sie von Copilot erklären: „Erkläre diese Zeile in einfachen Worten: [Zeile]". Notiere die Erklärung in einem Satz.
3. Optional, nur in Excel Desktop: Speichere eine Kopie als `nordwind-it-tickets-test.xlsm`, öffne den VBA-Editor (Alt+F11), füge über Einfügen → Modul den Code ein und starte ihn mit F5. Prüfe das Ergebnis im Blatt `Tickets`.

## Checkpoint

- Die drei Teile des Auftrags sind im Code wiedergefunden.
- Eine Codezeile ist in einem Satz in Alltagssprache erklärt.
- Optional: In der Testkopie ist genau ein Wert rot (VPN im März 2026), die Summenzeile ist fett, die Gesamtsumme zeigt `1.907`.

## Abschlusskriterien

- Ein kommentiertes Makro und eine erklärte Zeile liegen vor.
- Falls ausgeführt: nur in der Kopie `nordwind-it-tickets-test.xlsm`, das Original ist unverändert.

## Erweiterung

Führe die Profi-Variante aus und lass Copilot erklären, warum die Tabelle als Bezug robuster ist als ein fester Bereich wie `B2:G13`.

## Fallback

Ohne Excel Desktop oder ohne Makro-Erlaubnis: Prompt-Karte 7 in Copilot Chat oder Copilot in Excel im Web ausführen, den Code lesen und Aufgabe 1 und 2 vollständig bearbeiten. Einschränkung: Das Makro lässt sich nicht ausführen; das erwartete Ergebnis steht in der Lösung.
