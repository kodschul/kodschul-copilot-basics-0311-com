# Quizfragen

Alle Multiple-Choice-Fragen des Kurses mit Lösung und Erklärung. Jede Frage hat genau eine richtige Antwort. Die Sammlung dient als Vorlage für ein Quiz in Microsoft Forms oder als Umfrage in einer Teams-Besprechung und zum Wiederholen nach dem Kurs.

## Einstiegsquiz

1. Wie oft wird Microsoft 365 Copilot im eigenen Arbeitsalltag bisher genutzt?
   - A) noch nie bewusst
   - B) ab und zu, meist in Copilot Chat
   - C) regelmäßig, auch in Outlook, Word oder Teams
   - D) täglich, inklusive eigener Agenten
2. Woher hat Copilot sein allgemeines Sprachwissen?
   - A) aus den eigenen Mails und Dateien
   - B) aus einem einmaligen Training mit sehr großen Textmengen
   - C) aus einer ständig aktualisierten Datenbank mit geprüften Fakten
   - D) aus den Chats aller Copilot-Nutzenden von gestern
3. Was macht einen Prompt am ehesten gut?
   - A) möglichst kurz, damit Copilot frei entscheiden kann
   - B) höflich formuliert, mit „bitte" und „danke"
   - C) Ziel, Kontext, Quelle und erwartetes Ergebnis sind genannt
   - D) in Englisch geschrieben

**Lösung:**

| Frage | Richtig | Erklärung |
| ----- | ------- | --------- |
| 1 | – | Stimmungsbild ohne richtige Antwort; zeigt, wie gemischt die Vorerfahrung ist. |
| 2 | **B** | Das Sprachmodell lernt einmalig im Training; die eigenen Arbeitsdaten kommen erst bei der Frage dazu (Lab 1.1). |
| 3 | **C** | Die Prompt-Formel Ziel · Kontext · Quelle · Erwartung grenzt ein, was Copilot liefert (Lab 1.2). |

## Lab 1.1 – Wie KI lernt

1. Welches Wort setzt ein Sprachmodell ohne weitere Angaben am wahrscheinlichsten hinter „Unser Projekt ist …"?
   - A) „erfolgreich"
   - B) „blau"
   - C) „Hafenmodernisierung"
   - D) „verschoben, weil die Freigabe fehlt"
2. Lernt Copilot aus diesem Chat dauerhaft dazu?
   - A) Ja, jede Korrektur im Chat verbessert sofort das Modell.
   - B) Ja, die Antworten werden über Nacht für alle Kolleginnen und Kollegen übernommen.
   - C) Nein, das Modell bleibt unverändert; innerhalb eines Chats berücksichtigt Copilot den bisherigen Verlauf.
   - D) Nein, Copilot vergisst sogar die vorherige Nachricht im selben Chat.
3. Woher kennt Copilot die eigenen Mails?
   - A) Aus dem Training des Sprachmodells.
   - B) Copilot sucht im Moment der Frage über Microsoft Graph in den Mails, auf die die angemeldete Person Zugriff hat.
   - C) Microsoft kopiert vorab alle Postfächer in das Sprachmodell.
   - D) Gar nicht; Copilot kennt nur Inhalte aus dem Internet.

**Lösung:**

| Frage | Richtig | Erklärung |
| ----- | ------- | --------- |
| 1 | **A** | „erfolgreich" folgt in vielen Texten auf „Unser Projekt ist …". Das Modell kennt das eigene Projekt nicht und wählt das Häufige, nicht das Wahre. D wäre nur mit Projektdaten im Prompt möglich. |
| 2 | **C** | Das Modell ist nach dem Training fertig; Prompts und Antworten werden nicht zum Training der Basismodelle genutzt. Im selben Chat zählt der bisherige Verlauf, deshalb funktioniert Nachfragen. |
| 3 | **B** | Grounding über Microsoft Graph: Copilot sucht zum Zeitpunkt der Frage, nur in Inhalten, die die Person ohnehin sehen darf. Im Training waren die eigenen Mails nie enthalten. |

_Quelle: [Lab 1.1](m01-copilot-intro/l01-ai-learning/l01-ai-learning-exc.md)._

## Lab 5.1 – Was ist ein Agent?

**1. Der interne IT-Support bekommt jeden Monat Dutzende Fragen zur VPN-Einrichtung. Die Antworten stehen in der IT-Richtlinie.**

