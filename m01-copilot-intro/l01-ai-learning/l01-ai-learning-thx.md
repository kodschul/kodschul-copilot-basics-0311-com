# Lab 1.1: Wie KI lernt und was Copilot daraus macht

**Leitfragen:**

<details>
<summary>Wie schlägt das Handy beim Tippen das nächste Wort vor?</summary>

Es hat aus sehr vielen Texten gelernt, welches Wort nach den bisherigen Wörtern häufig folgt, und schlägt das wahrscheinlichste vor. Ein Sprachmodell macht dasselbe in sehr großem Maßstab.

</details>

<details>
<summary>Was weiß jemand am ersten Arbeitstag über die eigene Firma – und was nicht?</summary>

Viel Allgemeinwissen aus Ausbildung und Berufserfahrung, aber nichts über laufende Projekte, Kunden und interne Absprachen. Genau so steht ein Sprachmodell da, bevor es Firmendaten sieht.

</details>

<details>
<summary>Woher sollte ein Assistent wissen, was im eigenen Postfach steht?</summary>

Nur, wenn er im Moment der Frage nachsehen darf. Copilot sucht dafür über Microsoft Graph (den Microsoft-Dienst, der Inhalte in Microsoft 365 findet) in den Mails, Chats und Dateien, auf die die angemeldete Person ohnehin Zugriff hat.

</details>

- Ein Sprachmodell lernt einmalig aus riesigen Textmengen und sagt danach Wort für Wort das Wahrscheinlichste voraus.
- Es prüft keine Fakten und lernt im Betrieb nicht dazu; deshalb entscheidet der Prompt über die Qualität.
- Microsoft 365 Copilot verbindet ein Sprachmodell mit den eigenen Microsoft-365-Daten, nur im Rahmen der eigenen Berechtigungen.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Sprachmodell (LLM) | Programm, das aus riesigen Textmengen gelernt hat, Text fortzusetzen; LLM steht für Large Language Model. Bild: Autovervollständigung im Großformat. |
| Token | Textstück, mit dem das Modell rechnet: ein kurzes Wort, eine Silbe oder ein Satzzeichen. „Anforderungskatalog" sind mehrere Token. |
| Training | einmaliger Lernvorgang vor der Nutzung, bei dem das Modell Muster in Texten lernt. Bild: Ausbildung vor dem ersten Arbeitstag. |
| Halluzination | plausibel klingende, aber falsche Aussage des Modells, z. B. ein erfundenes Datum. |
| Grounding | Das Modell bekommt zur Frage passende, echte Inhalte mitgeliefert und stützt die Antwort darauf. Bild: vor der Antwort in die Akte schauen. |
| Microsoft Graph | Microsoft-Dienst, über den Copilot Mails, Termine, Chats und Dateien in Microsoft 365 findet, mit den Rechten der angemeldeten Person. |
| Prompt | die Eingabe an Copilot: Frage, Auftrag und mitgegebene Angaben. |

## KI auf einen Blick

```text
  Training (einmalig)                     Nutzung (bei jeder Frage)
  ───────────────────                     ─────────────────────────
  riesige Textmengen  ──► Sprachmodell ──► Prompt rein ──► wahrscheinlichste
  (Bücher, Web, Code)     (gelernte Muster)                 Fortsetzung raus
```

- **Definition:** Generative KI erzeugt neue Inhalte (Text, Bilder, Code), indem sie gelernte Muster fortsetzt.
- **Analogie:** Die Handy-Autovervollständigung schlägt ein Wort vor; ein Sprachmodell schreibt auf diese Weise ganze Mails, Berichte und Tabellenformeln.

