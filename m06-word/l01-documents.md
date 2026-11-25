# Lab 6.1: Word – vom Stichpunkt zum Bericht

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

## Beispiel A · Aus Stichpunkten ein Dokument erstellen

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

## Beispiel B · Schlecht formulierten Text überarbeiten

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

## Beispiel C · Ein Dokument verstehen

```text
Fasse dieses Dokument auf maximal einer Seite zusammen. Konzentriere dich auf die wichtigsten Aussagen, Fristen, Verpflichtungen, Risiken und offenen Punkte.
```

```text
Welche Termine und Fristen werden in diesem Dokument genannt? Stelle sie übersichtlich zusammen.
```

```text
Welche Punkte in diesem Dokument könnten für die Geschäftsführung besonders relevant sein? Begründe kurz, warum.
```

## Beispiel D · Neues Dokument aus einer vorhandenen Datei

Datei: `Vorlage_Projektinformationen_Demo.docx` als Referenz angeben.

```text
Erstelle auf Grundlage der bereitgestellten Projektinformationen eine Entscheidungsvorlage für die Geschäftsführung. Gliedere sie in: Ausgangssituation, aktueller Stand, Handlungsbedarf, finanzielle Auswirkungen, Risiken, Entscheidungsvorschlag. Maximal eine Seite. Verwende ausschließlich Informationen aus der angegebenen Quelle. Kennzeichne Informationen, die für eine Entscheidung noch fehlen.
```

Aus einem Dokument entsteht ein neues für einen anderen Zweck und eine andere Zielgruppe.

## Beispiel E · Text in eine Tabelle umwandeln

Ausgangstext:

```text
Koch29 hat ein Budget von 2,4 Mio. Euro, Fertigstellung Dezember, Status kritisch. Hafen28 hat ein Budget von 2,1 Mio. Euro, Fertigstellung Dezember, Status planmäßig. N39 hat ein Budget von 3,2 Mio. Euro, Fertigstellung März, Status verzögert.
```

Text markieren, dann:

```text
Stelle diese Informationen übersichtlich als Tabelle dar. Verwende die Spalten Objekt, Budget, geplante Fertigstellung und Status.
```

## Bonus · Dokument kritisch prüfen lassen

```text
Prüfe dieses Dokument aus Sicht der Geschäftsführung. Welche Fragen bleiben nach dem Lesen offen? Welche Aussagen sind unklar oder nicht ausreichend belegt? Bei welchen Punkten fehlen Zahlen, Termine oder Verantwortlichkeiten?
```

## Übung Word

**Arbeitsort:** neues Word-Dokument im OneDrive

1. Lass mit den Stichpunkten aus Beispiel A einen Projektstatusbericht erstellen.
2. Lass den Ausgangstext aus Beispiel B professionell überarbeiten.
3. Lass den Ausgangstext aus Beispiel E in eine Tabelle umwandeln.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Bericht enthält Zahlen, die nicht in den Stichpunkten stehen | „Erfinde keine Informationen …“ steht im Prompt? Zahl streichen |
| Umschreiben ändert den ganzen Text | erst den Absatz markieren, dann Copilot fragen |

## Musterergebnis

<details>
<summary>Musterergebnis anzeigen</summary>

Copilot formuliert jedes Mal etwas anders; entscheidend ist, was enthalten ist.

1. **Statusbericht:** sechs Überschriften (Projektstatus, Termine, Budget, Risiken, erforderliche Entscheidungen, nächste Schritte), nur die Fakten aus den Stichpunkten, keine neuen Zahlen.
2. **Überarbeiteter Text (Beispiel):**

> Das Projekt verläuft insgesamt gut. Verzögerungen bei den Elektroarbeiten verschieben die Fertigstellung voraussichtlich. Zudem sind die Kosten gestiegen. Die Geschäftsführung muss entscheiden, ob das Budget erhöht wird.

3. **Tabelle:**

| Objekt | Budget | geplante Fertigstellung | Status |
| ------ | ------ | ----------------------- | ------ |
| Koch29 | 2,4 Mio. € | Dezember | kritisch |
| Hafen28 | 2,1 Mio. € | Dezember | planmäßig |
| N39 | 3,2 Mio. € | März | verzögert |

</details>