- A: Agent lohnt sich
- B: normaler Prompt reicht
- C: gar nicht an KI geben

**2. Die Projektleitung möchte eine 40-seitige Ausschreibung der Stadtwerke Nordhafen einmalig in fünf Punkten zusammenfassen.**

- A: Agent lohnt sich
- B: normaler Prompt reicht
- C: gar nicht an KI geben

**3. Die Personalabteilung möchte 30 Bewerbungen für eine offene Stelle von Copilot in eine Rangfolge bringen lassen.**

- A: Agent lohnt sich
- B: normaler Prompt reicht
- C: gar nicht an KI geben

**Lösung:**

| Frage | Antwort | Erklärung |
| ----- | ------- | --------- |
| 1. VPN-Fragen | **A: Agent lohnt sich** | Die Frage kommt jeden Monat wieder, die Antwort steht immer in derselben Quelle (IT-Richtlinie), die Regeln sind klar. |
| 2. Ausschreibung zusammenfassen | **B: normaler Prompt reicht** | Einmalige Aufgabe mit einer einzigen Datei; ein Prompt nach der Formel aus Lab 1.2 mit `/`-Referenz genügt. |
| 3. Bewerbungen ranken | **C: gar nicht an KI geben** | Eine Rangfolge von Bewerbungen ist eine Bewertung von Personen mit Folgen für Einzelne; sie bleibt beim Menschen. |

_Quelle: [Lab 5.1](m05-custom-agents/l01-agent-basics/l01-agent-basics-exc.md)._

## Lab 5.3 – MCP und Aktionen

**1. Welche Aktion braucht eine Bestätigung?**

- A: den Status eines vorhandenen Tickets abfragen
- B: einen Abschnitt der IT-Richtlinie anzeigen
- C: ein neues Ticket im Ticketsystem anlegen
- D: die Liste der verfügbaren Werkzeuge anzeigen

**2. Was ist ein MCP-Server?**

- A: ein Server, auf dem das Sprachmodell von Copilot trainiert wird
- B: ein Programm, das einem Agenten über den offenen Standard MCP Werkzeuge mit Name und Beschreibung anbietet
- C: ein Ersatz für das Wissen eines Agenten, z. B. für die IT-Richtlinie
- D: ein Microsoft-Dienst, der neue Agenten automatisch freigibt

**Lösung:**

| Frage | Antwort | Erklärung |
| ----- | ------- | --------- |
| 1. Welche Aktion braucht eine Bestätigung? | **C** | Ein neues Ticket ändert das Ticketsystem; A, B und D lesen nur. |
| 2. Was ist ein MCP-Server? | **B** | Ein MCP-Server bietet Werkzeuge mit Name und Beschreibung an; der Agent liest die Beschreibung und wählt. Er trainiert kein Modell und ersetzt weder Wissen noch Freigabe. |

_Quelle: [Lab 5.3](m05-custom-agents/l03-mcp-actions/l03-mcp-actions-exc.md)._

## Lab 6.1 – Sicherer Einsatz

**1. In Copilot Chat (Work IQ eingeschaltet) wird der Mailverlauf `nordwind-mailverlauf.docx` aus Lab 2.1 zusammengefasst, der im eigenen OneDrive liegt.**

- A: erlaubt
- B: nicht erlaubt
- C: vorher nachfragen

**2. Die Krankmeldung einer Kollegin mit Diagnose wird in einen Prompt kopiert, um eine Vertretungsplanung zu erstellen.**

- A: erlaubt
- B: nicht erlaubt
- C: vorher nachfragen

**3. Eine kostenlose KI-Browsererweiterung, die Webseiten und Mails zusammenfasst, steht nicht auf der Liste der freigegebenen Werkzeuge. Sie wird installiert, weil sie praktisch ist.**

- A: erlaubt
- B: nicht erlaubt
- C: vorher nachfragen

**4. Copilot soll aus Leistungsnotizen eine Rangfolge der Teammitglieder für die nächste Gehaltsrunde erstellen.**

- A: erlaubt
- B: nicht erlaubt
- C: vorher nachfragen

**5. Der „Nordwind IT-Helfer" aus Lab 5.2 soll zusätzlich eine Kundenliste mit Namen und Telefonnummern der Ansprechpartner als Wissen bekommen und danach mit dem ganzen Team geteilt werden.**

