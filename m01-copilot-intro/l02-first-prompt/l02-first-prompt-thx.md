# Lab 1.2: Der erste gute Prompt

**Leitfragen:**

<details>
<summary>Was braucht eine neue Kollegin, um eine Aufgabe ohne Rückfrage zu erledigen?</summary>

Das Ziel, den Hintergrund (für wen, wozu), die Unterlagen, mit denen sie arbeiten soll, und eine Vorstellung davon, wie das Ergebnis aussehen soll. Genau diese vier Angaben braucht auch Copilot.

</details>

<details>
<summary>Was passiert, wenn ein Auftrag nur aus drei Wörtern besteht?</summary>

Alles Fehlende wird stillschweigend ergänzt: bei Menschen nach Vermutung, bei Copilot nach Wahrscheinlichkeit (Lab 1.1). Heraus kommt eine Durchschnittsantwort.

</details>

<details>
<summary>Woran ist eine gute Antwort erkennbar?</summary>

Sie beantwortet genau den Auftrag, stützt sich auf die genannte Quelle, hält das gewünschte Format ein und lässt sich Punkt für Punkt prüfen.

</details>

- Aus Lab 1.1 folgt: Was nicht im Prompt steht, entscheidet das Modell selbst.
- Vier Angaben machen einen Prompt vollständig: Ziel, Kontext, Quelle, Erwartung.
- Ein guter Prompt ist der Anfang eines Gesprächs; Nachfragen verbessert das Ergebnis schneller als neu beginnen.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Prompt-Formel | die vier Angaben Ziel · Kontext · Quelle · Erwartung, nach denen ein Prompt aufgebaut wird |
| `/`-Referenz | Eingabe von `/` im Copilot-Chatfeld öffnet eine Auswahl, über die eine Datei, Mail, Besprechung oder Person direkt in den Prompt eingefügt wird |
| Nachfrage | weiterer Prompt im selben Chat, der auf der letzten Antwort aufbaut („kürze Punkt 3") |

## Die Prompt-Formel

| Angabe | Frage | Beispiel bei Nordwind Consulting |
| ------ | ----- | -------------------------------- |
| Ziel | Was soll entstehen? | „Fasse den Projektstand in fünf Stichpunkten zusammen." |
| Kontext | Für wen, wozu, aus welcher Rolle? | „Ich bin neu im Projektteam und bereite den Jour fixe vor." |
| Quelle | Womit soll Copilot arbeiten? | „Nutze nur /nordwind-projektnotizen.docx." |
| Erwartung | Wie soll das Ergebnis aussehen? | „Ein Punkt pro Zeile, je mit Datum oder Zahl aus der Datei." |

- Microsoft beschreibt dieselben vier Teile als Goal, Context, Source, Expectations; nur das Ziel ist Pflicht, die anderen machen das Ergebnis brauchbar ([Microsoft Support](https://support.microsoft.com/en-us/microsoft-365-copilot/get-started-writing-prompts-in-microsoft-365-copilot), abgerufen am 31.10.2026).

![Microsoft-Grafik mit vier Kästen Goal, Context, Expectations und Source, je mit Leitfrage und englischem Beispieltext](https://support.microsoft.com/en-us/microsoft-365-copilot/media/prompt-framework.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/microsoft-365-copilot/get-started-writing-prompts-in-microsoft-365-copilot), abgerufen am 31.10.2026._

## Vorher / Nachher

| Variante | Prompt | Typisches Ergebnis |
| -------- | ------ | ------------------ |
| vage | „Wie läuft das Projekt?" | Rückfrage, welches Projekt gemeint ist, oder allgemeine Tipps zum Projektmanagement |
| vollständig | „Fasse den Stand des Projekts Hafenmodernisierung in fünf Stichpunkten zusammen. Ich bin neu im Projektteam und bereite den Jour fixe vor. Nutze nur /nordwind-projektnotizen.docx. Ein Punkt pro Zeile, je mit Datum oder Zahl." | fünf Punkte mit Arbeitspaketen, Budget, offenen Punkten aus der Datei |

> **Merksatz:** Was im Prompt nicht steht, entscheidet das Modell selbst, ohne Rückfrage.

## Dateien per `/` referenzieren

- Im Chatfeld `/` tippen und die ersten Buchstaben des Dateinamens eingeben; Copilot schlägt passende Dateien vor.
- Mit Work IQ an lassen sich so auch Personen, Besprechungen und Mails einfügen; mit Work IQ aus nur Dateien.
- Bis zu zehn Dateien oder Seiten einer SharePoint-Website pro Prompt ([Microsoft Support](https://support.microsoft.com/en-us/microsoft-365-copilot/refer-to-specific-files-and-more-in-microsoft-365-copilot), Stand 31.10.2026).
- Eine referenzierte Datei ist eindeutig; eine beschriebene („die Projektnotizen von letzter Woche") muss Copilot erst suchen und findet ggf. die falsche.

## Nachfragen statt neu beginnen

| Statt | Besser im selben Chat |
| ----- | --------------------- |
| neuen Chat mit längerem Prompt öffnen | „Kürze Punkt 3 auf einen Satz." |
| Ergebnis von Hand umschreiben | „Formuliere das für den Kunden, ohne interne Abkürzungen." |
| Fehler hinnehmen | „In Punkt 2 stimmt der Prozentwert nicht. Prüfe ihn in der Datei." |

- Im selben Chat kennt Copilot den bisherigen Verlauf (Lab 1.1); jede Nachfrage baut darauf auf.
- Ein neuer Chat lohnt sich erst, wenn sich das Thema ändert.

## Typische Fehler

| Symptom | Ursache | Lösung |
| ------- | ------- | ------ |
| Antwort erwähnt fremde Projekte oder Dateien | Quelle nicht referenziert, Copilot sucht frei | Datei per `/` einfügen und „Nutze nur …" ergänzen |
| Datei erscheint nach `/` nicht | Datei liegt nicht im eigenen OneDrive oder wurde gerade erst kopiert | Datei ins eigene OneDrive kopieren, einige Minuten warten, Namen neu eingeben |
| Fließtext statt Stichpunkte | Erwartung fehlt | Format, Anzahl und Länge angeben |
| Zahl im Ergebnis stimmt nicht mit der Datei überein | Halluzination oder Rundung | Zahl in der Datei prüfen, per Nachfrage korrigieren lassen |

## Fazit

- Ziel · Kontext · Quelle · Erwartung: vier Angaben, die jeden Prompt tragen.
- `/` macht die Quelle eindeutig.
- Nachfragen im selben Chat ist schneller als neu beginnen.

In der Übung entsteht mit Prompt-Karte 1 ein Kurzüberblick zum Projekt Hafenmodernisierung.
