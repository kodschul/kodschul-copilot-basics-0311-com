# The Nextise Agentic Way

Hintergrund zum Leitmotiv dieses Kurses. Es beschreibt eine Arbeitsweise mit KI und keine Funktion von Copilot. Es gilt für jede App, die im Kurs vorkommt.

- Dieser Kurs ist keine Klick-Schulung für einzelne Copilot-Funktionen.
- Das Ziel: KI so führen, dass sie das Richtige tut, und am Ende KI nutzen, um KI zu bauen.
- Der Mensch entscheidet in jedem Schritt; Copilot liefert Entwürfe.

## Der Denkwechsel

```text
KI kann fast alles formulieren.
  → Die eigene Rolle ist nicht mehr: ihr jeden Handgriff beibringen.
  → Die eigene Rolle ist: sie führen, damit sie das RICHTIGE tut.
```

| Bisher | Mit dem Nextise Agentic Way |
| ------ | --------------------------- |
| Aufgabe selbst lösen, KI nur am Rand nutzen | KI erledigt Entwurf und Ausformulierung, der Mensch steuert |
| KI direkt um eine fertige Lösung bitten („Schreib mir einen Bericht") | erst klären, was eigentlich gebraucht wird, dann bauen lassen |
| Ergebnis übernehmen, wenn es gut klingt | Ergebnis prüfen, bevor es weitergeht |

- Wer der KI direkt eine Lösung beschreibt, überträgt das eigene, oft noch unfertige Lösungsbild.
- Ist das Problem falsch verstanden, baut die KI zuverlässig die falsche Lösung für das falsche Problem.

## Problem vor Lösung: drei Schritte

```text
1. Problem verstehen   →   2. Lösung konzipieren   →   3. Lösung bauen
   Was ist eigentlich         Welche Bausteine            Copilot formuliert
   das Problem?               lösen es?                   und erstellt
```

| Schritt | Leitfrage | Beispiel bei Nordwind Consulting |
| ------- | --------- | -------------------------------- |
| 1. Problem verstehen | Was genau ist das Problem, unabhängig von jeder Lösungsidee? | Der IT-Support beantwortet jede Woche dieselben VPN-Fragen. |
| 2. Lösung konzipieren | Welches Konzept, welche Bausteine lösen dieses Problem? | ein Assistent mit der IT-Richtlinie als Wissen und klaren Grenzen |
| 3. Lösung bauen | Wie wird das Konzept konkret umgesetzt? | Anweisung schreiben, Assistent anlegen, testen |

- Schritt 2 beginnt erst, wenn Schritt 1 klar ist; Schritt 3 erst, wenn das Konzept steht.
- Copilot darf jeden Schritt als Entwurf übernehmen: Rückfragen stellen, Optionen vorschlagen, ausformulieren.

## Human in the Loop

„Human in the Loop" heißt: Ein Mensch bleibt in jeder Schleife des Ablaufs beteiligt und gibt das Ergebnis eines Schritts frei, bevor der nächste beginnt.

| Entscheidet der Mensch | Darf Copilot übernehmen |
| ---------------------- | ----------------------- |
| welches Problem gelöst wird | Rückfragen stellen, Problem zusammenfassen |
| Kernbotschaft, Gliederung, Gewichtung | Varianten vorschlagen |
| welches Konzept überzeugt | Konzept ausarbeiten |
| ob ein Ergebnis fertig ist | ausformulieren, kürzen, umformatieren |

> **Merksatz:** Der Mensch bleibt in jedem Schritt „in the loop": Er entscheidet, welches Problem gelöst wird, welches Konzept überzeugt und wann ein Ergebnis fertig ist.

## Die Drei-Assistenten-Kette als Bild

Die Idee dahinter lässt sich als Kette aus drei Spezialisten zeigen. Jeder übernimmt nur einen Schritt und bekommt das Ergebnis des vorherigen als Eingabe.

```text
Problem
  → [1] Problem-Solver         → klares Problem, beste Idee
  → [2] Solution Architect     → Konzept und Bausteine
  → [3] Anweisungs-Generator   → fertige Anweisung für einen Assistenten
```

- Jeder Schritt kennt den Kontext der vorherigen und liefert deshalb genau das, was in diesem Moment gebraucht wird.
- Das Gegenbild ist ein einziger Auftrag „Bau mir alles": Copilot entscheidet dann alles selbst, nach Wahrscheinlichkeit.
- In diesem Kurs wird die Kette zu einer einzigen Prompt-Karte verdichtet: Copilot stellt Rückfragen zum Problem, schlägt ein Konzept vor und schreibt danach die Anweisung.

## KI nutzen, um KI zu bauen

- Ein eigener Assistent (Agent) braucht eine schriftliche Anweisung: Zweck, Zielgruppe, Wissen, Grenzen.
- Diese Anweisung muss niemand allein schreiben: Copilot entwirft sie in den drei Schritten oben, der Mensch prüft und entscheidet.
- Damit baut KI einen KI-Assistenten, und der Mensch bleibt verantwortlich für das Ergebnis.

## Wo das Leitmotiv im Kurs vorkommt

| Element | Lab | Was dort passiert |
| ------- | --- | ----------------- |
| Problem vor Lösung | jede Prompt-Karte | Ziel und Kontext stehen vor dem Auftrag |
| Human in the Loop | Lab 3.1 | Kernbotschaft und Gliederung entscheidet der Mensch, Copilot formuliert aus |
| Prüfen vor Weitergeben | jede Übung | eine Angabe wird gegen die Quelle geprüft |
| KI baut KI | Lab 5.2 | Copilot entwirft die Anweisung für den Agenten „Nordwind IT-Helfer" |

Angewendet in Lab 3.1 und Lab 5.2.
