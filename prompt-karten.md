# Prompt-Karten

Alle Prompt-Karten des Kurses an einem Ort, zum Kopieren in Copilot. Jede Karte hat eine **Basis**-Fassung und eine **Profi-Variante** für mehr Tiefe. Die Dateien stammen aus `project/` und liegen als Kopie im eigenen OneDrive.

## Prompt-Karte 1 – Projektüberblick in fünf Punkten

**Basis** (zum Kopieren):

```text
Fasse den aktuellen Stand des Projekts Hafenmodernisierung in fünf Stichpunkten zusammen.
Ich bin neu im Projektteam von Nordwind Consulting und bereite mich auf den nächsten Jour fixe mit den Stadtwerken Nordhafen vor.
Nutze nur /nordwind-projektnotizen.docx.
Ein Stichpunkt pro Zeile, jeder mit mindestens einem Datum, einer Zahl oder einem Prozentwert aus der Datei. Markiere offene Punkte mit „offen".
```

**Profi-Variante:**

```text
Ziel: Fasse den aktuellen Stand des Projekts Hafenmodernisierung in fünf Stichpunkten zusammen.
Kontext: Ich bin neu im Projektteam von Nordwind Consulting und bereite mich auf den nächsten Jour fixe mit den Stadtwerken Nordhafen vor. Die Projektleitung möchte wissen, was den Zeitplan gefährdet.
Quelle: Nutze nur /nordwind-projektnotizen.docx. Wenn eine Angabe dort fehlt, schreibe „nicht in der Quelle" statt zu schätzen.
Erwartung: Ein Stichpunkt pro Zeile, Reihenfolge nach Dringlichkeit, jeder mit Datum, Zahl oder Prozentwert aus der Datei. Danach eine Zeile „Fragen für den Jour fixe" mit zwei Fragen an die Stadtwerke.
```

_Verwendet in [Lab 1.2](m01-copilot-intro/l02-first-prompt/l02-first-prompt-exc.md)._

## Prompt-Karte 2 – Kundenantwort im Wunschton (Few-Shot)

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

_Verwendet in [Lab 2.1](m02-outlook-teams/l01-outlook/l01-outlook-exc.md)._

## Prompt-Karte 3 – Aufgaben aus einer Besprechung

**Basis** (zum Kopieren):

```text
Erstelle aus /nordwind-meeting-transkript.docx eine Aufgabenliste als Tabelle mit den Spalten Aufgabe, Verantwortlich, Frist, Status, Uhrzeit im Transkript.
Status ist „zugesagt", wenn eine Person die Aufgabe ausdrücklich übernimmt, sonst „nur angedeutet".
Nutze nur das Transkript. Erfinde keine Fristen: fehlt eine Frist, schreibe „offen".
```

**Profi-Variante:**

```text
Erstelle aus /nordwind-meeting-transkript.docx eine Aufgabenliste als Tabelle mit den Spalten Aufgabe, Verantwortlich, Frist, Status, Uhrzeit im Transkript, wörtliches Zitat.
Status ist „zugesagt", wenn eine Person die Aufgabe ausdrücklich übernimmt, „bedingt", wenn sie von einer anderen Aufgabe abhängt, sonst „nur angedeutet".
Nutze nur das Transkript. Erfinde keine Fristen: fehlt eine Frist, schreibe „offen".
Vergleiche danach die Zusammenfassung von M. Brandt um 10:33 mit dem Transkript und nenne jede Aussage, die stärker oder schwächer formuliert ist als das Besprochene.
Entwirf zum Schluss eine kurze Teams-Nachricht an alle vier Teilnehmenden, die jede angedeutete Aufgabe als Frage formuliert.
```

_Verwendet in [Lab 2.2](m02-outlook-teams/l02-teams/l02-teams-exc.md)._

## Prompt-Karte 4 – Statusbericht mit Human in the Loop

