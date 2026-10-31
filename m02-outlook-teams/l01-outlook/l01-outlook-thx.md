# Lab 2.1: E-Mails zusammenfassen und beantworten

**Leitfragen:**

<details>
<summary>Wie lange dauert es, einen Mailverlauf mit sechs Nachrichten zu verstehen?</summary>

Oft mehrere Minuten: Wer hat was zugesagt, welche Frage ist noch offen, was steht in der neuesten Nachricht? Eine Zusammenfassung mit Verweis auf die einzelnen Mails verkürzt das auf Sekunden, ersetzt aber nicht den Blick in die entscheidende Nachricht.

</details>

<details>
<summary>Ist es leichter, einen gewünschten Tonfall zu beschreiben oder ein Beispiel zu zeigen?</summary>

Ein Beispiel zeigen. „Freundlich, aber verbindlich" versteht jeder anders; eine Beispielmail macht Länge, Anrede und Aufbau sofort sichtbar. Diese Technik heißt Few-Shot.

</details>

<details>
<summary>Was darf vor dem Senden nie ungeprüft bleiben?</summary>

Empfänger, jede Zahl, jedes Datum und jede Zusage. Copilot formuliert plausibel, auch wenn eine Angabe nicht in der Quelle steht (Lab 1.1).

</details>

- Copilot in Outlook fasst Verläufe zusammen, entwirft Antworten und gibt Rückmeldung zu einem Entwurf.
- Ein Beispiel im Wunschton steuert den Stil zuverlässiger als eine Beschreibung.
- Vor dem Senden prüft ein Mensch Fakten, Zusagen und Empfänger.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Mailverlauf (Thread) | alle Antworten zu einer Mail, die Outlook als eine Unterhaltung anzeigt |
| Coaching | Copilot-Funktion, die einen selbst geschriebenen Entwurf auf Ton, Klarheit und Wirkung beim Empfänger prüft und Verbesserungen vorschlägt |
| Zero-Shot | Prompt ohne Beispiel: nur die Anweisung |
| Few-Shot | Prompt mit einem oder mehreren Beispielen des gewünschten Ergebnisses; „Shot" steht für ein Beispiel |

## Outlook mit Copilot