- A: erlaubt
- B: nicht erlaubt
- C: vorher nachfragen

**Lösung:**

| Frage | Antwort | Regel | Erklärung |
| ----- | ------- | ----- | --------- |
| 1. Mailverlauf zusammenfassen | **A: erlaubt** | 1, 2, 5 | Freigegebenes Werkzeug, vorhandene Inhalte im eigenen OneDrive, nichts wird aktiv neu eingegeben. Das Ergebnis wird vor der Nutzung mit dem Prüfraster geprüft. |
| 2. Krankmeldung mit Diagnose | **B: nicht erlaubt** | 3 | Eine Diagnose ist eine Gesundheitsangabe und gehört zu den besonderen Kategorien nach Art. 9 DSGVO. Die Vertretungsplanung geht auch ohne Diagnose. |
| 3. Browsererweiterung ohne Freigabe | **B: nicht erlaubt** | 1 | Nicht freigegebene Werkzeuge sind tabu, auch wenn sie praktisch sind; sie sehen Webseiten und Mails mit. Wer sie braucht, beantragt die Freigabe. |
| 4. Rangfolge für die Gehaltsrunde | **B: nicht erlaubt** | 4 | Eine Rangfolge von Personen ist eine Bewertung mit Folgen für Einzelne; die Entscheidung bleibt beim Menschen. |
| 5. Kundenliste als Wissen, Agent teilen | **C: vorher nachfragen** | 1, 2 | Die Liste enthält personenbezogene Daten Dritter, und alle, mit denen der Agent geteilt wird, sehen den Inhalt hochgeladener Dateien. Vorher mit Datenschutz bzw. der in der KI-Richtlinie genannten Stelle klären. |

_Quelle: [Lab 6.1](m06-ai-policy/l01-ai-policy/l01-ai-policy-exc.md)._
## Abschlussquiz

1. Warum liefert ein vager Prompt meist eine durchschnittliche Antwort?
   - A) Copilot ist absichtlich gedrosselt.
   - B) Das Modell wählt ohne Angaben das, was in Texten am häufigsten folgt.
   - C) Vage Prompts werden an ein kleineres Modell weitergeleitet.
   - D) Copilot antwortet nur auf Englisch präzise.
2. Was bringt ein Beispiel im Prompt (Few-Shot)?
   - A) Copilot übernimmt Ton, Länge und Aufbau des Beispiels.
   - B) Copilot übernimmt die Inhalte des Beispiels.
   - C) Copilot sucht im Web nach ähnlichen Texten.
   - D) Nichts, Beispiele werden ignoriert.
3. Was bleibt bei Human in the Loop immer beim Menschen?
   - A) das Ausformulieren aller Sätze
   - B) das Formatieren des Dokuments
   - C) Kernbotschaft, Gliederung und Gewichtung
   - D) die Rechtschreibprüfung
4. Was unterscheidet einen Agenten von einem gespeicherten Prompt?
   - A) Ein Agent ist immer teurer.
   - B) Ein Agent hat einen Namen, feste Anweisungen und eigenes Wissen, mit dem er wiederkehrende Fragen beantwortet.
   - C) Ein Agent braucht keine Prüfung seiner Antworten.
   - D) Es gibt keinen Unterschied.
5. Was muss vor einer ändernden Aktion eines Agenten passieren, z. B. „Ticket anlegen"?
   - A) nichts, der Agent entscheidet selbst
   - B) Der Mensch bestätigt die Aktion.
   - C) Der Agent fragt einen zweiten Agenten.
   - D) Die Aktion wird erst am nächsten Tag ausgeführt.

**Lösung:**

| Frage | Richtig | Erklärung |
| ----- | ------- | --------- |
| 1 | **B** | Ohne Angaben kommt die wahrscheinlichste, also durchschnittlichste Fortsetzung (Lab 1.1). |
| 2 | **A** | Few-Shot zeigt die Form; die Inhalte kommen aus der Quelle (Lab 2.1). |
| 3 | **C** | Entscheidungen behält der Mensch, Ausformulieren darf Copilot (Lab 3.1). |
| 4 | **B** | Ein Agent ist ein gespeicherter Spezialassistent mit Anweisungen und Wissen (Lab 5.1, 5.2). |
| 5 | **B** | Lesende Werkzeuge laufen nach der Freigabe der Verbindung, ändernde Aktionen nur nach Bestätigung (Lab 5.3). |