**Basis** (zum Kopieren, Schritt für Schritt nacheinander):

Schritt 1 – Kernbotschaft schärfen:

```text
Meine Kernbotschaft für den Statusbericht an den Lenkungskreis am 06.10. lautet: „[eigene Kernbotschaft in ein bis zwei Sätzen]". Grundlage ist /nordwind-stichpunkte.docx. Schärfe die Kernbotschaft auf höchstens zwei Sätze und biete zwei Alternativen an. Schreibe noch keinen Bericht.
```

Schritt 2 – Gliederung mit Rückfragen:

```text
Schlage für einen einseitigen Statusbericht an den Lenkungskreis eine Gliederung vor. Grundlage ist /nordwind-stichpunkte.docx, die Kernbotschaft lautet: „[gewählte Kernbotschaft]". Stelle mir zuerst bis zu fünf Fragen, bevor du die Gliederung erstellst.
```

Schritt 3 – Kernaussagen prüfen lassen:

```text
Hier ist meine Gliederung mit einer Kernaussage je Abschnitt:
[Abschnitt 1]: [Kernaussage]
[Abschnitt 2]: [Kernaussage]
…
Prüfe für jede Kernaussage, ob sie durch /nordwind-stichpunkte.docx belegt ist, und nenne Lücken oder Widersprüche. Formuliere noch nichts aus.
```

Schritt 4 – Ausformulieren:

```text
Schreibe jetzt den Statusbericht aus Kernbotschaft, Gliederung und Kernaussagen. Höchstens eine Seite, sachlicher Ton, Zielgruppe Lenkungskreis. Verwende nur Angaben aus /nordwind-stichpunkte.docx und nenne den Stand 02.10.2026. Markiere jede Angabe, die nicht in der Quelle steht, mit [prüfen].
```

**Profi-Variante:**

```text
Erstelle aus diesem Statusbericht eine zweite Fassung für die Geschäftsführung von Nordwind Consulting: höchstens eine halbe Seite, der Entscheidungsbedarf steht ganz oben, danach die Kernbotschaft, das Budget in einem Satz und nur das größte Risiko. Keine neuen Angaben, nichts aus der ersten Fassung umdeuten. Stelle mir zuerst bis zu drei Fragen, falls etwas unklar ist.
```

_Verwendet in [Lab 3.1](m03-word-powerpoint/l01-word-hitl/l01-word-hitl-exc.md)._

## Prompt-Karte 5 – Fünf Folien aus dem Bericht

Weicht die eigene Gliederung aus Lab 3.1 ab, ersetze die fünf Folientitel durch die eigenen Abschnitte.

**Basis** (zum Kopieren):

Präsentation erstellen:

```text
Erstelle aus /nordwind-statusbericht.docx eine Präsentation für den Lenkungskreis mit genau fünf Folien: 1. Kernbotschaft, 2. Entscheidungsbedarf, 3. Stand der Arbeitspakete, 4. Budget, 5. Risiken und nächste Schritte. Höchstens vier Stichpunkte je Folie. Verwende nur Angaben aus dem Bericht und übernimm Einschränkungen wie „nicht bestätigt" und den Stand der Zahlen.
```

Eine Folie überarbeiten:

```text
Überarbeite nur Folie [Nummer]. Ihre Kernaussage lautet: „[Kernaussage aus Lab 3.1]". Richte die Folie auf genau diese Aussage aus, höchstens drei Stichpunkte, keine neuen Zahlen. Verschiebe Details in die Sprechernotiz.
```

**Profi-Variante:**

```text
Fasse diese Präsentation in drei Sätzen zusammen. Prüfe danach Folie für Folie, ob jede Zahl und jeder Termin mit /nordwind-statusbericht.docx übereinstimmt, und liste Abweichungen als Tabelle mit Folie, Angabe auf der Folie und Angabe im Bericht. Ergänze zu jeder Folie eine Sprechernotiz mit höchstens drei Sätzen.
```

