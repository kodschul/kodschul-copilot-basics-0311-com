# Microsoft 365 Copilot kompakt – Möglichkeiten entdecken und direkt anwenden

## Die Entwicklung von Microsoft 365 Copilot

- Seit ChatGPT (30.11.2022) ist generative KI für alle nutzbar: Programme schreiben Texte, fassen zusammen und beantworten Fragen.
- Seit 01.11.2023 ist Microsoft 365 Copilot für Unternehmen verfügbar und arbeitet direkt in Outlook, Teams, Word, PowerPoint und Excel.
- Heute lassen sich mit Copilot auch eigene Agenten bauen: gespeicherte Spezialassistenten, die wiederkehrende Fragen beantworten. Über MCP, einen offenen Standard zum Anbinden fremder Werkzeuge, führen sie auch Aktionen in anderen Systemen aus.
- Details und Quellen: [Lab 1.1](../m01-copilot-intro/l01-ai-learning/l01-ai-learning-thx.md).

## Was ist Microsoft 365 Copilot?

- **Sprachmodell (LLM):** ein Programm, das aus riesigen Textmengen gelernt hat, Text fortzusetzen – wie die Handy-Autovervollständigung im Großformat.
- **Microsoft 365 Copilot:** ein Sprachmodell plus Zugriff auf die eigenen Mails, Chats, Termine und Dateien über Microsoft Graph, nur mit den Rechten der angemeldeten Person.
- **Grounding:** Copilot holt zur Frage passende echte Inhalte und stützt die Antwort darauf, statt nur aus dem Gedächtnis des Modells zu antworten.
- **Prompt:** die Eingabe an Copilot; Ziel, Kontext, Quelle und Erwartung entscheiden über die Qualität ([Lab 1.2](../m01-copilot-intro/l02-first-prompt/l02-first-prompt-thx.md)).

## Warum Microsoft 365 Copilot?

| | Allgemeiner KI-Chat | Microsoft 365 Copilot |
| - | ------------------- | --------------------- |
| Kennt die eigenen Mails und Dateien | nein, nur was eingefügt wird | ja, über Microsoft Graph und die eigenen Berechtigungen |
| Arbeitet in der App | nein, Kopieren hin und her | ja, in Outlook, Teams, Word, PowerPoint, Excel |
| Daten bleiben im Unternehmensrahmen | abhängig vom Anbieter | ja, im Microsoft-365-Tenant; keine Nutzung zum Training der Basismodelle |
| Eigene Agenten | je nach Anbieter | ja, mit dem Agent Builder in Copilot Chat |

## Ziel und Ergebnis

- Copilot in fünf Apps für je eine typische Alltagsaufgabe nutzen, mit einer passenden Prompt-Technik.
- Entscheidungen selbst behalten (Human in the Loop) und jedes Ergebnis prüfen.
- Mit Copilot die Anweisung für einen eigenen Agenten entwerfen und ihn anlegen: **KI nutzen, um KI zu bauen**.
- Verstehen, wie ein Agent über MCP handelt und wo eine Freigabe nötig ist.
- Die Regeln für den sicheren Einsatz kennen.
- Leitmotiv: [The Nextise Agentic Way](../m01-copilot-intro/00-nextise-agentic-way.md).

## Zielgruppe und Voraussetzungen

| Punkt | Inhalt |
| ----- | ------ |
| Zielgruppe | Mitarbeitende aus allen Fachbereichen, von „Copilot noch nie bewusst genutzt" bis „nutzt Copilot Chat regelmäßig" |
| Vorkenntnisse | keine; Programmierkenntnisse nicht nötig |
| Lizenz | Microsoft 365 Copilot (Zusatzlizenz) mit Copilot in Outlook, Teams, Word, PowerPoint und Excel |
| Software | aktuelle Microsoft-365-Apps; für das Ausführen von Makros (Lab 4.2) Excel Desktop |
| Dateien | Übungsdateien aus [`project/`](../project/README.md) im eigenen OneDrive |

## Technik-Check vor dem Start

1. Öffne Outlook, Teams, Word, PowerPoint und Excel und prüfe, ob jeweils das Copilot-Symbol erscheint.
2. Kopiere alle `.docx`- und `.xlsx`-Dateien aus `project/` in einen eigenen Ordner im OneDrive, z. B. `OneDrive/Copilot-Kurs/`.
3. Öffne Copilot Chat in der Microsoft 365 Copilot App und prüfe, ob **Work IQ** eingeschaltet ist (ältere Oberfläche: Registerkarte „Arbeit").
4. Tippe `/nordwind` in das Chatfeld und prüfe, ob die kopierten Dateien zur Auswahl erscheinen.

## Szenario

- **Nordwind Consulting:** fiktives Beratungsunternehmen mit dem Kundenprojekt „Hafenmodernisierung" für die Stadtwerke Nordhafen und einem internen IT-Support, der viele gleiche Fragen beantwortet.
- Die Labs bilden eine Kette: Mail → Besprechung → Bericht → Präsentation → Ticketauswertung → eigener Agent → Ausblick auf Aktionen.
- Personen und Dateien: [`project/szenarien.md`](../project/szenarien.md).

## Ablauf

| Zeit | Inhalt |
| ---- | ------ |
| 09:00–09:10 | Auftakt: Ziel, Spielregeln, Einstiegsquiz, Nextise Agentic Way |
| 09:10–09:35 | Modul 1: Wie KI denkt – und warum der Prompt entscheidet |
| 09:35–10:25 | Modul 2: Outlook und Teams in der Praxis |
| 10:25–10:35 | Pause |
| 10:35–11:20 | Modul 3: Dokumente und Präsentationen mit Human in the Loop |
| 11:20–11:50 | Modul 4: Datenanalyse und Automatisierung mit Excel |
| 11:50–12:00 | Pause |
| 12:00–12:35 | Modul 5: Copilot Chat und Agents – KI baut KI |
| 12:35–12:50 | Modul 6: KI-Richtlinie und sicherer Einsatz |
| 12:50–13:05 | Abschluss: Abschlussquiz, Fragen, erster eigener Schritt |

Module und Labs im Detail: [topics.md](topics.md).

## Arbeitsweise

- Jedes Lab folgt **Zeigen → Nachmachen → Prüfen**: kurze Vorführung am echten Produkt, dann dieselbe Aufgabe mit einer Prompt-Karte, dann ein Prüfschritt.
- Alle Prompts stehen in [prompt-karten.md](../prompt-karten.md), jeweils als Basis und Profi-Variante.
- Einordnungen laufen als Quiz mit Multiple-Choice-Fragen: [quiz-fragen.md](../quiz-fragen.md).
- In allen Übungen gilt: nur die Kursdateien verwenden, keine echten personenbezogenen Daten eingeben.
