# Lab 5.2 – Übung: KI baut KI: einen eigenen Agenten entwerfen und anlegen

**Ändert die Nordwind-Projektbasis?** Ja — es entsteht der private Agent „Nordwind IT-Helfer"; Lab 5.3 nutzt ihn als Beispiel für Aktionen.

## Ausgangslage

Lab 4.1 hat gezeigt: VPN ist die häufigste Ticketkategorie bei Nordwind, und VPN-Fragen lassen sich meist mit der IT-Richtlinie beantworten. Daraus entsteht jetzt ein Agent, den Copilot selbst entwirft.

- Datei: `nordwind-it-richtlinie.docx` im eigenen OneDrive (Textzwilling: [`nordwind-it-richtlinie.md`](../../project/nordwind-it-richtlinie.md))
- Werkzeug: Copilot Chat mit eingeschaltetem Work IQ, danach der Agent Builder (**New agent**)
- Fallback-Anweisung: [`nordwind-agent-anweisung.md`](../../project/nordwind-agent-anweisung.md)

### Prompt-Karte 8 – Agent entwerfen

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

## Aufgaben

1. Öffne Copilot Chat mit eingeschaltetem Work IQ, füge Prompt-Karte 8 ein (Basis oder Profi) und beantworte die Rückfragen in Stichworten mit dem Ergebnis aus Lab 4.1.
2. Prüfe den Konzeptvorschlag: ändere oder ergänze mindestens einen Punkt bei Zweck, Wissen oder Grenzen, gib das Konzept frei und kopiere die fertige Anweisung.
3. Öffne **New agent** → **Skip to configure** und fülle **Name** („Nordwind IT-Helfer"), **Description** und **Instructions** (Anweisung aus Aufgabe 2); lade unter **Knowledge** die Datei `nordwind-it-richtlinie.docx` hoch und ergänze zwei **Starter Prompts**.
4. Teste auf **Try it** mit zwei Fragen und speichere danach mit **Create**:
   - „Wie lang muss ein Passwort sein und wie oft muss es gewechselt werden?" Vergleiche die Antwort mit dem Abschnitt „Geräte- und Passwortrichtlinie" in `nordwind-it-richtlinie.md`.
   - „Wie viele Urlaubstage habe ich noch?" Prüfe, ob der Agent ablehnt und weiterverweist.

## Checkpoint

- Copilot hat vor dem Konzept Rückfragen gestellt und vor der Anweisung auf die Freigabe gewartet.
- Das Konzept enthält eine eigene Änderung.
- Der Agent „Nordwind IT-Helfer" erscheint in der Agentenliste von Copilot Chat.
- Die Passwortantwort stimmt mit der Richtlinie überein und nennt den Abschnitt; die Urlaubsfrage wird abgelehnt.

## Abschlusskriterien

- Der private Agent „Nordwind IT-Helfer" ist mit eigener Anweisung und `nordwind-it-richtlinie.docx` als Wissen angelegt.
- Beide Testfragen sind geprüft und das Ergebnis ist notiert.

## Erweiterung

Schärfe die Anweisung, bis fremde Themen sauber abgelehnt werden: teste zusätzlich „Schreibe mir ein Gedicht über den Hafen" und „Wie lautet das VPN-Passwort?", ergänze bei Bedarf die Grenzen, aktiviere unter **Knowledge** den Schalter **Only use specified sources** und teste erneut.

## Fallback

- **Anweisung nicht fertig geworden:** Text aus [`nordwind-agent-anweisung.md`](../../project/nordwind-agent-anweisung.md) in **Instructions** einfügen und mit Aufgabe 3 weitermachen. Einschränkung: der Entwurf mit Copilot entfällt.
- **Agent Builder nicht verfügbar:** Anweisung als Prompt in Copilot Chat einfügen, `/nordwind-it-richtlinie.docx` referenzieren und dieselben zwei Testfragen stellen. Einschränkung: nichts wird gespeichert, die Anweisung muss jedes Mal neu eingefügt werden.
