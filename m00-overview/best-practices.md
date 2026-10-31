# Best Practices

## Prompts

| Regel | Grund |
| ----- | ----- |
| Ziel, Kontext, Quelle und Erwartung nennen | Ohne Angaben liefert das Modell die durchschnittlichste Antwort (Lab 1.1, 1.2). |
| Dateien per `/` referenzieren statt beschreiben | Eine referenzierte Datei ist eindeutig; eine beschriebene muss Copilot erst suchen und findet ggf. die falsche (Lab 1.2). |
| Im selben Chat nachfragen statt neu beginnen | Der bisherige Verlauf bleibt als Kontext erhalten (Lab 1.2). |
| Für Ton und Format ein Beispiel mitgeben | Ein Beispiel zeigt, was sich schwer beschreiben lässt (Few-Shot, Lab 2.1). |
| Bei unklaren Aufträgen zuerst Rückfragen verlangen | Copilot holt sich fehlenden Kontext, statt Lücken zu raten (Lab 3.1). |
| Bei Zahlen und Begründungen „Schritt für Schritt" verlangen | Jeder Zwischenschritt lässt sich einzeln prüfen (Lab 4.1). |
| „Nutze nur die Quelle; fehlt etwas, schreibe [ergänzen]" ergänzen | senkt das Risiko erfundener Angaben (Lab 2.1, 2.2). |

## Arbeiten mit Ergebnissen

| Regel | Grund |
| ----- | ----- |
| Kernbotschaft und Gliederung selbst festlegen | Diese Entscheidungen trifft Copilot sonst nach Wahrscheinlichkeit, nicht nach Absicht (Lab 3.1). |
| Mindestens eine Zahl, ein Datum und einen Namen gegen die Quelle prüfen | Sprachmodelle prüfen keine Fakten; Halluzinationen klingen plausibel (Lab 1.1). |
| Bei Aufgabenlisten „zugesagt" und „nur angedeutet" trennen | Nur Zusagen haben eine verantwortliche Person (Lab 2.2). |
| Formeln und Diagramme gegen eine Kontrollsumme prüfen | Ein falscher Zellbereich fällt sonst nicht auf (Lab 4.1). |
| Makros nur an einer Kopie testen | Ein Makro lässt sich nicht mit „Rückgängig" zurücknehmen (Lab 4.2). |
| Vor dem Senden oder Teilen das Prüfraster anwenden | Verantwortlich bleibt die Person, die das Ergebnis nutzt (Lab 6.1). |

## Agenten

| Regel | Grund |
| ----- | ----- |
| Einen Agenten nur für wiederkehrende Fragen mit fester Quelle bauen | Für Einmaliges reicht ein Prompt (Lab 5.1). |
| Die Anweisung mit Copilot entwerfen, aber selbst freigeben | KI baut KI, der Mensch entscheidet über Zweck und Grenzen (Lab 5.2). |
| Jeden Agenten mit einer Frage außerhalb seines Zwecks testen | Erst dann zeigt sich, ob die Grenzen greifen (Lab 5.2). |
| Ändernde Aktionen nur mit Bestätigung erlauben | Lesen ist harmlos, Anlegen oder Senden verändert Systeme (Lab 5.3). |
| Jede neue Verbindung und jedes neue Wissen freigeben lassen | Jede Verbindung erweitert den Zugriff des Agenten (Lab 5.3, 6.1). |

## Sicherheit

| Regel | Grund |
| ----- | ----- |
| Nur freigegebene Werkzeuge nutzen | Nicht freigegebene Werkzeuge können Daten außerhalb des Unternehmens verarbeiten (Lab 6.1). |
| Personenbezogene Daten nicht ohne Klärung aktiv eingeben | Das Auswerten vorhandener Inhalte im freigegebenen System ist etwas anderes als das Einfügen neuer Daten (Lab 6.1). |
| Im Zweifel vorher nachfragen | Die eigene KI-Richtlinie nennt die zuständigen Ansprechpersonen (Lab 6.1). |
