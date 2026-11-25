# Lab 2.1: Die Prompt-Formel

Ein **Prompt** ist der Auftrag an Copilot, als Text eingetippt.

**Leitfragen:**

<details>
<summary>Was braucht eine neue Kollegin, um einen Bericht ohne Rückfrage zu schreiben?</summary>

Worum es geht, für wen, welche Unterlagen sie nutzen soll und wie das Ergebnis aussehen soll. Copilot braucht dieselben Angaben.

</details>

<details>
<summary>Was kommt heraus, wenn ein Auftrag nur aus vier Wörtern besteht?</summary>

Etwas Allgemeines. Wer nichts vorgibt, bekommt einen Durchschnittstext.

</details>

## Vier Fragen für jeden Prompt

| Teil | Frage | Beispiel |
| ---- | ----- | -------- |
| **Aufgabe** | Was soll Copilot machen? | „Erstelle einen Projektstatusbericht zum Projekt Lindenhof.“ |
| **Kontext** | Für wen und wofür? | „Für das Projektteam.“ |
| **Quelle** | Welche Informationen soll Copilot nutzen? | „Die Protokolle der letzten drei Baubesprechungen.“ |
| **Ergebnis** | Wie soll die Antwort aussehen? | „Drei kurze Abschnitte mit höchstens fünf Stichpunkten.“ |

Ein Prompt muss nicht lang sein. Er muss klar und konkret sein.

## Vorher-Nachher: Projektbericht Lindenhof

Schwach:

```text
Erstelle einen Projektbericht.
```

Es fehlt: welches Projekt, für wen, welche Unterlagen, was wichtig ist, welcher Aufbau, welche Länge.

Stark:

```text
Erstelle einen Projektstatusbericht zum Projekt Lindenhof für das Projektteam. Verwende die Protokolle der letzten drei Baubesprechungen als Grundlage. Konzentriere dich auf erledigte Arbeiten, offene Aufgaben und die nächsten Termine. Gliedere den Bericht in drei kurze Abschnitte mit jeweils höchstens fünf Stichpunkten. Kennzeichne Punkte, zu denen Informationen fehlen. Erfinde keine fehlenden Angaben.
```

Die letzten zwei Sätze sind Qualitätsregeln: Lücken werden sichtbar statt erfunden.

> **Merksatz:** Aufgabe + Kontext + Quelle + gewünschtes Ergebnis.