_Verwendet in [Lab 3.2](m03-word-powerpoint/l02-powerpoint/l02-powerpoint-exc.md)._

## Prompt-Karte 6 – IT-Tickets auswerten

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

_Verwendet in [Lab 4.1](m04-excel/l01-excel-analysis/l01-excel-analysis-exc.md)._

## Prompt-Karte 7 – Makro für die Ticketübersicht

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

_Verwendet in [Lab 4.2](m04-excel/l02-excel-macros/l02-excel-macros-exc.md)._

## Prompt-Karte 8 – Agent entwerfen

**Basis** (zum Kopieren):

```text
Ich möchte einen Copilot-Agenten für ein wiederkehrendes Problem entwerfen. Arbeite in drei Phasen und warte nach Phase 1 und Phase 2 auf meine Antwort.

Ausgangslage: Unser interner IT-Support bei Nordwind Consulting bekommt viele gleiche Fragen. Die Ticketauswertung der letzten zwölf Monate zeigt VPN als häufigste Kategorie (564 von 1.907 Tickets). Die meisten VPN-Fragen lassen sich mit unserer IT-Richtlinie /nordwind-it-richtlinie.docx beantworten.

Phase 1 – Problem verstehen: Stelle mir zuerst bis zu fünf kurze Fragen zum Problem, zum Beispiel wer fragt, was gefragt wird, wo die richtige Antwort steht und was der Agent nicht beantworten darf. Schlage noch keine Lösung vor.

Phase 2 – Agent konzipieren: Schlage nach meinen Antworten in einer Tabelle vor: Zweck, Zielgruppe, Wissen, Grenzen und zwei Testfragen (eine aus der Richtlinie, eine außerhalb des Zwecks). Warte, bis ich das Konzept freigebe oder ändere.

Phase 3 – Anweisung schreiben: Schreibe erst nach meiner Freigabe den Text für das Feld „Anweisungen" im Agent Builder. Sprich den Agenten in der Du-Form an, gliedere in Zweck, Quelle, Stil und Grenzen, schreibe auf Deutsch und bleibe unter 8.000 Zeichen.
```

**Profi-Variante:**

```text
Führe mich als Kette aus drei Rollen zu einem Copilot-Agenten. Wechsle die Rolle erst, wenn ich „Freigegeben" schreibe.

Ausgangslage: Der interne IT-Support von Nordwind Consulting beantwortet viele gleiche Fragen. Ticketauswertung über zwölf Monate: VPN ist mit 564 von 1.907 Tickets die häufigste Kategorie, Spitze im März 2026 mit 118 Tickets nach abgelaufenen VPN-Zertifikaten. Quelle für die Antworten: /nordwind-it-richtlinie.docx.

Rolle 1 – Problem-Solver: Stelle höchstens fünf Fragen zu Zielgruppe, heutigem Ablauf, Nutzen, Quelle und Risiken. Trenne danach in einer kurzen Zusammenfassung belegte Angaben, Annahmen und offene Punkte.

Rolle 2 – Solution Architect: Schlage als Tabelle vor: Zweck, Zielgruppe, Wissen, Grenzen mit Verweisstelle, drei Startvorschläge und vier Testfragen mit erwartetem Verhalten (zwei aus der Richtlinie, eine außerhalb des Zwecks, eine nach Zugangsdaten).

Rolle 3 – Anweisungs-Generator: Schreibe die Anweisung in der Du-Form mit den Abschnitten Zweck, Quelle, Stil und Grenzen, auf Deutsch, unter 8.000 Zeichen, dazu eine Beschreibung mit höchstens 1.000 Zeichen. Prüfe am Ende die Anweisung gegen das freigegebene Konzept und nenne jede Abweichung.
```

_Verwendet in [Lab 5.2](m05-custom-agents/l02-agent-builder/l02-agent-builder-exc.md)._
