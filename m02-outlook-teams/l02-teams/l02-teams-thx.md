# Lab 2.2: Besprechungen nachbereiten und Aufgaben ableiten

**Leitfragen:**

<details>
<summary>Was geht nach einer Besprechung am häufigsten verloren?</summary>

Wer was bis wann erledigt. Besonders Aufgaben, die nur nebenbei erwähnt wurden, hat danach niemand mehr auf dem Zettel.

</details>

<details>
<summary>Ist „Wir schauen uns das an" eine Aufgabe?</summary>

Nur eine angedeutete: Es fehlen Person, Ergebnis und Frist. Eine Aufgabe ist erst zugesagt, wenn jemand sie ausdrücklich übernimmt; alles andere wird nachgefragt.

</details>

<details>
<summary>Wer ist verantwortlich, wenn eine Zusammenfassung etwas Falsches enthält?</summary>

Die Person, die sie weitergibt. Copilot fasst zusammen, was gesagt wurde, nicht, was gemeint war; die Prüfung bleibt bei einem Menschen, der dabei war oder das Transkript gelesen hat.

</details>

- Copilot in Teams beantwortet Fragen zu einer Besprechung während und nach dem Termin, wenn transkribiert wird.
- Copilot hilft auch in Chats und Kanälen: lange Unterhaltungen zusammenfassen, Verpasstes nachholen.
- Aufgaben werden in „zugesagt" und „nur angedeutet" unterschieden; Angedeutetes wird nachgefragt, nicht erfunden.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Transkript | automatisch erstellte Mitschrift einer Besprechung: wer hat wann was gesagt |
| Recap | Registerkarte einer vergangenen Teams-Besprechung mit Aufzeichnung, Transkript, KI-Notizen und Copilot |
| Intelligent Recap | KI-Notizen, Themen und Folgeaufgaben im Recap; enthalten in Teams Premium oder der Copilot-Lizenz |
| zugesagte Aufgabe | eine Person übernimmt ausdrücklich etwas („Ich schicke … bis Freitag.") |
| angedeutete Aufgabe | etwas wird erwähnt, aber niemand übernimmt es verbindlich („Da müsste man mal …") |

## Teams mit Copilot

![Recap einer Teams-Besprechung mit KI-Notizen in der Mitte und Copilot-Bereich rechts, der offene Fragen aus der Besprechung auflistet](https://support.microsoft.com/en-us/teams/media/copilot-in-meeting-recap-revised.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/teams/copilot/catch-up-on-meetings-with-microsoft-365-copilot-in-teams), abgerufen am 31.10.2026._

| Wo | Was Copilot kann | Voraussetzung |
| -- | ---------------- | ------------- |
| während der Besprechung | Fragen zum bisher Besprochenen und zum Besprechungschat beantworten; bei Verspätung über 5 Minuten anbieten, das Verpasste zusammenzufassen | Copilot in der Besprechung aktiv |
| nach der Besprechung | im Besprechungschat oder in der Registerkarte Recap weiterfragen; Antworten nach Word oder Excel übernehmen | Transkription war eingeschaltet |
| Chats | „Was habe ich verpasst?"; Hauptpunkte, Aufgaben, Entscheidungen; standardmäßig die letzten 30 Tage | Copilot-Lizenz |
| Kanäle | Beiträge und Threads zusammenfassen („Summarize thread", ab 1.000 Zeichen) | Copilot-Lizenz |

- Mit der Einstellung „Only during the meeting" läuft Copilot ohne Transkript; nach dem Termin ist dann nichts mehr abrufbar.
- Copilot funktioniert nicht in Besprechungen, die eine andere Organisation ausrichtet.
- Bilder, Loop-Komponenten (gemeinsam bearbeitbare Bausteine im Chat) und geteilte Dateien im Chat fasst Copilot nicht zusammen.

Quellen: [Catch up on meetings](https://support.microsoft.com/en-us/teams/copilot/catch-up-on-meetings-with-microsoft-365-copilot-in-teams), [Copilot in Teams chats and channels](https://support.microsoft.com/en-us/teams/copilot/how-to-use-microsoft-365-copilot-in-teams-chats-and-channels), abgerufen am 31.10.2026.

## Neu 2026 in Teams

- **Facilitator:** KI-Helfer für geplante Besprechungen (eigene Agenten folgen in Lab 5.1), der Live-Notizen schreibt, die Agenda mit Timer verfolgt, Fragen im Besprechungschat beantwortet und aus der Besprechung ein Word-Dokument erstellt; Aufgabenverwaltung mit Microsoft Planner, der Aufgabenliste in Microsoft 365, in der Vorschau ([Microsoft Support](https://support.microsoft.com/en-us/teams/copilot/facilitator-in-microsoft-teams-meetings)).
- **Copilot als Teilnehmer im Gruppenchat:** per @Copilot hinzufügen; verwendet Quellen, die nicht alle sehen dürfen, bestätigt die fragende Person die Antwort vorher; öffentliche Vorschau ([Microsoft Support](https://support.microsoft.com/en-us/teams/chat-channels/how-to-use-microsoft-365-copilot-in-teams-group-chats)).
- **Thread-Zusammenfassung in Kanälen:** „Summarize thread" fasst einen Kanal-Thread direkt am Beitrag zusammen ([Microsoft Support](https://support.microsoft.com/en-us/teams/copilot/how-to-use-microsoft-365-copilot-in-teams-chats-and-channels)).

Stand: 31.10.2026. Verfügbarkeit hängt von Lizenz und Tenant ab; vor Kursbeginn prüfen.

## Transkription: vorher ankündigen

- Transkription wird zu Beginn gestartet und wirkt nicht rückwirkend.
- Alle Teilnehmenden werden vorher informiert; bei Kunden ausdrücklich, nicht nur über das Hinweisbanner.
- Bei sensiblen Themen (Personalfragen, Konflikte) wird bewusst nicht transkribiert; Regeln der eigenen Organisation gehen vor.

## Zugesagt oder nur angedeutet?

| Signal im Gespräch | Einordnung | Beispiel |
| ------------------ | ---------- | -------- |
| „Ich mache …", „Ich schicke … bis …" | zugesagt | „Ich schicke das Protokoll bis Montag." |
| „Ich versuche …" | zugesagt, Ergebnis offen | „Ich versuche, bis Mittwoch eine Antwort vom Einkauf zu bekommen." |
| „Wir schauen uns das mal an", „mal sehen" | nur angedeutet | keine Person, keine Frist |
| „Da müsste man mal …" | nur angedeutet | niemand übernimmt |
| „Wenn …, dann starten wir …" | bedingt | hängt von einer anderen Aufgabe ab |

- Copilot erkennt ausdrückliche Zusagen meist zuverlässig; Angedeutetes fehlt oft oder wird zu einer festen Aufgabe gemacht.
- Auch die Zusammenfassung eines Menschen im Termin kann zu stark sein („Das ist dann ja geklärt"); geprüft wird gegen das Transkript.

> **Merksatz:** Copilot fasst zusammen, was gesagt wurde, nicht, was gemeint war. Was nur angedeutet ist, wird nachgefragt.

## Typische Fehler

| Symptom | Ursache | Lösung |
| ------- | ------- | ------ |
| Copilot in der Besprechung antwortet nicht zum Inhalt | Copilot nicht gestartet oder keine Transkription | Copilot in der Besprechungsleiste starten, Transkription einschalten |
| Nach dem Termin keine Copilot-Antworten | Einstellung „Only during the meeting", kein Transkript | künftig vorab transkribieren; Inhalt nicht rekonstruierbar |
| Aufgabe mit Frist, die nie genannt wurde | Copilot füllt Lücken mit Plausiblem | „Erfinde keine Fristen, schreibe offen" in den Prompt |
| „Mal sehen" steht als feste Aufgabe in der Liste | Andeutung als Zusage gelesen | Status je Aufgabe gegen die Transkriptstelle prüfen |

## Fazit

- Ohne Transkript keine Nachbereitung; Transkription wird vorher angekündigt.
- Eine Aufgabenliste braucht Person, Frist und Status „zugesagt" oder „nur angedeutet".
- Jede Aufgabe wird gegen die Stelle im Transkript geprüft.

In der Übung entsteht mit Prompt-Karte 3 aus dem Jour-fixe-Transkript eine geprüfte Aufgabenliste.
