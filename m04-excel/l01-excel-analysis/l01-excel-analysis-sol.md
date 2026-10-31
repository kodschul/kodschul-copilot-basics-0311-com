# Lab 4.1 – Lösung: Fragen an einen Datensatz stellen

Alle Zahlen stammen aus `nordwind-it-tickets.xlsx` (Textfassung `nordwind-it-tickets.md`). Copilot formuliert anders, die Zahlen müssen übereinstimmen.

## Aufgabe 1: Häufigste Kategorie

| Kategorie | Tickets Okt 2025 – Sep 2026 | Anteil |
| --------- | --------------------------: | -----: |
| **VPN** | **564** | 29,6 % |
| Passwort/MFA | 497 | 26,1 % |
| Software | 350 | 18,4 % |
| Hardware | 270 | 14,2 % |
| Sonstiges | 132 | 6,9 % |
| Onboarding | 94 | 4,9 % |
| **Gesamt** | **1.907** | 100 % |

Ergebnis: **VPN mit 564 Tickets.**

Formel (deutsches Excel; in englischer Anzeige `SUM`):

```text
=SUMME(TicketsJeMonat[VPN])
```

`TicketsJeMonat[VPN]` ist ein Verweis auf die Spalte VPN der Tabelle; er bleibt richtig, wenn neue Monate hinzukommen.

## Aufgabe 2: Auffälligkeit und Diagramm

**Auffälligkeit:** VPN im März 2026 mit **118** Tickets.

- Übliche Monatswerte bei VPN: 31 bis 45; Durchschnitt ohne März und April (64) gut 38.
- 118 ist knapp dreimal so viel wie ein üblicher Monat; auch die Monatssumme im März (232) ist die höchste des Jahres.
- Der April (64) zeigt einen Nachlauf.

**Ursache:** Aus den Zahlen allein nicht ablesbar; Copilot darf hier nur vermuten (z. B. viele VPN-Zertifikate gleichzeitig abgelaufen). Bestätigen ließe sich die Vermutung nur mit Daten der IT, etwa den Ablaufdaten der Zertifikate.

**Diagramm:** Liniendiagramm, x-Achse Monat (Okt 2025 bis Sep 2026), y-Achse Anzahl VPN-Tickets; die Spitze im März ist auf einen Blick sichtbar.

Prüfpunkte: Das Diagramm zeigt die Spalte VPN (nicht `Summe`) und genau zwölf Punkte (ohne Summenzeile).

## Aufgabe 3: Empfehlung Schritt für Schritt

**Antwort von Copilot (Beispiel, geprüft):**

1. **Anzahl:** VPN 564, Passwort/MFA 497, Software 350, Hardware 270, Sonstiges 132, Onboarding 94.
2. **Zeitaufwand** (Anzahl × Minuten je Ticket ÷ 60):

   | Kategorie | Minuten je Ticket | Stunden pro Jahr |
   | --------- | ----------------: | ---------------: |
   | Hardware | 35 | 157,5 |
   | VPN | 14 | 131,6 |
   | Software | 22 | 128,3 |
   | Passwort/MFA | 9 | 74,6 |
   | Sonstiges | 20 | 44,0 |
   | Onboarding | 18 | 28,2 |

3. **Lösbar mit Richtlinie:** VPN „ja, meist", Onboarding „ja, meist", Passwort/MFA und Software „teilweise", Hardware und Sonstiges „nein".
4. **Empfehlung:** Zuerst VPN, danach Onboarding.

Prüfung der Zwischenschritte: Hardware kostet die meisten Stunden, ist aber nicht mit der Richtlinie lösbar; eine Selbsthilfe würde dort nicht entlasten. Die Empfehlung ergibt sich erst aus Schritt 2 und 3 zusammen; ohne Zwischenschritte wäre diese Abwägung unsichtbar.

**Empfehlung (drei Sätze):**

> VPN ist mit 564 von 1.907 Tickets (29,6 %) die häufigste Kategorie und kostet rund 132 Stunden im Jahr. VPN-Fragen sind meist mit der IT-Richtlinie lösbar; deshalb lohnt sich hier zuerst ein Selbsthilfe-Assistent, der die Richtlinie kennt. Onboarding kommt als zweites Thema dazu, weil die Tickets im August und September deutlich steigen (19 und 24 statt sonst 2 bis 9) und ebenfalls meist mit der Richtlinie lösbar sind.

## Aufgabe 4: Wert von Hand nachrechnen

| Geprüfter Wert | Rechnung | Ergebnis |
| -------------- | -------- | -------- |
| VPN gesamt | `B2:B13` markiert, Statusleiste: Summe 564 | stimmt mit Aufgabe 1 |
| alternativ März gesamt | 118 + 40 + 23 + 31 + 7 + 13 = 232 | stimmt mit Spalte `Summe` |

Mögliche Abweichung: 1.128 für VPN. Dann wurde die Summenzeile mitgezählt (Bereich `B2:B14` statt `B2:B13`, also 564 + 564); die Formel zeigt den falschen Bereich.

## Erweiterung: Anzahl oder Stunden?

Blatt `Auswertung` (Formeln für VPN als Beispiel, die übrigen Zeilen analog):

| Spalte | Formel |
| ------ | ------ |
| Anzahl | `=SUMME(TicketsJeMonat[VPN])` |
| Stunden | `=SUMME(TicketsJeMonat[VPN])*Bearbeitungszeit!B2/60` |
| Lösbar | `=Bearbeitungszeit!C2` |

| Sortierung | Reihenfolge |
| ---------- | ----------- |
| nach Anzahl | VPN, Passwort/MFA, Software, Hardware, Sonstiges, Onboarding |
| nach Stunden | Hardware, VPN, Software, Passwort/MFA, Sonstiges, Onboarding |

Nach Stunden liegt Hardware vorne (157,5 h). Für Selbsthilfe ist Hardware trotzdem keine Kandidatin: Defekte Geräte lassen sich nicht mit einer Richtlinie beheben. Die Empfehlung „zuerst VPN" bleibt. Ursachen mit Kennzeichnung:

| Auffälligkeit | Mögliche Ursache |
| ------------- | ---------------- |
| VPN März 2026 (118) | Vermutung: viele VPN-Zertifikate gleichzeitig abgelaufen; nur mit IT-Daten zu bestätigen |
| Onboarding Aug/Sep 2026 (19, 24) | Vermutung: mehr neue Mitarbeitende |
| Passwort/MFA Jan und Jul 2026 (52, 50) | Vermutung: regelmäßiger Passwortwechsel im Halbjahresrhythmus |
