# Lab 2.1 – Übung: E-Mails zusammenfassen und beantworten

**Ändert die Nordwind-Projektbasis?** Ja — der geprüfte Antwortentwurf an K. Sievers gilt als vorbereitete Kundenkommunikation; das Transkript in Lab 2.2 setzt zwei Tage später an.

## Ausgangslage

Der Fachbereich Betrieb der Stadtwerke Nordhafen hat den Anforderungskatalog (AP2) gelesen. K. Sievers stellt in seiner Mail vom 29.09.2026 zwei Rückfragen. Die Antwort soll im Namen der Projektleitung M. Brandt entstehen.

- Datei: `nordwind-mailverlauf.docx` im eigenen OneDrive, sechs Mails vom 09.09. bis 29.09.2026 (Textfassung: `output/project/nordwind-mailverlauf.md`).
- Zum Prüfen: `nordwind-projektnotizen.docx` (Textfassung: `output/project/nordwind-projektnotizen.md`).
- Werkzeug: Copilot in Outlook (Copilot-Symbol bzw. Copilot Chat im Outlook-Fenster), Work IQ eingeschaltet. Der Verlauf liegt als Datei vor, deshalb wird er per `/` referenziert (Lab 1.2).

### Prompt-Karte 2 – Kundenantwort im Wunschton (Few-Shot)

**Basis** (zum Kopieren):

```text
Entwirf die Antwort von M. Brandt (Nordwind Consulting) an K. Sievers (Stadtwerke Nordhafen) auf seine letzte Mail vom 29.09.2026 in /nordwind-mailverlauf.docx.
Beantworte beide Rückfragen nummeriert. Nutze nur Angaben aus dem Mailverlauf; fehlt eine Angabe, setze [ergänzen] ein.
Schreibe im Stil der folgenden Beispielmail. Übernimm nur Ton, Länge und Aufbau, keine Inhalte.

Beispielmail:
Hallo Frau Kramer,
danke für Ihre Rückmeldung. Zu Ihren beiden Fragen:
1. Die Schulungsunterlagen fehlen noch, weil wir die Ergebnisse aus dem Testlauf einarbeiten. Sie kommen wie angekündigt bis Freitag.
2. Findet der Testlauf erst im November statt, verschiebt sich der Start um etwa zwei Wochen.
Sobald Sie einen Termin haben, plane ich die nächsten Schritte mit Ihnen.
Viele Grüße
M. Brandt
```

**Profi-Variante:**

```text
Entwirf die Antwort von M. Brandt (Nordwind Consulting) an K. Sievers (Stadtwerke Nordhafen) auf seine letzte Mail vom 29.09.2026 in /nordwind-mailverlauf.docx.
Ziel der Mail: Die Freigabe des Anforderungskatalogs vor dem 15.10. sichern.
Beantworte beide Rückfragen nummeriert. Nutze nur Angaben aus dem Mailverlauf; fehlt eine Angabe, setze [ergänzen] ein und erfinde keine Dauer und kein Datum.
Schreibe im Stil der folgenden Beispielmail. Übernimm nur Ton, Länge und Aufbau, keine Inhalte.

Beispielmail:
Hallo Frau Kramer,
danke für Ihre Rückmeldung. Zu Ihren beiden Fragen:
1. Die Schulungsunterlagen fehlen noch, weil wir die Ergebnisse aus dem Testlauf einarbeiten. Sie kommen wie angekündigt bis Freitag.
2. Findet der Testlauf erst im November statt, verschiebt sich der Start um etwa zwei Wochen.
Sobald Sie einen Termin haben, plane ich die nächsten Schritte mit Ihnen.
Viele Grüße
M. Brandt

Erstelle danach eine interne Kurzfassung für die Projektleitung M. Brandt in drei Stichpunkten: Was fragt der Kunde, was antwortet der Entwurf, was muss die Projektleitung vor dem Senden entscheiden?
```

## Aufgaben

1. Öffne Copilot in Outlook und lass den Verlauf zusammenfassen:

   ```text
   Fasse /nordwind-mailverlauf.docx in fünf Stichpunkten zusammen: Worum geht es, was wurde zugesagt, welche Fragen sind offen? Nenne zu jedem Punkt Datum und Absender.
   ```

2. Erzeuge im selben Chat zuerst einen Antwortentwurf ohne Beispiel (Zero-Shot) mit „Beantworte die letzte Mail von K. Sievers vom 29.09.2026 freundlich-sachlich und kurz.", danach mit der Basis von Prompt-Karte 2 (Few-Shot). Halte in einem Satz fest, worin sich die beiden Entwürfe unterscheiden.
3. Prüfe den Few-Shot-Entwurf: Sind beide Rückfragen beantwortet? Steht jedes Datum und jede Dauer im Mailverlauf? Gleiche eine Angabe gegen `nordwind-projektnotizen.docx` ab (z. B. die Verschiebung der Rollout-Planung oder den Stand des Testsystemzugangs) und markiere fehlende Angaben als `[ergänzen]`.
4. Erstelle in Outlook eine neue Mail mit dem Betreff „AW: Entwurf Anforderungskatalog Leitstand (AP2)", füge den geprüften Entwurf ein, lass das Feld „An" leer und sende die Mail nicht.

## Checkpoint

- Die Zusammenfassung nennt die zwei Rückfragen vom 29.09.2026 und die Einschätzung „Freigabe vor dem 15.10. realistisch".
- Der Few-Shot-Entwurf ist so kurz und so gegliedert wie die Beispielmail und enthält keinen Inhalt aus ihr (keine Frau Kramer, keine Schulungsunterlagen).
- Jede Angabe im Entwurf ist im Mailverlauf belegt oder als `[ergänzen]` markiert.

## Abschlusskriterien

- Ein versandfertiger Entwurf liegt als ungesendete Mail in Outlook vor; offen ist nur, was die Projektleitung entscheiden muss.
- Ein Satz benennt den Unterschied zwischen Zero-Shot- und Few-Shot-Entwurf.

## Erweiterung

1. Wähle in der Mail aus Aufgabe 4 über das Copilot-Symbol „Coaching by Copilot", übernimm einen Vorschlag oder verwirf ihn mit einer kurzen Begründung.
2. Führe die Profi-Variante von Prompt-Karte 2 aus und vergleiche die interne Kurzfassung mit dem Kundenentwurf in Ton und Detailtiefe.

## Fallback

Ist Copilot in Outlook nicht verfügbar: Führe dieselben Prompts in Copilot Chat in der Microsoft 365 Copilot App aus und kopiere den Entwurf in eine neue Outlook-Mail. Fehlt „Coaching by Copilot": Sende im Chat „Gib mir Rückmeldung zu Ton, Klarheit und Wirkung dieses Entwurfs" zusammen mit dem eingefügten Entwurf. Einschränkung: Die Rückmeldung ändert den Text in der Mail nicht direkt.
