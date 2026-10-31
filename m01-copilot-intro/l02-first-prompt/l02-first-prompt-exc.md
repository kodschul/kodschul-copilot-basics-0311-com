# Lab 1.2 – Übung: Der erste gute Prompt

**Ändert die Nordwind-Projektbasis?** Ja — der Kurzüberblick zum Projektstand ist der Hintergrund für Modul 2; Lab 2.1 bleibt auch ohne ihn vollständig machbar.

## Ausgangslage

Nordwind Consulting betreut für die Stadtwerke Nordhafen das Projekt „Hafenmodernisierung". Vor dem nächsten Jour fixe wird ein knapper Überblick über den Projektstand gebraucht.

- Datei: `nordwind-projektnotizen.docx` im eigenen OneDrive (Textfassung: `output/project/nordwind-projektnotizen.md`).
- Werkzeug: Copilot Chat in der Microsoft 365 Copilot App, Work IQ eingeschaltet (Lab 1.1).

### Prompt-Karte 1 – Projektüberblick in fünf Punkten

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

## Aufgaben

1. Öffne Copilot Chat, sende den vagen Prompt „Wie läuft das Projekt?" und lies die Antwort.
2. Öffne einen neuen Chat, tippe die Basis von Prompt-Karte 1 ab oder kopiere sie, wähle beim Tippen von `/nordwind` die Datei `nordwind-projektnotizen.docx` aus der Vorschlagsliste aus und sende den Prompt.
3. Prüfe zwei Angaben aus der Antwort gegen `nordwind-projektnotizen.docx`, z. B. den Fortschritt von AP2 und den verbrauchten Betrag.
4. Stelle im selben Chat eine Nachfrage, die das Ergebnis verbessert (z. B. „Formuliere Punkt 3 so, dass ihn jemand ohne Projektwissen versteht."), und halte in einem Satz fest, was den vagen vom vollständigen Prompt unterscheidet.

## Checkpoint

- Die Antwort aus Aufgabe 2 hat fünf Stichpunkte mit Daten oder Zahlen aus den Projektnotizen.
- Unter der Antwort steht die Datei `nordwind-projektnotizen.docx` als Quelle.
- Zwei Angaben sind gegen die Datei geprüft; Abweichungen sind notiert.

## Abschlusskriterien

- Kurzüberblick zum Projektstand in fünf Punkten liegt vor.
- Ein Satz benennt den Unterschied zwischen vagem und vollständigem Prompt mit mindestens einer der vier Angaben Ziel, Kontext, Quelle, Erwartung.

## Erweiterung

Führe die Profi-Variante aus und vergleiche die Reihenfolge der Punkte mit dem Ergebnis der Basis. Prüfe, ob die zwei Fragen für den Jour fixe auf offene Punkte aus der Datei zurückgehen.

## Fallback

Erscheint die Datei nach `/` nicht: Hänge `nordwind-projektnotizen.docx` über die Hochladen-Schaltfläche im Chatfeld an, oder füge den Text aus `nordwind-projektnotizen.md` in den Prompt ein und schreibe „Nutze nur den folgenden Text" davor. Einschränkung: Die Quellenangabe verweist dann nicht auf die OneDrive-Datei.
