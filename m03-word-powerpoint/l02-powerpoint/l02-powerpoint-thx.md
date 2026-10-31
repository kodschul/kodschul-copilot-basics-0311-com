# Lab 3.2: Aus dem Bericht eine Präsentation

**Leitfragen:**

<details>
<summary>Wie viele Folien braucht eine Kernbotschaft?</summary>

Eine, um sie zu sagen, und je eine Folie für jede Aussage, die sie stützt. Für einen einseitigen Bericht reichen meist fünf.

</details>

<details>
<summary>Was geht verloren, wenn ein Text zu Folien verdichtet wird?</summary>

Begründungen, Bedingungen und Einschränkungen („nicht bestätigt", „Stand 23.09."). Genau diese Details machen eine Zahl richtig oder falsch.

</details>

<details>
<summary>Wer entscheidet, ob eine Folie fertig ist?</summary>

Der Mensch, der präsentiert. Maßstab ist die Kernaussage der Folie aus der Gliederung, nicht, wie gut die Folie aussieht.

</details>

- Copilot in PowerPoint erstellt aus einem Word-Dokument einen Folienentwurf; die Gliederung aus Lab 3.1 bestimmt die Folien.
- Jede Folie wird gegen ihre Kernaussage geprüft und bei Bedarf per Prompt überarbeitet.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Unternehmensvorlage | PowerPoint-Datei mit Farben, Schriften und Folienlayouts des Unternehmens; Copilot baut die Folien mit diesen Layouts. |
| Brand Kit | Im Unternehmen hinterlegte Markenelemente (Logos, Vorlagen, Farben, Schriften), die Copilot auf neue Präsentationen anwendet; wie ein Corporate-Design-Handbuch, das Copilot selbst liest. |
| Sprechernotiz | Text unter der Folie, den nur die vortragende Person sieht. |

## PowerPoint mit Copilot 2026

Copilot öffnet sich über das Copilot-Symbol unten rechts; Vorschläge wie „Create a presentation" und „Add a slide" erscheinen direkt daneben.