| Datum | Ereignis | Quelle |
| ----- | -------- | ------ |
| Juni 2017 | Forschungsarbeit „Attention Is All You Need" beschreibt die Transformer-Technik, auf der heutige Sprachmodelle aufbauen | [arXiv 1706.03762](https://arxiv.org/abs/1706.03762) |
| 30.11.2022 | OpenAI veröffentlicht ChatGPT; generative KI wird für alle nutzbar | [OpenAI: Introducing ChatGPT](https://openai.com/index/chatgpt/) |
| 01.11.2023 | Microsoft 365 Copilot wird für Unternehmenskunden allgemein verfügbar (angekündigt am 21.09.2023) | [Microsoft 365 Blog, 21.09.2023](https://www.microsoft.com/en-us/microsoft-365/blog/2023/09/21/announcing-microsoft-365-copilot-general-availability-and-microsoft-365-chat/) |
| 2026 | In Copilot Chat ersetzt die Schaltfläche „Work IQ" die bisherigen Registerkarten „Arbeit" und „Web" | [Microsoft Support](https://support.microsoft.com/en-US/Microsoft-365-Copilot/what-information-does-copilot-use-to-answer-my-prompt) |

- **Verbreitung:** Copilot Chat steht allen berechtigten Microsoft-365-Abonnements zur Verfügung; mehr Funktionen gibt es mit der Copilot-Zusatzlizenz ([Microsoft Support](https://support.microsoft.com/en-us/microsoft-365-copilot/how-copilot-chat-works-in-microsoft-365-apps), Stand April 2026).
- **Bekannte Beispiele:** ChatGPT (OpenAI), Microsoft 365 Copilot, Gemini (Google), Claude (Anthropic).
- **Typische Einsätze im Büro:** Mailverlauf zusammenfassen, Antwort entwerfen, Besprechung nachbereiten, aus Stichpunkten einen Bericht machen, Fragen an eine Tabelle stellen.

## Wie ein Sprachmodell lernt

- Beim **Training** liest das Modell einmalig riesige Textmengen und lernt, welche Wörter in welchem Zusammenhang aufeinander folgen.
- Es speichert dabei Muster, keine Faktenliste: Es „weiß", wie ein Statusbericht klingt, aber nicht, wie das eigene Projekt steht.
- Nach dem Training ist das Modell fertig. Im Betrieb lernt es nicht dazu; eine Korrektur im Chat ändert das Modell nicht.
- Microsoft nutzt Prompts, Antworten und über Microsoft Graph abgerufene Daten nicht zum Training der Basismodelle ([Microsoft Learn](https://learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-privacy), Stand 31.10.2026).

## Wie eine Antwort entsteht

```text
„Unser Projekt ist …"  →  Modell bewertet mögliche nächste Wörter
                           erfolgreich  ███████  häufig in Texten
                           verschoben   ███      seltener
                           blau         ▏        kaum
                       →  wählt ein wahrscheinliches Wort, dann das nächste, bis der Text fertig ist
```

- Das Modell wählt, was in ähnlichen Texten **häufig** folgt, nicht, was **wahr** ist.
- Es schlägt nichts nach und prüft nichts. Fehlt eine Angabe, füllt es die Lücke mit etwas Plausiblem: Das ist eine **Halluzination**.
- Dieselbe Frage kann deshalb zweimal leicht unterschiedliche Antworten liefern.

## Warum der Prompt entscheidet

Ohne Angaben liefert das Modell die durchschnittlichste Antwort. Jede Angabe grenzt ein, welcher Teil des Gelernten „aktiviert" wird.

| Prompt | Was das Modell aktiviert | Ergebnis |
| ------ | ------------------------ | -------- |
| „Schreib was über Projekte" | alles, was je über Projekte geschrieben wurde | beliebig, generisch |
| „Schreib als Projektleiterin an den Kunden" | Rolle und Adressat grenzen ein | passender Ton |
| … „in fünf Stichpunkten, ohne Floskeln" | zusätzlich Format und Stil | direkt verwendbar |

## Copilot = Sprachmodell + eigene Daten

```text
Prompt
  → Copilot sucht passende Inhalte über Microsoft Graph (Grounding)
  → nur Mails, Chats, Termine, Dateien, die die Person ohnehin sehen darf
  → Prompt + gefundene Inhalte gehen an das Sprachmodell
  → Antwort mit Quellenangaben zurück in die App
```

- Copilot sieht nur Inhalte, für die die angemeldete Person mindestens Leserechte hat ([Microsoft Learn](https://learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-privacy), Stand 31.10.2026).
- Copilot vergibt keine neuen Rechte. Was falsch freigegeben ist, wird nur schneller gefunden.

> **Merksatz:** Copilot ist der Neue am ersten Arbeitstag, der viel weiß, aber erst in die Akte schauen muss. Der Prompt sagt, welche Akte und was daraus werden soll.

## Copilot Chat und Copilot in den Apps

| | Copilot Chat | Copilot in Outlook, Teams, Word, PowerPoint, Excel |
| --- | --- | --- |
| Wo | Microsoft 365 Copilot App (Web, Desktop, in Teams) und als Seitenbereich in den Apps | direkt in der geöffneten Mail, Besprechung oder Datei |
| Grundlage | Prompt, mitgegebene Dateien, Web; mit Work IQ zusätzlich Arbeitsdaten | der Inhalt, der gerade offen ist, plus Arbeitsdaten |
| Gut für | Fragen über mehrere Quellen, Entwürfe, Recherche | Arbeit am konkreten Dokument: zusammenfassen, entwerfen, überarbeiten |

## Work IQ: Arbeitsdaten an oder aus

| Work IQ | Copilot nutzt | Verfügbar |
| ------- | ------------- | --------- |
| an | Mails, Dateien, Chats, Besprechungen, Personen in Microsoft 365, dazu angehängte Inhalte und Web | mit Copilot-Zusatzlizenz, dort standardmäßig an |
| aus | angehängte Inhalte, öffentliches Web, Profil und persönliche Einstellungen | alle Copilot-Chat-Nutzenden |

- Die Schaltfläche **Work IQ** sitzt oben im Chatfenster und ersetzt die früheren Registerkarten „Arbeit" und „Web" ([Microsoft Support](https://support.microsoft.com/en-US/Microsoft-365-Copilot/what-information-does-copilot-use-to-answer-my-prompt), Stand 31.10.2026).
- Ältere Oberflächen zeigen noch „Arbeit"/„Web"; „Arbeit" entspricht Work IQ an. Verfügbarkeit hängt von Lizenz und Tenant ab; vor Kursbeginn prüfen.
- In der aktuellen Microsoft-Dokumentation heißt das Produkt teils nur „Microsoft Copilot"; gemeint ist dieselbe Lizenz.

## Grenzen

- Was nicht im Training, im Prompt oder in den gefundenen Quellen steht, kennt Copilot nicht und ersetzt es durch Plausibles.
- Zahlen, Daten, Namen und Zitate sind am anfälligsten für Halluzinationen.
- Jede Antwort ist ein Entwurf; die Verantwortung für das Ergebnis bleibt beim Menschen.

## Fazit

- Ein Sprachmodell setzt Text wahrscheinlich fort; es prüft keine Fakten und lernt im Betrieb nicht dazu.
- Der Prompt grenzt ein, was das Modell aktiviert; ohne Angaben kommt die Durchschnittsantwort.
- Copilot holt sich über Microsoft Graph die eigenen Inhalte dazu, nur mit den eigenen Rechten.

In der Übung beantworten drei Quizfragen, wie Copilot zu seiner Antwort kommt.
