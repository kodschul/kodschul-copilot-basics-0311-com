# Nordwind Consulting – IT-Tickets Oktober 2025 bis September 2026

Textzwilling von `nordwind-it-tickets.xlsx` für Lab 4.1 und 4.2. Anzahl der Tickets je Kategorie und Monat im internen IT-Support. Alle Angaben sind fiktiv und anonymisiert.

## Tabelle „Tickets" (Arbeitsblatt `Tickets`, formatiert als Tabelle `TicketsJeMonat`)

| Monat | VPN | Passwort/MFA | Hardware | Software | Onboarding | Sonstiges | Summe |
| ----- | --: | -----------: | -------: | -------: | ---------: | --------: | ----: |
| Okt 2025 | 38 | 41 | 22 | 30 | 6 | 12 | 149 |
| Nov 2025 | 35 | 39 | 25 | 28 | 4 | 10 | 141 |
| Dez 2025 | 31 | 44 | 18 | 24 | 2 | 9 | 128 |
| Jan 2026 | 40 | 52 | 27 | 35 | 9 | 14 | 177 |
| Feb 2026 | 42 | 38 | 21 | 29 | 5 | 11 | 146 |
| Mrz 2026 | 118 | 40 | 23 | 31 | 7 | 13 | 232 |
| Apr 2026 | 64 | 37 | 20 | 27 | 6 | 10 | 164 |
| Mai 2026 | 39 | 36 | 24 | 26 | 5 | 12 | 142 |
| Jun 2026 | 37 | 35 | 19 | 33 | 4 | 9 | 137 |
| Jul 2026 | 34 | 50 | 17 | 25 | 3 | 8 | 137 |
| Aug 2026 | 41 | 42 | 26 | 30 | 19 | 11 | 169 |
| Sep 2026 | 45 | 43 | 28 | 32 | 24 | 13 | 185 |
| **Summe** | **564** | **497** | **270** | **350** | **94** | **132** | **1.907** |

## Tabelle „Bearbeitungszeit" (Arbeitsblatt `Bearbeitungszeit`)

| Kategorie | Minuten je Ticket (Durchschnitt) | Lösbar mit Richtlinie? |
| --------- | ------------------: | ---------------------- |
| VPN | 14 | ja, meist |
| Passwort/MFA | 9 | teilweise (Zurücksetzen nur durch IT) |
| Hardware | 35 | nein |
| Software | 22 | teilweise |
| Onboarding | 18 | ja, meist |
| Sonstiges | 20 | nein |

## Aufbau der Excel-Datei

- Layout in Excel: Kopfzeile in Zeile 1, Monate in Zeile 2–13 (Spalte A), Kategorien in Spalte B–G, Summe je Monat in Spalte H; die Tabelle `TicketsJeMonat` umfasst A1:H13. Die Summenzeile steht direkt darunter in Zeile 14.
- Die Summenzeile und die Summenspalte enthalten Formeln (`=SUMME(...)`) und dienen als Kontrollwerte.