![Leere PowerPoint-Präsentation mit Copilot-Symbol unten rechts und den Vorschlägen Create a presentation, Add a slide, Add an image](https://support.microsoft.com/en-us/powerpoint/media/copilot-chat-with-icon.png)

_Quelle: Microsoft Support, „Create a new presentation with Copilot in PowerPoint" (https://support.microsoft.com/en-us/powerpoint/copilot/create-a-new-presentation-with-copilot-in-powerpoint), abgerufen am 31.10.2026._

| Funktion | Beispiel-Prompt | Hinweis |
| -------- | --------------- | ------- |
| Präsentation aus Datei | „Erstelle eine Präsentation aus /nordwind-statusbericht.docx" | Datei per `/` oder über das Plus-Symbol (Add content) einbinden; Word-Dokumente unter 24 MB |
| Folie hinzufügen | „Füge eine Folie zu den nächsten Schritten hinzu" | landet in der geöffneten Präsentation |
| Zusammenfassen | „Fasse diese Präsentation in drei Sätzen zusammen" | gut als Prüfung: Kommt die Kernbotschaft heraus? |
| Unternehmensvorlage | Vorlage öffnen, dann Präsentation erstellen lassen | Copilot nutzt deren Layouts; mit Brand Kit über „Select a brand" |

Copilot stellt beim Erstellen teilweise Rückfragen zu Publikum, Länge oder Design, dieselbe Technik wie „Rückfragen zuerst" aus Lab 3.1. Die Fragen lassen sich beantworten oder überspringen.

## Neu 2026 in PowerPoint

- **Rückfragen und Brand Kit:** Copilot fragt vor dem Erstellen nach Publikum, Länge, Vorlage und Bildsprache; ein im Unternehmen hinterlegtes Brand Kit wird auf die neue Präsentation angewendet ([Microsoft Support, Stand Oktober 2026](https://support.microsoft.com/en-us/powerpoint/copilot/create-a-new-presentation-with-copilot-in-powerpoint)).
- **Folien direkt bearbeiten:** Seit April 2026 ändert Copilot bestehende Präsentationen direkt, aktualisiert Inhalte und hält sich an die Unternehmensvorlagen ([Microsoft 365 Blog, 22.04.2026](https://www.microsoft.com/en-us/copilot/blog/2026/04/22/copilots-agentic-capabilities-in-word-excel-and-powerpoint-are-generally-available/)).
- **Stil einer vorhandenen Präsentation übernehmen:** Wird eine bestehende Präsentation angehängt, übernimmt Copilot deren Design für die neue (Windows, Web; [Release Notes, 27.10.2026](https://learn.microsoft.com/en-us/microsoft-365/copilot/release-notes)).

Stand: 31.10.2026. Oberfläche und Funktionsumfang hängen von Lizenz, Tenant-Einstellungen und Rollout ab; vor dem Kurs im eigenen Tenant prüfen.

## Von der Gliederung zur Folie

Die Arbeit aus Lab 3.1 wird weiterverwendet, nicht neu gemacht: Jeder Abschnitt des Berichts wird zu einer Folie, seine Kernaussage zum Prüfmaßstab.

```text
Bericht (Lab 3.1)                    Präsentation
Kernbotschaft            ──────────▶ Folie 1  Kernbotschaft
Entscheidungsbedarf      ──────────▶ Folie 2  Entscheidungsbedarf
Stand der Arbeitspakete  ──────────▶ Folie 3  Stand der Arbeitspakete
Budget                   ──────────▶ Folie 4  Budget
Risiken + Nächste Schritte ────────▶ Folie 5  Risiken und nächste Schritte
```

Copilot erkennt die Abschnitte am zuverlässigsten, wenn die Abschnittstitel im Word-Dokument als Überschriften formatiert sind.

## Jede Folie gegen ihre Kernaussage prüfen

| Prüffrage | Wenn nein |
| --------- | --------- |
| Trägt die Folie genau ihre Kernaussage? | Folie per Prompt auf diese Aussage zuschneiden |
| Stimmen Zahlen und Termine mit dem Bericht? | Zahl korrigieren, nie aus dem Gedächtnis ergänzen |
| Sind Bedingungen erhalten („nicht bestätigt", Stand)? | Einschränkung wieder aufnehmen |
| Höchstens vier Stichpunkte? | kürzen lassen, Details in die Sprechernotiz |

Überarbeitet wird eine Folie mit einem gezielten Prompt, nicht durch Neuerstellen der ganzen Präsentation: „Überarbeite Folie 3: …".

> **Merksatz:** Eine Folie ist fertig, wenn sie ihre Kernaussage trägt, nicht wenn sie gut aussieht.

## Grenzen

- **Layout:** Copilot wählt Layouts und Bilder selbst; Feinschliff bleibt Handarbeit.
- **Diagramme:** Ein Diagramm entsteht nur zuverlässig, wenn es ausdrücklich angefordert wird; Werte und Achsen werden von Hand geprüft.
- **Zahlen:** Beim Verdichten fallen Einschränkungen weg oder Zahlen werden gerundet; jede Zahl wird gegen den Bericht geprüft.
- **Vorlage:** Ohne Unternehmensvorlage oder Brand Kit wählt Copilot ein eigenes Design.

## Typische Fehler

| Symptom | Ursache | Lösung |
| ------- | ------- | ------ |
| Mehr oder weniger als fünf Folien | Folienzahl nicht vorgegeben | „genau fünf Folien" und die Folientitel im Prompt nennen |
| Folien enthalten Angaben, die nicht im Bericht stehen | Copilot ergänzt Plausibles | „nur Angaben aus dem Bericht" ergänzen; Angabe streichen |
| Folie 1 zeigt nur den Titel | Kernbotschaft nicht als eigene Folie verlangt | Folie 1 ausdrücklich als „Kernbotschaft" anfordern |
| Ganze Präsentation ändert sich beim Überarbeiten | Prompt nennt keine Folie | Foliennummer und Kernaussage im Prompt nennen |
| Bericht wird nicht gefunden | Datei nicht im OneDrive oder anderer Name | Fallback `nordwind-statusbericht-referenz.docx` verwenden |

## Fazit

- Die Gliederung aus Lab 3.1 bestimmt die Folien; Copilot setzt sie um.
- Jede Folie wird gegen ihre Kernaussage geprüft, besonders Zahlen und Einschränkungen.
- Überarbeiten heißt: eine Folie, ein gezielter Prompt.

In der Übung entsteht aus dem eigenen Statusbericht ein geprüfter Entwurf mit fünf Folien.
