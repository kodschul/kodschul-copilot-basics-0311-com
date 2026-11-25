# Lab 4.1: Teams – Besprechungen und Chats zusammenfassen

**Leitfragen:**

<details>
<summary>Was geht nach einer Besprechung am häufigsten verloren?</summary>

Wer was bis wann erledigt.

</details>

<details>
<summary>Ist „Das klären wir noch“ eine Aufgabe?</summary>

Nur mit Person und Termin. Fehlt beides, gehört es als „nicht festgelegt“ auf die Liste.

</details>

<details>
<summary>Braucht die Geschäftsführung dieselbe Zusammenfassung wie das Projektteam?</summary>

Nein. Dasselbe Material lässt sich für verschiedene Empfänger kürzer oder ausführlicher aufbereiten.

</details>

![Recap einer Teams-Besprechung mit KI-Notizen in der Mitte und Copilot rechts, der offene Fragen auflistet](https://support.microsoft.com/en-us/teams/media/copilot-in-meeting-recap-revised.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/teams/media/copilot-in-meeting-recap-revised.png), abgerufen am 25.11.2026._

Copilot in Teams fasst Chats und Besprechungen zusammen und listet Aufgaben auf. Für Besprechungen muss die **Transkription** (die automatische Mitschrift) laufen; was erlaubt ist, legt das Unternehmen fest.

## Beispiel A · „Ich bin zu spät gekommen“

Während der Besprechung:

```text
Fasse zusammen, was bisher besprochen wurde. Welche Entscheidungen wurden getroffen und welche Fragen sind noch offen?
```

## Beispiel B · Aufgaben aus der Besprechung

```text
Erstelle aus dieser Besprechung eine Aufgabenliste. Nenne zu jeder Aufgabe die verantwortliche Person und den genannten Termin. Wenn keine Person oder kein Termin genannt wurde, kennzeichne dies deutlich als „nicht festgelegt“.
```

Der letzte Satz verhindert, dass Copilot fehlende Angaben als feststehend darstellt.

## Beispiel C · Ergebnis für verschiedene Zielgruppen

```text
Erstelle eine ausführliche Zusammenfassung der Besprechung mit Entscheidungen, Risiken, offenen Fragen und Aufgaben.
```

Danach:

```text
Erstelle daraus eine Kurzfassung für die Geschäftsführung. Verwende maximal sechs Stichpunkte und konzentriere dich auf Entscheidungen, Kosten, Termine und Risiken.
```

## Beispiel D · Teams-Chat zusammenfassen

```text
Fasse die Diskussion der vergangenen sieben Tage zusammen. Welche Vorschläge wurden gemacht, worüber besteht Einigkeit und welche Punkte wurden noch nicht entschieden?
```

## Übung Teams

**Arbeitsort:** eigener Teams-Chat oder eine Besprechung mit Transkription

1. Lass die Diskussion mit dem Prompt aus Beispiel D zusammenfassen.
2. Lass eine Aufgabenliste mit Verantwortlichen und Terminen erstellen.
3. Prüfe, ob fehlende Angaben korrekt als „nicht festgelegt“ gekennzeichnet sind.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Copilot antwortet nicht zur Besprechung | Transkription war aus; bei der nächsten Besprechung einschalten |
| Aufgabe ohne Person wirkt fest vergeben | Satz „nicht festgelegt“ aus Beispiel B ergänzen |

## Musterergebnis

<details>
<summary>Musterergebnis anzeigen</summary>

Copilot formuliert jedes Mal etwas anders; entscheidend ist, was enthalten ist.

1. **Zusammenfassung:** drei Teile: Vorschläge, Einigkeit, noch nicht entschieden.
2. **Aufgabenliste:** Tabelle Aufgabe | verantwortlich | Termin.
3. **Prüfen:** jede Aufgabe ohne Person oder Termin zeigt „nicht festgelegt“. Fehlt das, den Satz aus Beispiel B als Folgeprompt nachreichen.

| Aufgabe | verantwortlich | Termin |
| ------- | -------------- | ------ |
| Kostenaufstellung anfordern | Projektleitung | 30.11. |
| Budgetvorlage vorbereiten | nicht festgelegt | nicht festgelegt |

</details>
