# Lab 3.2 – Übung: Aus dem Bericht eine Präsentation

**Ändert die Nordwind-Projektbasis?** Ja — es entsteht `nordwind-statusbericht.pptx`; spätere Labs bauen nicht darauf auf.

## Ausgangslage

Der Statusbericht aus Lab 3.1 soll im Lenkungskreis am 06.10.2026 als kurze Präsentation gezeigt werden: fünf Folien, je Folie eine Kernaussage.

Dateien im eigenen OneDrive:

- `nordwind-statusbericht.docx` — eigener Bericht aus Lab 3.1
- `nordwind-statusbericht-referenz.docx` — Fallback, falls kein eigener Bericht vorliegt (Textfassung: `output/project/nordwind-statusbericht-referenz.md`)

Gearbeitet wird in PowerPoint mit Copilot (Copilot-Symbol unten rechts).

### Prompt-Karte 5 – Fünf Folien aus dem Bericht

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

## Aufgaben

1. Öffne in PowerPoint eine neue, leere Präsentation (bei vorhandener Unternehmensvorlage diese) und führe „Präsentation erstellen" von Prompt-Karte 5 aus. Ohne eigenen Bericht ersetze im Prompt den Dateinamen durch `/nordwind-statusbericht-referenz.docx`. Beantworte Rückfragen von Copilot oder überspringe sie.
2. Prüfe jede der fünf Folien gegen ihre Kernaussage aus Lab 3.1 und notiere je Folie „trägt" oder „trägt nicht" mit einem Stichwort als Grund.
3. Wähle die schwächste Folie und überarbeite sie mit „Eine Folie überarbeiten" von Prompt-Karte 5.
4. Prüfe eine Zahl und einen Termin auf den Folien gegen den Bericht, korrigiere Abweichungen von Hand und speichere die Präsentation als `nordwind-statusbericht.pptx`.

## Checkpoint

- Die Präsentation hat genau fünf Folien in der vorgegebenen Reihenfolge.
- Für jede Folie liegt ein Prüfergebnis „trägt" oder „trägt nicht" vor.
- Eine Folie wurde per Prompt überarbeitet, die anderen Folien blieben dabei unverändert.

## Abschlusskriterien

- `nordwind-statusbericht.pptx` liegt im eigenen OneDrive.
- Folie 2 nennt den Freigabetermin 09.10.2026 und dass er noch nicht bestätigt ist.
- Keine Folie enthält eine Angabe, die nicht im Bericht steht.

## Erweiterung

Führe die Profi-Variante aus. Vergleiche die Zusammenfassung von Copilot mit der Kernbotschaft aus Lab 3.1: Kommt dieselbe Botschaft heraus? Wenn nicht, welche Folie lenkt ab?

## Fallback

Fehlt Copilot in PowerPoint: Prompt-Karte 5 in Copilot Chat mit hochgeladenem Bericht ausführen und Folientitel samt Stichpunkten als Text erzeugen lassen; die Folien von Hand in PowerPoint anlegen. Einschränkung: Layout und Design entstehen nicht automatisch, der Prüfschritt je Folie bleibt gleich.
