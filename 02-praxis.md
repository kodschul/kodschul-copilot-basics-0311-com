# Teil 2 · Copilot in Outlook, Teams, Excel, Word und PowerPoint

Modul 3 bis 7: je App die Beispiele aus der Live-Demo mit Prompt zum Kopieren, danach die Praxisübung.

| Lab | App | Ergebnis der Übung |
| --- | --- | ------------------ |
| [3.1](#lab-31-outlook-e-mails-zusammenfassen-beantworten-und-verbessern) | Outlook | Zusammenfassung und geprüfter Antwortentwurf |
| [4.1](#lab-41-teams-besprechungen-und-chats-zusammenfassen) | Teams | geprüfte Aufgabenliste |
| [5.1](#lab-51-excel-budgetabweichungen-berechnen-und-auswerten) | Excel | Tabelle mit Abweichungen und geprüfte Top 3 |
| [6.1](#lab-61-word-vom-stichpunkt-zum-bericht) | Word | Statusbericht, überarbeiteter Text, Tabelle |
| [7.1](#lab-71-powerpoint-präsentation-erstellen-verbessern-und-vorbereiten) | PowerPoint | Präsentationsentwurf und Fragenliste |

Prompts in den grauen Kästen lassen sich direkt kopieren. Lösungen: [Teil 3](03-spickzettel-und-loesungen.md).

## Lab 3.1: Outlook: E-Mails zusammenfassen, beantworten und verbessern

**Leitfragen:**

<details>
<summary>Wie lange dauert es, einen Verlauf mit acht Nachrichten zu verstehen?</summary>

Oft zehn Minuten und mehr. Copilot fasst ihn in Sekunden zusammen und sucht gezielt Aufgaben, Entscheidungen und Fristen.

</details>

<details>
<summary>Was darf vor dem Senden nie ungeprüft bleiben?</summary>

Termine, Zahlen, Namen und Zusagen.

</details>

<details>
<summary>Wie lässt sich eine dringende Bitte formulieren, ohne Vorwürfe zu machen?</summary>

Sachlich, mit Grund und klarer Frist. Copilot kann einen Entwurf genau darauf umschreiben.

</details>

![Outlook zeigt über einem Mailverlauf den Kasten „Summary by Copilot“ mit Quellenverweisen](https://support.microsoft.com/en-us/outlook/media/email-summary-by-copilot-in-outlook-for-mac.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/outlook/media/email-summary-by-copilot-in-outlook-for-mac.png), abgerufen am 25.11.2026._

Copilot in Outlook fasst Verläufe zusammen, schreibt Antworten und passt Ton und Länge an, ohne die App zu wechseln.

### Beispiel A · Langen Verlauf zusammenfassen

```text
Fasse diesen E-Mail-Verlauf in maximal fünf Stichpunkten zusammen. Nenne anschließend alle offenen Entscheidungen, Aufgaben, verantwortlichen Personen und Termine. Trenne bestätigte Informationen von noch ungeklärten Punkten.
```

Copilot kürzt nicht nur, sondern sucht gezielt nach Aufgaben, Entscheidungen und Fristen.

### Beispiel B · Professionelle Antwort formulieren

```text
Erstelle eine freundliche, aber verbindliche Antwort. Bestätige, dass wir die Unterlagen bis zum 2. Dezember prüfen. Bitte gleichzeitig darum, die noch fehlende Kostenaufstellung vorher zu senden. Die E-Mail soll maximal 120 Wörter lang sein.
```

Folgeprompt:

```text
Formuliere die Antwort etwas kürzer und weniger formell. Die Frist und die Bitte um die Kostenaufstellung müssen erhalten bleiben.
```

### Beispiel C · Unklare Mail sachlich machen

Entwurf: „Hallo, wir brauchen die Unterlagen jetzt endlich. Das wurde schon mehrfach besprochen. Bitte schnell schicken.“

```text
Überarbeite diese E-Mail. Der Ton soll freundlich, professionell und verbindlich sein. Vermeide Vorwürfe. Erkläre kurz, warum die Unterlagen benötigt werden, und nenne den 30. November als spätesten Termin.
```

### Beispiel D · E-Mail aus einer Datei erstellen

Datei in Copilot Chat anhängen (**+**), dann:

```text
Erstelle auf Basis der angehängten Datei eine E-Mail an unseren Projektpartner. Fasse die wichtigsten Informationen aus der Datei in drei bis fünf Stichpunkten zusammen und nenne relevante Zahlen, Termine und offene Punkte. Der Ton soll freundlich und professionell sein. Die E-Mail soll maximal 150 Wörter lang sein. Verwende nur Informationen aus der Datei und kennzeichne fehlende Angaben.
```

Ergebnis immer mit der Originaldatei vergleichen.

### Übung Outlook

**Arbeitsort:** eigenes Postfach · **Datei:** `Übungsblatt Koch29 für Promt und Outlook.docx`

1. Lass einen längeren E-Mail-Verlauf mit dem Prompt aus Beispiel A zusammenfassen.
2. Lass eine Antwort entwerfen und passe mit einem Folgeprompt Ton oder Länge an.
3. Prüfe das Ergebnis: Stimmen Termine, Namen und Aufgaben?

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Copilot-Schaltfläche fehlt | neues Outlook oder Outlook im Web öffnen; Lizenz prüfen |
| Entwurf nennt einen Termin, der nirgends steht | „Verwende nur Informationen aus dem Verlauf.“ ergänzen, Termin streichen |

## Lab 4.1: Teams: Besprechungen und Chats zusammenfassen

**Leitfragen:**

<details>
<summary>Was geht nach einer Besprechung am häufigsten verloren?</summary>

Wer was bis wann erledigt.

</details>

<details>
<summary>Ist „Das klären wir noch“ eine Aufgabe?</summary>

Nur mit Person und Termin. Fehlt beides, gehört es als „nicht festgelegt“ auf die Liste.

</details>

<details>
<summary>Braucht die Geschäftsführung dieselbe Zusammenfassung wie das Projektteam?</summary>

Nein. Dasselbe Material lässt sich für verschiedene Empfänger kürzer oder ausführlicher aufbereiten.

</details>

![Recap einer Teams-Besprechung mit KI-Notizen in der Mitte und Copilot rechts, der offene Fragen auflistet](https://support.microsoft.com/en-us/teams/media/copilot-in-meeting-recap-revised.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/teams/media/copilot-in-meeting-recap-revised.png), abgerufen am 25.11.2026._

Copilot in Teams fasst Chats und Besprechungen zusammen und listet Aufgaben auf. Für Besprechungen muss die **Transkription** (die automatische Mitschrift) laufen; was erlaubt ist, legt das Unternehmen fest.

### Beispiel A · „Ich bin zu spät gekommen“

Während der Besprechung:

```text
Fasse zusammen, was bisher besprochen wurde. Welche Entscheidungen wurden getroffen und welche Fragen sind noch offen?
```

### Beispiel B · Aufgaben aus der Besprechung

```text
Erstelle aus dieser Besprechung eine Aufgabenliste. Nenne zu jeder Aufgabe die verantwortliche Person und den genannten Termin. Wenn keine Person oder kein Termin genannt wurde, kennzeichne dies deutlich als „nicht festgelegt“.
```

Der letzte Satz verhindert, dass Copilot fehlende Angaben als feststehend darstellt.

### Beispiel C · Ergebnis für verschiedene Zielgruppen

```text
Erstelle eine ausführliche Zusammenfassung der Besprechung mit Entscheidungen, Risiken, offenen Fragen und Aufgaben.
```

Danach:

```text
Erstelle daraus eine Kurzfassung für die Geschäftsführung. Verwende maximal sechs Stichpunkte und konzentriere dich auf Entscheidungen, Kosten, Termine und Risiken.
```

### Beispiel D · Teams-Chat zusammenfassen

```text
Fasse die Diskussion der vergangenen sieben Tage zusammen. Welche Vorschläge wurden gemacht, worüber besteht Einigkeit und welche Punkte wurden noch nicht entschieden?
```

### Übung Teams

**Arbeitsort:** eigener Teams-Chat oder eine Besprechung mit Transkription

1. Lass die Diskussion mit dem Prompt aus Beispiel D zusammenfassen.
2. Lass eine Aufgabenliste mit Verantwortlichen und Terminen erstellen.
3. Prüfe, ob fehlende Angaben korrekt als „nicht festgelegt“ gekennzeichnet sind.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Copilot antwortet nicht zur Besprechung | Transkription war aus; bei der nächsten Besprechung einschalten |
| Aufgabe ohne Person wirkt fest vergeben | Satz „nicht festgelegt“ aus Beispiel B ergänzen |

## Lab 5.1: Excel: Budgetabweichungen berechnen und auswerten

**Leitfragen:**

<details>
<summary>Welche Fragen an eine Kostentabelle stellen sich jeden Monat wieder?</summary>

Wo liegen wir über Budget, um wie viel, und welche Objekte sind kritisch?

</details>

<details>
<summary>Ist die größte Überschreitung in Euro auch die größte in Prozent?</summary>

Nicht unbedingt. Ein großes Objekt überschreitet in Euro schnell viel, ein kleines in Prozent. Beide Sichten zählen.

</details>

<details>
<summary>Woran ist erkennbar, ob eine berechnete Zahl stimmt?</summary>

An einer Stichprobe: eine Zeile selbst nachrechnen.

</details>

![Copilot in Excel mit den Modi Allow editing, Plan und Chat only](https://support.microsoft.com/en-us/excel/media/copilot-in-excel-modes.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/excel/media/copilot-in-excel-modes.png), abgerufen am 25.11.2026._

Copilot in Excel ergänzt Spalten mit Formeln, erklärt sie, findet Auffälligkeiten und erstellt Diagramme.

| Voraussetzung | Warum |
| ------------- | ----- |
| Datei liegt im OneDrive oder in SharePoint | sonst ist Copilot in Excel nicht aktiv |
| Daten als Tabelle mit eindeutigen Spaltenüberschriften | Copilot erkennt so, was jede Spalte bedeutet |
| einheitliche Datentypen, keine verbundenen Zellen | sonst rechnet Copilot falsch oder gar nicht |

Die Übungsdatei erfüllt alles bereits (Tabelle `Schulungsdaten`).

### Beispiel A · Abweichungen ermitteln

```text
Ergänze eine Spalte „Budgetabweichung in Euro“. Berechne die Ist-Kosten abzüglich des Budgets.
```

Danach:

```text
Ergänze eine weitere Spalte „Budgetabweichung in Prozent“ und erkläre mir die verwendete Formel.
```

### Beispiel B · Auffälligkeiten erkennen

```text
Analysiere die Tabelle. Welche drei Objekte weisen die größten Budgetüberschreitungen auf? Nenne die Abweichung in Euro und Prozent und beschreibe mögliche Auffälligkeiten in den Daten. Erfinde keine Ursachen, die nicht aus der Tabelle hervorgehen.
```

### Beispiel C · Managementauswertung

```text
Erstelle eine kurze Managementzusammenfassung. Nenne die Gesamtbudgets, die gesamten Ist-Kosten, die größten Abweichungen und alle Objekte mit dem Status „kritisch“. Verwende maximal acht Stichpunkte.
```

### Beispiel D · Visualisierung

```text
Erstelle ein geeignetes Diagramm, das Budget und Ist-Kosten je Objekt gegenüberstellt.
```

Zum Diagramm besprechen: Passt der Diagrammtyp? Sind die Beschriftungen verständlich? Nach Betrag oder Abweichung sortieren? Taugt es für die Geschäftsführung?

### Übung Excel

**Datei:** `Projektkosten – Übung.xlsx` (im eigenen OneDrive)

1. Lass die Spalten zur Budgetabweichung aus Beispiel A ergänzen.
2. Lass die drei Objekte mit den größten Überschreitungen ermitteln.
3. Rechne ein Ergebnis von Copilot stichprobenartig selbst nach.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Copilot ist ausgegraut | Datei aus dem OneDrive öffnen, nicht vom Desktop |
| Prozentspalte zeigt 0,22 statt 22 % | Zelle als Prozent formatieren oder Copilot darum bitten |

## Lab 6.1: Word: vom Stichpunkt zum Bericht

**Leitfragen:**

<details>
<summary>Wie lange dauert der Start eines Berichts mit einer leeren Seite?</summary>

Oft am längsten. Copilot liefert in Sekunden einen ersten Entwurf, an dem weitergearbeitet wird.

</details>

<details>
<summary>Wer liefert die Fakten, wer die Formulierung?</summary>

Die Fakten kommen vom Menschen, Copilot verbessert die Formulierung.

</details>

<details>
<summary>Welche Teile eines vorhandenen Dokuments lassen sich für eine andere Zielgruppe wiederverwenden?</summary>

Fakten, Zahlen, Termine. Aufbau, Länge und Ton ändern sich je nach Leser.

</details>

![Word: neuer Entwurf aus einem bestehenden Dokument über „Reference a file“](https://support.microsoft.com/en-us/word/copilot/media/start-from-exist/start-from-exist-document.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/word/copilot/media/start-from-exist/start-from-exist-document.png), abgerufen am 25.11.2026._

Copilot in Word erstellt Entwürfe aus Stichpunkten oder vorhandenen Dateien, schreibt markierten Text um und beantwortet Fragen zum Dokument.

**Eigenes Dokument als Grundlage:** im Copilot-Feld `/` tippen und die Datei wählen oder über **Datei referenzieren** aus dem OneDrive holen (Bezeichnung im eigenen Word prüfen).

### Beispiel A · Aus Stichpunkten ein Dokument erstellen

Notizen:

```text
Projekt: Sanierung Koch29
Baubeginn März 2026
geplante Fertigstellung Dezember 2026
Budget 2,4 Mio. €
aktuell ca. 70 % fertig
Verzögerung bei Elektroarbeiten
Mehrkosten aktuell ca. 120.000 € (noch in Prüfung)
Entscheidung zur Budgeterhöhung erforderlich
```

```text
Erstelle aus diesen Informationen einen professionellen Projektstatusbericht für die Geschäftsführung. Gliedere ihn in: Projektstatus, Termine, Budget, Risiken, erforderliche Entscheidungen, nächste Schritte. Verwende eine klare und sachliche Sprache. Maximal zwei Seiten. Erfinde keine Informationen, die nicht in meinen Angaben enthalten sind.
```

### Beispiel B · Schlecht formulierten Text überarbeiten

Ausgangstext:

```text
Das Projekt läuft eigentlich ganz gut. Wir haben aber Probleme mit dem Elektriker und deswegen wird es wahrscheinlich später. Die Kosten sind auch höher geworden. Wir müssen jetzt überlegen ob wir das Budget erhöhen.
```

Text markieren, dann:

```text
Überarbeite diesen Text für einen Bericht an die Geschäftsführung. Formuliere professionell, sachlich und präzise. Ändere keine Fakten und füge keine neuen Informationen hinzu.
```

Folgeprompt:

```text
Formuliere den Text noch prägnanter. Maximal 80 Wörter.
```

Der Mensch liefert die Fakten, Copilot verbessert die Formulierung.

### Beispiel C · Ein Dokument verstehen

```text
Fasse dieses Dokument auf maximal einer Seite zusammen. Konzentriere dich auf die wichtigsten Aussagen, Fristen, Verpflichtungen, Risiken und offenen Punkte.
```

```text
Welche Termine und Fristen werden in diesem Dokument genannt? Stelle sie übersichtlich zusammen.
```

```text
Welche Punkte in diesem Dokument könnten für die Geschäftsführung besonders relevant sein? Begründe kurz, warum.
```

### Beispiel D · Neues Dokument aus einer vorhandenen Datei

Datei: `Vorlage_Projektinformationen_Demo.docx` als Referenz angeben.

```text
Erstelle auf Grundlage der bereitgestellten Projektinformationen eine Entscheidungsvorlage für die Geschäftsführung. Gliedere sie in: Ausgangssituation, aktueller Stand, Handlungsbedarf, finanzielle Auswirkungen, Risiken, Entscheidungsvorschlag. Maximal eine Seite. Verwende ausschließlich Informationen aus der angegebenen Quelle. Kennzeichne Informationen, die für eine Entscheidung noch fehlen.
```

Aus einem Dokument entsteht ein neues für einen anderen Zweck und eine andere Zielgruppe.

### Beispiel E · Text in eine Tabelle umwandeln

Ausgangstext:

```text
Koch29 hat ein Budget von 2,4 Mio. Euro, Fertigstellung Dezember, Status kritisch. Hafen28 hat ein Budget von 2,1 Mio. Euro, Fertigstellung Dezember, Status planmäßig. N39 hat ein Budget von 3,2 Mio. Euro, Fertigstellung März, Status verzögert.
```

Text markieren, dann:

```text
Stelle diese Informationen übersichtlich als Tabelle dar. Verwende die Spalten Objekt, Budget, geplante Fertigstellung und Status.
```

### Bonus · Dokument kritisch prüfen lassen

```text
Prüfe dieses Dokument aus Sicht der Geschäftsführung. Welche Fragen bleiben nach dem Lesen offen? Welche Aussagen sind unklar oder nicht ausreichend belegt? Bei welchen Punkten fehlen Zahlen, Termine oder Verantwortlichkeiten?
```

### Übung Word

**Arbeitsort:** neues Word-Dokument im OneDrive

1. Lass mit den Stichpunkten aus Beispiel A einen Projektstatusbericht erstellen.
2. Lass den Ausgangstext aus Beispiel B professionell überarbeiten.
3. Lass den Ausgangstext aus Beispiel E in eine Tabelle umwandeln.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Bericht enthält Zahlen, die nicht in den Stichpunkten stehen | „Erfinde keine Informationen …“ steht im Prompt? Zahl streichen |
| Umschreiben ändert den ganzen Text | erst den Absatz markieren, dann Copilot fragen |

## Lab 7.1: PowerPoint: Präsentation erstellen, verbessern und vorbereiten

**Leitfragen:**

<details>
<summary>Wie viele Folien braucht eine Entscheidung der Geschäftsführung?</summary>

Wenige. Sechs Folien mit kurzen Aussagen reichen meist.

</details>

<details>
<summary>Was geht verloren, wenn ein Bericht zu Folien verdichtet wird?</summary>

Details und Begründungen. Deshalb prüfen, ob die wichtigen Zahlen und Fakten erhalten bleiben.

</details>

<details>
<summary>Welche Frage wäre bei der eigenen letzten Präsentation am unangenehmsten gewesen?</summary>

Meist eine zu Geld, Terminen oder fehlenden Zahlen. Copilot kann solche Fragen vorher sammeln.

</details>

![Leere PowerPoint-Präsentation mit Copilot-Vorschlägen wie Create a presentation und Add a slide](https://support.microsoft.com/en-us/powerpoint/media/copilot-chat-with-icon.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/powerpoint/media/copilot-chat-with-icon.png), abgerufen am 25.11.2026._

Copilot in PowerPoint erstellt Präsentationen aus einem Prompt oder aus einer Datei, kürzt Folientexte, schlägt Gestaltung vor und bereitet auf Fragen vor.

| Word | PowerPoint |
| ---- | ---------- |
| ausführlicher Bericht | Managementpräsentation |

Funktionsnamen können in der deutschen Oberfläche abweichen; im eigenen PowerPoint prüfen.

### Beispiel A · Präsentation aus einem Prompt

```text
Erstelle eine professionelle Präsentation zum aktuellen Stand des Projekts Koch29 für die Geschäftsführung. Erstelle maximal 6 Folien: Ausgangslage, Aktueller Projektstand, Termine, Budgetentwicklung, Risiken, Entscheidungen und nächste Schritte. Verwende kurze und prägnante Aussagen und eine professionelle Managementsprache.
```

Grundlage: Budget 2,4 Mio. €, Fertigstellung geplant Dezember 2026, 70 % fertig, Elektroarbeiten verzögert, ca. 120.000 € Mehrkosten erwartet, Entscheidung über Budgeterhöhung erforderlich. Diese Angaben unter den Prompt schreiben.

### Beispiel B · Präsentation aus einem Word-Dokument

Neue Präsentation → Copilot → **Präsentation aus Datei erstellen** (engl. *Create presentation from file*) → `Vorlage_Projektinformationen_Demo.docx` wählen → Entwurf prüfen.

Überschriften im Word-Dokument helfen Copilot, die Gliederung zu verstehen. Gleiche Informationen, anderer Zweck.

### Beispiel C · Bestehende Folie verbessern

Ausgangsfolie „Projektstatus Koch29“: Fertigstellungsgrad etwa 70 Prozent · Verzögerungen bei den Elektroarbeiten · ursprüngliches Budget 2,4 Millionen Euro · Mehrkosten von ungefähr 120.000 Euro möglich · Geschäftsführung muss über Budgeterhöhung entscheiden.

```text
Überarbeite die Inhalte dieser Folie. Kürze die Aussagen deutlich und formuliere sie für eine Managementpräsentation. Die wesentlichen Zahlen und Fakten müssen erhalten bleiben.
```

```text
Visualisiere diese Folie so, dass Projektfortschritt, Budgetabweichung und Risiko schneller erkennbar sind.
```

Für Folientexte gibt es auch Schnellbefehle wie *Auto-rewrite*, *Condense* und *Make professional*.

### Beispiel D · Lange Präsentation schnell verstehen

```text
Fasse diese Präsentation in maximal 5 Stichpunkten zusammen.
```

```text
Welche drei wichtigsten Entscheidungen müssen aufgrund dieser Präsentation getroffen werden?
```

```text
Welche Risiken werden in der Präsentation genannt?
```

```text
Welche offenen Fragen ergeben sich aus der Präsentation?
```

### Beispiel E · Auf kritische Fragen vorbereiten

```text
Ich präsentiere diese Präsentation morgen vor der Geschäftsführung. Welche kritischen Fragen könnten mir gestellt werden? Konzentriere dich besonders auf Budget, Termine, Risiken und fehlende Informationen.
```

```text
Erstelle zu jeder Frage einen kurzen Antwortvorschlag auf Grundlage dieser Präsentation. Wenn die erforderliche Information nicht vorhanden ist, kennzeichne dies deutlich.
```

Dafür gibt es auch die Funktion *Prepare for Questions* (deutscher Name im eigenen PowerPoint prüfen).

### Beispiel F · Bild erzeugen

```text
Erstelle ein professionelles Bild zum Thema nachhaltige Modernisierung eines Mehrfamilienhauses, das für diese Präsentation geeignet ist.
```

Vor dem Einfügen prüfen: Passt das Bild zur Aussage? Wirkt es professionell? Zeigt es keine echten Personen oder Marken?

### Übung PowerPoint

**Arbeitsort:** neue Präsentation im OneDrive

1. Lass mit dem Prompt aus Beispiel A einen Präsentationsentwurf zu Koch29 erstellen.
2. Lass eine Folie mit einem Folgeprompt kürzen oder visuell verbessern.
3. Lass mit dem Prompt aus Beispiel E kritische Fragen zur Präsentation vorschlagen.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Folien enthalten erfundene Zahlen | Angaben unter den Prompt schreiben, jede Zahl prüfen |
| Präsentation aus Datei findet die Datei nicht | Datei im OneDrive speichern, dann erneut wählen |

Weiter mit Prüf-Checkliste und Lösungen: [Teil 3](03-spickzettel-und-loesungen.md).