![Outlook zeigt über einem Mailverlauf den Kasten „Summary by Copilot" mit drei Absätzen und nummerierten Quellenverweisen](https://support.microsoft.com/en-us/outlook/media/email-summary-by-copilot-in-outlook-for-mac.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/outlook/copilot-pages/summarize-an-email-thread-with-copilot-in-outlook), abgerufen am 31.10.2026._

| Funktion | Wo | Wirkung |
| -------- | -- | ------- |
| Zusammenfassen | „Summary by Copilot" bzw. „Summarize" oben im Verlauf | Kernpunkte des Verlaufs, nummerierte Verweise auf die einzelnen Mails |
| Entwurf | Copilot-Symbol in einer neuen Mail → „Draft", danach „Generate" und „Keep it" | Text aus einem Prompt; Länge und Ton per Auswahl anpassbar |
| Antworten | „Help me reply" in der geöffneten Mail | Copilot öffnet den Chat, stellt ggf. Rückfragen und legt einen Entwurf in die Antwort |
| Coaching | Copilot-Symbol im Entwurf → „Coaching by Copilot" | Vorschläge zu Ton, Klarheit und Wirkung; „Apply all suggestions" übernimmt sie |

Schaltflächen nach der englischen Microsoft-Dokumentation; die deutsche Oberfläche zeigt übersetzte Bezeichnungen. Quellen: [Entwurf](https://support.microsoft.com/en-us/outlook/copilot-pages/draft-an-email-message-with-copilot-in-outlook), [Coaching](https://support.microsoft.com/en-us/outlook/copilot-pages/get-email-coaching-with-copilot-in-outlook), abgerufen am 31.10.2026.

## Neu 2026 in Outlook

- **Antworten im Chat:** „Help me reply" öffnet Copilot Chat neben der Mail; Copilot kann Rückfragen stellen, bevor er den Antwortentwurf einfügt ([Microsoft Support](https://support.microsoft.com/en-us/outlook/copilot-pages/draft-an-email-message-with-copilot-in-outlook)).
- **Coaching mit einem Klick übernehmen:** „Apply all suggestions" schreibt den Entwurf mit allen Vorschlägen neu; einzelne Änderungen bleiben von Hand möglich ([Microsoft Support](https://support.microsoft.com/en-us/outlook/copilot-pages/get-email-coaching-with-copilot-in-outlook)).
- **Posteingang priorisieren:** Copilot stuft eingehende Mails als hoch, normal oder niedrig ein, ersetzt die Vorschauzeile durch eine Kurzfassung und begründet die Einstufung; wird schrittweise ausgerollt ([Microsoft Support](https://support.microsoft.com/en-us/outlook/copilot-outlook/prioritize-my-inbox)).

Stand: 31.10.2026. Verfügbarkeit hängt von Lizenz und Tenant ab; vor Kursbeginn prüfen.

## Zielgruppengerecht schreiben

| Empfänger | Anrede und Ton | Inhalt |
| --------- | -------------- | ------ |
| Kunde | förmlich, freundlich, verbindlich | Antwort auf jede gestellte Frage, nächster Schritt, keine internen Abkürzungen |
| Projektleitung intern | direkt, knapp | Stand, Risiko, Entscheidung, die gebraucht wird |

Im Prompt steht deshalb immer, wer die Mail liest und was sie bei ihm bewirken soll.

## Prompt-Technik: Few-Shot

| | Zero-Shot | Few-Shot |
| --- | --- | --- |
| Prinzip | nur Anweisung („freundlich-sachlich, kurz") | Anweisung plus Beispiel im Wunschton |
| Beispiel-Eingabe | „Beantworte die Mail von Herrn Sievers freundlich-sachlich und kurz." | dieselbe Anweisung + „Schreibe im Stil dieser Beispielmail: Hallo Frau Kramer, danke für Ihre Rückmeldung. Zu Ihren beiden Fragen: 1. … 2. … Viele Grüße" |
| Typische Ausgabe | „Sehr geehrter Herr Sievers, vielen Dank für Ihre ausführliche Nachricht, über die wir uns sehr gefreut haben …" – drei Absätze, Floskeln, Fragen im Fließtext versteckt | „Hallo Herr Sievers, danke für Ihre Rückmeldung. Zu Ihren beiden Fragen: 1. … 2. …" – gleiche Länge und Gliederung wie das Beispiel |
| Vorteile | schnell getippt, kein Beispiel nötig | Ton, Länge, Aufbau sofort getroffen; stabiler über mehrere Versuche |
| Nachteile | Copilot wählt Ton und Aufbau selbst | Beispiel muss passen; Copilot übernimmt auch seine Schwächen und manchmal Inhalte daraus |
| Wann ja | Standardaufgaben, bei denen jeder plausible Stil passt | wiederkehrende Mails mit festem Hausstil, schwer beschreibbarer Ton |
| Wann nicht | wenn ein bestimmter Stil gefordert ist | einmalige Mails ohne Stilvorgabe; wenn kein gutes Beispiel vorliegt |

- Das Beispiel behandelt bewusst ein **anderes Thema**, damit Copilot nur den Stil übernimmt, keine Fakten.
- Ein bis drei Beispiele reichen fast immer.

> **Merksatz:** Few-Shot steuert, wie das Ergebnis aussieht; die Fakten kommen weiterhin nur aus der Quelle.

## Vor dem Senden prüfen

- Ist jede Frage aus der letzten Mail beantwortet?
- Steht jede Zahl, jedes Datum und jede Zusage so in der Quelle? Was fehlt, wird als Platzhalter markiert, nicht erfunden.
- Passen Empfänger, Anrede und Ton zur Person?
- Kommt etwas aus dem Few-Shot-Beispiel in den Inhalt (fremder Name, fremdes Datum)?

## Typische Fehler

| Symptom | Ursache | Lösung |
| ------- | ------- | ------ |
| Entwurf nennt einen Termin, der im Verlauf nicht steht | Copilot ergänzt Plausibles oder zieht mit Work IQ eine spätere Datei heran | „Nutze nur …" in den Prompt, Termin streichen oder als Platzhalter markieren |
| Nur eine der beiden Fragen beantwortet | Erwartung fehlt im Prompt | „Beantworte beide Rückfragen nummeriert." ergänzen |
| Name oder Thema aus der Beispielmail im Entwurf | Few-Shot-Beispiel wurde als Inhalt gelesen | Beispiel klar abgrenzen: „Übernimm nur Ton und Aufbau, keine Inhalte." |
| „Coaching by Copilot" fehlt im Menü | Entwurf noch leer oder Funktion im Tenant nicht verfügbar | zuerst Text in die Mail schreiben bzw. einfügen; sonst Feedback im Chat anfordern |

## Fazit

- Zusammenfassen und Entwerfen spart Lesezeit und das leere Blatt; die Prüfung bleibt.
- Few-Shot: ein Beispiel im Wunschton zeigen statt den Ton zu beschreiben.
- Vor dem Senden: jede Frage beantwortet, jede Angabe in der Quelle belegt.

In der Übung entsteht mit Prompt-Karte 2 die Antwort an die Stadtwerke Nordhafen, einmal ohne und einmal mit Beispielmail.
