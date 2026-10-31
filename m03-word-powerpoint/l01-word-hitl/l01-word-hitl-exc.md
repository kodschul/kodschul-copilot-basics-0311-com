# Lab 3.1 – Übung: Vom Stichpunkt zum Bericht – der Mensch entscheidet

**Ändert die Nordwind-Projektbasis?** Ja — `nordwind-statusbericht.docx` ist die Grundlage für die Präsentation in Lab 3.2.

## Ausgangslage

M. Brandt, Projektleitung bei Nordwind Consulting, braucht für den Lenkungskreis am 06.10.2026 einen einseitigen Statusbericht zum Projekt „Hafenmodernisierung" der Stadtwerke Nordhafen. Vorhanden sind nur lose Stichpunkte.

Dateien im eigenen OneDrive (Kopie der Kursdateien):

- `nordwind-stichpunkte.docx` — unsortierte Stichpunkte, Stand 02.10.2026 (Textfassung: `output/project/nordwind-stichpunkte.md`)
- `nordwind-projektnotizen.docx` — Projektnotizen, Stand 23.09.2026, für den Prüfschritt (Textfassung: `output/project/nordwind-projektnotizen.md`)

Gearbeitet wird in Word mit geöffnetem Copilot-Bereich. Die Prompts stehen auf Prompt-Karte 4; Text in eckigen Klammern wird ersetzt.

### Prompt-Karte 4 – Statusbericht mit Human in the Loop

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

## Aufgaben

1. Lies `nordwind-stichpunkte.docx` und formuliere die Kernbotschaft in ein bis zwei Sätzen selbst, ohne Copilot. Lege danach in Word ein neues Dokument `nordwind-statusbericht.docx` im eigenen OneDrive an und führe Schritt 1 der Prompt-Karte aus; wähle eine Fassung der Kernbotschaft.
2. Führe Schritt 2 aus, beantworte die Rückfragen von Copilot in einer Nachricht und kürze den Gliederungsvorschlag auf höchstens sechs Abschnitte. Optional: Notiere zu jeder Streichung ein Wort als Grund (z. B. „doppelt", „Detail", „keine Entscheidung").
3. Lege je Abschnitt eine Kernaussage in einem Satz fest, führe Schritt 3 aus und danach Schritt 4. Kürze das Ergebnis bei Bedarf auf eine Seite, bestätige oder streiche jede Markierung `[prüfen]`, formatiere die Abschnittstitel als Überschrift 1 (Start → Formatvorlagen) und speichere `nordwind-statusbericht.docx`.
4. Prüfe eine Zahl aus dem Bericht (Budget oder Fortschritt AP2) gegen `nordwind-projektnotizen.docx` und notiere: Zahl, Ergebnis „stimmt" oder „weicht ab", Quelle mit Stand. Optional: Halte das Ergebnis als Kommentar im Bericht fest.

## Checkpoint

- Die eigene Kernbotschaft steht vor der ersten Copilot-Antwort fest.
- Copilot hat in Schritt 2 Fragen gestellt, bevor eine Gliederung erschien.
- Die Gliederung hat höchstens sechs Abschnitte.
- Der Bericht passt auf eine Seite; für einen Wert ist das Prüfergebnis mit Quelle notiert.

## Abschlusskriterien

- `nordwind-statusbericht.docx` liegt im eigenen OneDrive und ist in Lab 3.2 per `/` auffindbar.
- Kernbotschaft und Entscheidungsbedarf (Freigabetermin AP2) stehen im ersten Drittel der Seite.
- Keine Markierung `[prüfen]` ist mehr offen: jede wurde bestätigt oder gestrichen.
- Die Abschnittstitel sind als Word-Überschriften formatiert (Start → Formatvorlagen); daran erkennt PowerPoint in Lab 3.2 die Abschnitte.

## Erweiterung

Führe die Profi-Variante aus und speichere das Ergebnis als `nordwind-statusbericht-gf.docx`. Vergleiche beide Fassungen: Welche Angaben sind weggefallen, und war das jeweils eine bewusste Entscheidung?

## Fallback

Fehlt Copilot in Word oder findet der `/`-Befehl die Datei nicht: Prompt-Karte 4 in Copilot Chat ausführen, `nordwind-stichpunkte.docx` dort hochladen und das Ergebnis aus Schritt 4 in ein Word-Dokument kopieren. Einschränkung: Copilot schreibt dann nicht direkt ins Dokument; Formatierung und Überschriften werden von Hand gesetzt.
