# Lab 4.1 – Übung: Fragen an einen Datensatz stellen

**Ändert die Nordwind-Projektbasis?** Ja — Diagramm und Empfehlung kommen in `nordwind-it-tickets.xlsx`; die Häufung bei VPN-Fragen ist der Anlass für den Agenten in Modul 5.

## Ausgangslage

Der interne IT-Support von Nordwind Consulting beantwortet viele gleiche Fragen. Die Leitung will wissen, wo sich Entlastung am meisten lohnt.

Datei im eigenen OneDrive: `nordwind-it-tickets.xlsx` (Textfassung: `output/project/nordwind-it-tickets.md`)

- Blatt `Tickets`: Excel-Tabelle `TicketsJeMonat` mit Ticketzahlen je Monat (Okt 2025 bis Sep 2026) und Kategorie (VPN, Passwort/MFA, Hardware, Software, Onboarding, Sonstiges), Spalte `Summe` je Monat, darunter eine Summenzeile.
- Blatt `Bearbeitungszeit`: durchschnittliche Minuten je Ticket und ob die Kategorie mit der IT-Richtlinie lösbar ist.

### Prompt-Karte 6 – IT-Tickets auswerten

**Basis** (zum Kopieren, nacheinander):

Häufigste Kategorie (Modus „Chat only"):

```text
Welche Ticketkategorie in der Tabelle TicketsJeMonat kommt über alle zwölf Monate am häufigsten vor? Die Spalte Summe ist keine Kategorie. Nenne die Gesamtzahl je Kategorie und die Formel, mit der du gerechnet hast.
```

Auffälligkeit und Diagramm (Modus „Allow editing"):

```text
Finde in der Tabelle TicketsJeMonat den auffälligsten Einzelwert, also den Wert, der am stärksten vom üblichen Monatswert seiner Kategorie abweicht. Erstelle ein Liniendiagramm, das den Verlauf dieser Kategorie über die zwölf Monate zeigt.
```

Empfehlung Schritt für Schritt (Modus „Chat only"):

```text
Welche Ticketkategorie sollte die IT zuerst mit einer Selbsthilfe-Lösung angehen, zum Beispiel einem Assistenten, der Fragen anhand der IT-Richtlinie beantwortet? Gehe Schritt für Schritt vor: 1. Anzahl je Kategorie, 2. Zeitaufwand je Kategorie mit dem Blatt Bearbeitungszeit, 3. ob die Kategorie mit der Richtlinie lösbar ist, 4. Empfehlung in drei Sätzen. Zeige jeden Zwischenschritt mit Zahlen, bevor du die Empfehlung nennst.
```

**Profi-Variante:**

```text
Lege ein neues Blatt Auswertung an und berechne dort mit Formeln für jede Kategorie die Anzahl, die Stunden pro Jahr (Anzahl × Minuten aus dem Blatt Bearbeitungszeit ÷ 60) und ob sie mit der Richtlinie lösbar ist. Sortiere einmal nach Anzahl und einmal nach Stunden. Begründe Schritt für Schritt, ob sich die Empfehlung ändert, wenn nach Stunden statt nach Anzahl entschieden wird. Nenne zu jeder Auffälligkeit eine mögliche Ursache und kennzeichne sie als Vermutung.
```

## Aufgaben

1. Öffne `nordwind-it-tickets.xlsx` aus dem eigenen OneDrive, öffne Copilot und wähle „Chat only". Führe „Häufigste Kategorie" aus und notiere Kategorie und Gesamtzahl.
2. Wechsle zu „Allow editing" und führe „Auffälligkeit und Diagramm" aus. Notiere Monat, Kategorie und Wert der Auffälligkeit und prüfe, ob das Diagramm die richtige Spalte zeigt.
3. Wechsle zurück zu „Chat only" und führe „Empfehlung Schritt für Schritt" aus. Prüfe jeden Zwischenschritt und notiere die Empfehlung in eigenen Worten in drei Sätzen (im Chat oder optional in einem neuen Blatt `Empfehlung`).
4. Rechne einen Wert von Hand nach: Markiere die zwölf Monatswerte einer Kategorie (z. B. `B2:B13` für VPN), lies die Summe unten in der Statusleiste ab und vergleiche sie mit der Antwort aus Aufgabe 1.

## Checkpoint

- Die häufigste Kategorie ist mit Gesamtzahl notiert; „Summe" wurde nicht als Kategorie gezählt.
- Ein Liniendiagramm mit zwölf Monaten liegt im Blatt `Tickets`.
- Die Antwort aus Aufgabe 3 zeigt vier nummerierte Zwischenschritte mit Zahlen vor der Empfehlung.
- Der handgerechnete Wert stimmt mit der Copilot-Antwort überein oder die Abweichung ist notiert.

## Abschlusskriterien

- `nordwind-it-tickets.xlsx` enthält das Diagramm; die Empfehlung liegt in drei eigenen Sätzen vor.
- Die Empfehlung nennt eine Kategorie, eine Zahl als Beleg und einen Grund, warum Selbsthilfe dort funktioniert.
- Jede genannte Ursache ist als Vermutung gekennzeichnet oder mit einer Quelle belegt.

## Erweiterung

Führe die Profi-Variante aus. Vergleiche die Reihenfolge nach Anzahl und nach Stunden und notiere, welche Kategorie in der zweiten Sortierung vorne liegt und warum sie trotzdem keine Kandidatin für Selbsthilfe ist.

## Fallback

Ist Copilot in Excel nicht verfügbar oder ausgegraut: `nordwind-it-tickets.xlsx` in Copilot Chat hochladen und dieselben Prompts stellen; das Diagramm von Hand anlegen (Spalte markieren → Einfügen → Linie). Einschränkung: Copilot Chat ändert die Arbeitsmappe nicht und zeigt Formeln nur als Text.
