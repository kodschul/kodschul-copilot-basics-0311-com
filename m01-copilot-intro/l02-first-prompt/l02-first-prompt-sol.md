# Lab 1.2 – Lösung: Der erste gute Prompt

## Aufgaben

### 1. Vager Prompt

```text
Wie läuft das Projekt?
```

Typisches Ergebnis: eine Rückfrage („Welches Projekt ist gemeint?"), allgemeine Tipps zur Projektsteuerung oder, mit Work IQ an, eine Zusammenfassung irgendeines Projekts, das in Mails oder Dateien zuletzt vorkam. Ohne Ziel, Kontext, Quelle und Erwartung entscheidet Copilot alles selbst.

### 2. Prompt-Karte 1 (Basis)

Zuordnung der vier Angaben:

| Angabe | Textstelle |
| ------ | ---------- |
| Ziel | „Fasse den aktuellen Stand … in fünf Stichpunkten zusammen." |
| Kontext | „Ich bin neu im Projektteam … bereite mich auf den nächsten Jour fixe … vor." |
| Quelle | „Nutze nur /nordwind-projektnotizen.docx." |
| Erwartung | „Ein Stichpunkt pro Zeile, jeder mit … Datum, Zahl oder Prozentwert … offen markieren" |

Beispielergebnis (Wortlaut variiert):

- Projekt seit 12.08.2026, Berichtsstand 23.09.2026 (Woche 7); 71.500 € von 184.000 € verbraucht (38,9 %).
- AP1 Ist-Analyse abgeschlossen (100 %); AP2 Anforderungskatalog 70 %, AP3 Schnittstellenkonzept 35 %; AP4 und AP5 nicht begonnen.
- **offen:** Freigabe des Anforderungskatalogs (AP2) durch den Fachbereich Betrieb steht seit 11.09.2026 aus; blockiert AP4, Rollout-Planung verschiebt sich um 3–4 Wochen (Risiko R1).
- **offen:** Testsystemzugang Sensorik beantragt (16.09.2026), noch nicht erteilt; AP3 kann ohne ihn nicht abgeschlossen werden (Risiko R2).
- **offen:** Zwei Fachinterviews kundenseitig abgesagt, ohne Ersatztermin; Zuständigkeit für die Datenmigration zwischen IT und Betrieb ungeklärt.

### 3. Prüfung gegen die Projektnotizen

| Angabe | Wert in `nordwind-projektnotizen.docx` | Häufige Abweichung |
| ------ | -------------------------------------- | ------------------ |
| Fortschritt AP2 | 70 % | korrekt übernommen |
| Verbraucht | 71.500 € (38,9 %) | auf „rund 39 %" gerundet oder Prozent ohne Betrag |
| Freigabe AP2 ausstehend seit | 11.09.2026 | Datum der Mail (09.09.) statt Jour fixe (11.09.) |
| Testsystemzugang | beantragt, noch nicht erteilt | „erteilt" oder „noch nicht beantragt" |

Auch „keine Abweichung" ist ein gültiges Ergebnis, wenn beide Angaben tatsächlich in der Datei nachgesehen wurden.

### 4. Nachfrage und Unterschied

Beispiel-Nachfrage:

```text
Formuliere Punkt 3 so, dass ihn jemand ohne Projektwissen versteht.
```

Beispielergebnis: „Der Kunde hat den Anforderungskatalog seit dem 11.09.2026 noch nicht freigegeben. Solange die Freigabe fehlt, kann die Planung der Einführung nicht beginnen; das kostet voraussichtlich drei bis vier Wochen."

Beispielsatz zum Unterschied: „Der vage Prompt hatte kein Ziel und keine Quelle, deshalb kam eine allgemeine Antwort; mit Quelle und Erwartung kamen fünf prüfbare Punkte aus der Datei."

## Checkpoint

- Fünf Punkte mit Zahlen oder Daten aus der Datei, die Projektnotizen als Quelle angegeben.
- Zwei geprüfte Angaben mit Ergebnis.

## Erweiterung

Mit der Profi-Variante steht die AP2-Freigabe meist an erster Stelle, weil sie laut Risiko R1 den Zeitplan am stärksten gefährdet. Passende Fragen für den Jour fixe:

- „Bis wann kann der Fachbereich Betrieb den Anforderungskatalog freigeben?"
- „Wer klärt die Zuständigkeit für die Datenmigration zwischen IT und Betrieb?"

Beide gehen auf die offenen Punkte 1 und 4 der Projektnotizen zurück. Eine Frage zu einem Thema, das nicht in der Datei steht, wäre ein Hinweis auf eine Halluzination.

## Fallback

Mit hochgeladener Datei oder eingefügtem Text entstehen dieselben fünf Punkte. Der Prüfschritt bleibt gleich.
