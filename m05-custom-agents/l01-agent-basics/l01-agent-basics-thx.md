# Lab 5.1: Was ist ein Agent?

**Leitfragen:**

<details>
<summary>Welche Fragen stellen Kolleginnen und Kollegen immer wieder?</summary>

Typisch sind Standardfragen wie „Wie richte ich das VPN ein?" oder „Wie oft muss ich mein Passwort wechseln?". Bei Nordwind zeigt die Ticketauswertung aus Lab 4.1 VPN als häufigste Kategorie (564 Tickets in zwölf Monaten).

</details>

<details>
<summary>Wann lohnt es sich, einen guten Prompt aufzuheben?</summary>

Wenn dieselbe Aufgabe regelmäßig wiederkommt, mit denselben Quellen und Regeln. Dann wird aus dem Prompt die feste Anweisung eines gespeicherten Assistenten, eines Agenten.

</details>

- Ein Prompt gilt für eine Anfrage; ein Agent speichert Auftrag, Regeln und Wissen dauerhaft.
- Ein Agent lohnt sich für wiederkehrende Aufgaben mit gleichen Quellen und klaren Regeln, nicht für jede Aufgabe.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Agent | ein gespeicherter Spezialassistent in Copilot mit Name, Anweisungen und eigenem Wissen; wie eine neue Kollegin mit Stellenbeschreibung und Handbuch |
| Anweisungen | der feste Auftrag an den Agenten: wofür er da ist, welche Quelle er nutzt, wie er antwortet und was er ablehnt |
| Wissen | Dateien oder Seiten, auf die sich der Agent stützt (Grounding aus Lab 1.1), z. B. eine Richtlinie |
| vorgefertigter Agent | ein Agent, den Microsoft mitliefert und der ohne eigenen Aufbau nutzbar ist |
| eigener Agent | ein Agent, den jemand im Unternehmen für eine bestimmte Aufgabe anlegt |

## Prompt oder Agent?

| Merkmal | Prompt in Copilot Chat | Agent |
| ------- | ---------------------- | ----- |
| Lebensdauer | gilt für diesen Chat | bleibt gespeichert und ist jederzeit wieder aufrufbar |
| Auftrag | jedes Mal neu formulieren (Prompt-Formel aus Lab 1.2) | einmal als Anweisung hinterlegt |
| Quelle | jedes Mal per `/` referenzieren | fest als Wissen hinterlegt |
| Nutzung durch andere | Prompt kopieren und weitergeben | Agent teilen, alle bekommen dasselbe Verhalten |
| Aufwand | keiner | Entwurf, Test und Pflege |

## Woraus ein Agent besteht

| Baustein | Aufgabe | Beispiel „Nordwind IT-Helfer" |
| -------- | ------- | ----------------------------- |
| Name | macht den Agenten auffindbar | Nordwind IT-Helfer |
| Anweisungen | legen Zweck, Quelle, Stil und Grenzen fest | „Beantworte IT-Standardfragen nur aus der IT-Richtlinie." |
| Wissen | liefert die Fakten | `nordwind-it-richtlinie.docx` |
| Startvorschläge | zeigen typische Fragen zum Anklicken | „Wie richte ich das VPN ein?" |

Ein weiterer Baustein sind Aktionen, mit denen ein Agent etwas erledigt statt nur zu antworten (Lab 5.3).

## Vorgefertigte und eigene Agenten

| Art | Beispiele | Wofür |
| --- | --------- | ----- |
| vorgefertigt | **Researcher**: mehrstufige Recherche über Arbeitsdaten und Web, Bericht mit Quellen · **Analyst**: Datenanalyse wie ein Data Scientist, lässt dafür selbst Programmcode rechnen | allgemeine Aufgaben, die in vielen Unternehmen gleich sind |
| eigen | Nordwind IT-Helfer, Reisekosten-Helfer, Onboarding-Helfer | Aufgaben mit eigenen Quellen und eigenen Regeln des Unternehmens |

Researcher und Analyst sind seit 2025 verfügbar und erscheinen bei Copilot-Lizenz in der Agentenliste von Copilot Chat. Welche Agenten sichtbar sind, legt die IT-Administration für die Microsoft-365-Umgebung des Unternehmens (den Tenant) fest. Stand: 31.10.2026, vor Kursbeginn prüfen.

_Quelle: Microsoft 365 Blog, „Introducing Researcher and Analyst in Microsoft 365 Copilot" (https://www.microsoft.com/en-us/microsoft-365/blog/2025/03/25/introducing-researcher-and-analyst-in-microsoft-365-copilot/), abgerufen am 31.10.2026; Microsoft Support, „Get started with Analyst in Microsoft 365 Copilot" (https://support.microsoft.com/en-us/topic/ff505b9c-a06c-4be9-b855-69d89b1d25d2), abgerufen am 31.10.2026._

## Wann lohnt sich ein Agent?

| Einordnung | Merkmale | Beispiel |
| ---------- | -------- | -------- |
| Agent lohnt sich | wiederkehrend, viele Fragende, gleiche Quelle, klare Regeln | Standardfragen zu Reisekosten, beantwortet aus der Reiserichtlinie |
| normaler Prompt reicht | einmalig oder selten, Quelle wechselt jedes Mal | einen bestimmten Mailverlauf einmal zusammenfassen (Lab 2.1) |
| gar nicht an KI geben | Entscheidung über Menschen, Ermessen, hohe Folgen für Einzelne | Leistungsbeurteilung einer Kollegin von Copilot formulieren und bewerten lassen |

- Bewertungen von Personen bleiben beim Menschen, weil sie Ermessen verlangen und Folgen für Einzelne haben; die Regeln dazu stehen in Modul 6.
- Ein Agent für eine Aufgabe ohne stabile Quelle erzeugt Pflegeaufwand statt Entlastung.

> **Merksatz:** Ein Agent ist ein guter Prompt, der bleibt: sinnvoll, wenn sich Frage, Quelle und Regeln wiederholen.

## Fazit

- Ein Agent ist ein gespeicherter Spezialassistent mit Name, Anweisungen und Wissen.
- Vorgefertigte Agenten wie Researcher und Analyst decken allgemeine Aufgaben ab, eigene Agenten die Aufgaben mit eigenen Quellen.
- Wiederkehrend, gleiche Quelle, klare Regeln: Agent. Einmalig: Prompt. Bewertung von Menschen: nicht an KI.

Die Übung ordnet drei Nordwind-Fälle in einem kurzen Quiz ein.
