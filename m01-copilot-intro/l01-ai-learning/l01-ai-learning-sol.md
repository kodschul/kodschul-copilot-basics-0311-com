# Lab 1.1 – Lösung: Wie KI lernt und was Copilot daraus macht

## Quiz

| Frage | Richtig | Erklärung |
| ----- | ------- | --------- |
| 1 | **A** | „erfolgreich" folgt in vielen Texten auf „Unser Projekt ist …". Das Modell kennt das eigene Projekt nicht und wählt das Häufige, nicht das Wahre. D wäre nur mit Projektdaten im Prompt möglich. |
| 2 | **C** | Das Modell ist nach dem Training fertig; Prompts und Antworten werden nicht zum Training der Basismodelle genutzt. Im selben Chat zählt der bisherige Verlauf, deshalb funktioniert Nachfragen. |
| 3 | **B** | Grounding über Microsoft Graph: Copilot sucht zum Zeitpunkt der Frage, nur in Inhalten, die die Person ohnehin sehen darf. Im Training waren die eigenen Mails nie enthalten. |

## Aufgaben

### 1. Quizfragen

Lösung siehe Tabelle oben.

### 2. Theorieabschnitt je Antwort

| Frage | Abschnitt |
| ----- | --------- |
| 1 | „Wie eine Antwort entsteht" |
| 2 | „Wie ein Sprachmodell lernt" |
| 3 | „Copilot = Sprachmodell + eigene Daten" |

## Checkpoint

- Quiz: 1 A, 2 C, 3 B.

## Erweiterung

#### 1. Work IQ finden

- Die Schaltfläche **Work IQ** sitzt oben im Chatfenster von Copilot Chat; mit Copilot-Zusatzlizenz ist sie standardmäßig eingeschaltet.
- In älteren Oberflächen entspricht die Registerkarte „Arbeit" dem eingeschalteten Work IQ.

#### 2. Dieselbe Frage mit und ohne Work IQ

| Work IQ | Typische Antwort |
| ------- | ---------------- |
| an | Liste konkreter Dateien, z. B. `nordwind-projektnotizen.docx`, `nordwind-mailverlauf.docx`, mit Links als Quellenangabe |
| aus | Hinweis, dass ohne Zugriff auf Arbeitsdaten keine eigenen Dateien bekannt sind, ggf. allgemeine Tipps zum Finden von Dateien in OneDrive |

#### 3. Begründung in einem Satz

Beispiel: „Mit Work IQ an sucht Copilot über Microsoft Graph in den eigenen OneDrive-Dateien (Grounding), mit Work IQ aus fehlen diese Inhalte und das Modell kann nur allgemein antworten."

Nach der Erweiterung ist Work IQ wieder eingeschaltet; alle folgenden Übungen setzen das voraus.
