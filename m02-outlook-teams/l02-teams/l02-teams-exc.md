# Lab 2.2 – Übung: Besprechungen nachbereiten und Aufgaben ableiten

**Ändert die Nordwind-Projektbasis?** Ja — die geprüfte Aufgabenliste aus dem Jour fixe vom 01.10.2026 ist der Projektstand für die folgenden Module.

## Ausgangslage

Am 01.10.2026 hatte das Projekt Hafenmodernisierung einen Jour fixe mit M. Brandt (Nordwind, Projektleitung), T. Okonkwo (Nordwind, Fachanalyse), K. Sievers (Stadtwerke, Betrieb) und R. Lammers (Stadtwerke, IT). Das Transkript liegt vor; daraus soll eine Aufgabenliste werden, die nach dem Termin an alle geht.

- Datei: `nordwind-meeting-transkript.docx` im eigenen OneDrive (Textfassung: `output/project/nordwind-meeting-transkript.md`).
- Werkzeug für Aufgabe 1: eine laufende oder aufgezeichnete Teams-Besprechung mit Transkript.
- Werkzeug ab Aufgabe 2: Copilot Chat in Teams oder in der Microsoft 365 Copilot App, Work IQ eingeschaltet.

### Prompt-Karte 3 – Aufgaben aus einer Besprechung

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

## Aufgaben

1. Öffne in einer laufenden oder aufgezeichneten Teams-Besprechung mit Transkript Copilot (in der Besprechungsleiste bzw. in der Registerkarte Recap) und frage: „Was wurde bisher besprochen?"
2. Sende in Copilot Chat die Basis von Prompt-Karte 3 und wähle beim Tippen von `/nordwind` die Datei `nordwind-meeting-transkript.docx` aus.
3. Prüfe jede Zeile der Tabelle gegen die genannte Uhrzeit in `nordwind-meeting-transkript.docx`: Stimmen Person, Frist und Status? Korrigiere falsche Einträge im Chat per Nachfrage oder von Hand.
4. Ergänze jede Aufgabe aus dem Transkript, die in der Tabelle fehlt, kennzeichne sie mit „von Hand ergänzt" und notiere den Termin des nächsten Jour fixe.

## Checkpoint

- Aufgabe 1: Copilot nennt Themen der laufenden oder aufgezeichneten Besprechung mit Verweis auf Transkriptstellen.
- Die Tabelle hat für jede Aufgabe eine Person, eine Frist oder „offen" und einen Status.
- Mindestens eine Aufgabe ist „nur angedeutet"; keine Frist steht in der Tabelle, die im Transkript fehlt.

## Abschlusskriterien

- Eine geprüfte Aufgabenliste zum Jour fixe vom 01.10.2026 liegt vor; jede Zeile ist mit einer Uhrzeit im Transkript belegt.
- Der nächste Jour fixe ist mit Datum genannt.

## Erweiterung

Führe die Profi-Variante aus. Prüfe die gefundenen Abweichungen in der Zusammenfassung von 10:33 selbst im Transkript nach und entscheide, ob die vorgeschlagene Teams-Nachricht so verschickt werden könnte.

## Fallback

Läuft keine Besprechung mit Transkript oder ist Copilot in Besprechungen nicht freigegeben, entfällt Aufgabe 1. Öffne stattdessen in Teams die Registerkarte Recap einer vergangenen, transkribierten Besprechung und stelle dort dieselbe Frage. Ohne jede transkribierte Besprechung bleibt nur der Teil mit Prompt-Karte 3. Einschränkung: Das Verhalten von Copilot während einer Besprechung bleibt unbeobachtet.
