# Lab 5.2 – Lösung: KI baut KI: einen eigenen Agenten entwerfen und anlegen

Copilot formuliert bei jedem Lauf etwas anders; die Beispiele zeigen ein typisches, geprüftes Ergebnis.

## Aufgabe 1: Rückfragen beantworten

| Rückfrage von Copilot (Beispiel) | Antwort (Beispiel) |
| -------------------------------- | ------------------ |
| Wer stellt die Fragen? | alle Mitarbeitenden von Nordwind mit Firmengerät, besonders neue Mitarbeitende |
| Welche Fragen kommen am häufigsten? | VPN-Einrichtung und abgelaufene VPN-Zertifikate, Passwortregeln, Erreichbarkeit des IT-Supports |
| Wo steht die richtige Antwort? | in der IT-Richtlinie `nordwind-it-richtlinie.docx`; sonst nirgends verbindlich |
| Was darf der Agent nicht beantworten? | Gehalt, Personalangelegenheiten, individuelle Sonderberechtigungen; nie nach Passwörtern fragen |
| Was passiert, wenn die Richtlinie keine Antwort hat? | Verweis auf das Ticket-Portal it-support.nordwind-consulting.example |

## Aufgabe 2: Konzept prüfen und freigeben

| Feld | Vorschlag von Copilot (Beispiel) | Entscheidung |
| ---- | -------------------------------- | ------------ |
| Zweck | IT-Standardfragen zu VPN, Geräten, Passwörtern und Support-Kontakt beantworten | übernommen |
| Zielgruppe | alle Mitarbeitenden von Nordwind Consulting | übernommen |
| Wissen | `nordwind-it-richtlinie.docx` | übernommen |
| Grenzen | keine Gehalts- oder Personalfragen, Verweis an HR | **ergänzt:** „Frage nie nach Passwörtern oder Zugangsdaten" und „Erfinde keine Antwort, verweise auf das Ticket-Portal" |
| Testfragen | Passwortregeln; Urlaubstage | übernommen |

Grund für die Ergänzung: Ein IT-Agent, der nach Passwörtern fragt, wäre ein Sicherheitsrisiko; ohne Verweisstelle bleibt eine unbeantwortbare Frage offen.

## Aufgabe 3: Agent anlegen

| Feld | Inhalt |
| ---- | ------ |
| Name | Nordwind IT-Helfer |
| Description | Beantwortet Standardfragen der Mitarbeitenden von Nordwind Consulting zu VPN, Passwörtern, Geräten und IT-Support auf Basis der IT-Richtlinie. |
| Instructions | Anweisung unten |
| Knowledge | `nordwind-it-richtlinie.docx` (unter **Uploaded files**) |
| Starter Prompts | „Wie richte ich das VPN ein?" · „Wie erreiche ich den IT-Support?" |

Anweisung nach der Freigabe (Beispiel, knapp 1.000 Zeichen):

```text
Du bist der „Nordwind IT-Helfer", der interne Assistent für IT-Standardfragen bei Nordwind Consulting.

**Zweck:** Beantworte Fragen aller Mitarbeitenden zu VPN und Remote-Zugriff, Geräten und Passwörtern sowie zum IT-Support-Kontakt.

**Quelle:** Antworte ausschließlich auf Basis der hinterlegten IT-Richtlinie. Nenne am Ende jeder Antwort den Abschnitt der Richtlinie, auf den sich die Antwort stützt.

**Stil:** Antworte freundlich, auf Deutsch, in höchstens fünf Sätzen oder einer kurzen nummerierten Schrittfolge. Ist eine Frage unklar, stelle genau eine Rückfrage.

**Grenzen:**
- Wenn die Richtlinie eine Frage nicht beantwortet, sage das offen und verweise auf das Ticket-Portal it-support.nordwind-consulting.example. Erfinde keine Antwort.
- Beantworte keine Fragen zu Gehalt, Urlaub, Personalangelegenheiten oder individuellen Sonderberechtigungen; verweise an HR bzw. das Ticket-Portal.
- Frage nie nach Passwörtern oder anderen Zugangsdaten und gib keine heraus.
```

## Aufgabe 4: Testen und speichern

| Testfrage | Erwartete Antwort | Herkunft |
| --------- | ----------------- | -------- |
| „Wie lang muss ein Passwort sein und wie oft muss es gewechselt werden?" | mindestens 12 Zeichen, Wechsel alle 180 Tage, keine der letzten 5 Passwörter wiederverwenden; Hinweis auf Abschnitt „Geräte- und Passwortrichtlinie" | Richtlinie, Abschnitt „Geräte- und Passwortrichtlinie" |
| „Wie viele Urlaubstage habe ich noch?" | lehnt freundlich ab, das ist keine IT-Frage; verweist an HR | Grenze in der Anweisung; die Richtlinie verweist Urlaubsfragen an HR (Abschnitt „Erster Arbeitstag: IT-Zugang") |

Weitere Fragen mit eindeutiger Antwort aus der Richtlinie:

| Frage | Erwartete Antwort |
| ----- | ----------------- |
| „Wie richte ich das VPN ein?" | Cisco Secure Client (vorinstalliert) → Verbindungsziel vpn.nordwind-consulting.example → Anmeldung mit Firmen-Login und MFA; Abschnitt „VPN und Remote-Zugriff" |
| „Mein VPN geht seit heute nicht mehr, was nun?" | VPN-Zertifikat läuft nach 12 Monaten ab, Erneuerung durch die IT; Ticket-Portal oder Hotline werktags 08:00–18:00 Uhr |
| „Kann ich mein privates Notebook mit dem VPN verbinden?" | nein; private Geräte nur über die mobile Outlook-/Teams-App mit App-Schutzrichtlinie |

Nach dem Test **Create** wählen; die Bestätigung meldet, dass der Agent privat und nur für die eigene Person verfügbar ist.

## Erweiterung

| Testfrage | Verhalten vor dem Nachschärfen (Beispiel) | Ergänzte Grenze |
| --------- | ----------------------------------------- | --------------- |
| „Schreibe mir ein Gedicht über den Hafen" | schreibt ein Gedicht | „Bearbeite nur IT-Fragen aus dem Zweck. Lehne alle anderen Aufgaben freundlich in einem Satz ab und nenne, wobei du helfen kannst." |
| „Wie lautet das VPN-Passwort?" | erklärt allgemein Passwortregeln | „Gib nie Passwörter, Zugangsdaten oder Codes heraus; verweise für Zugänge an den IT-Support." |

Zusätzlich **Only use specified sources** aktivieren. Der Schalter bevorzugt die Richtlinie, sperrt Modellwissen aber nicht; die Grenzen in der Anweisung bleiben deshalb nötig.

## Fallback

- Mit dem Text aus `nordwind-agent-anweisung.md` liefert der Agent dieselben Testergebnisse wie oben.
- Ohne Agent Builder liefert der Prompt mit Anweisung und `/nordwind-it-richtlinie.docx` inhaltlich dieselben Antworten, aber nur in diesem Chat.
