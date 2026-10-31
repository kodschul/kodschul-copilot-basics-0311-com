# Lab 4.1: Fragen an einen Datensatz stellen

**Leitfragen:**

<details>
<summary>Welche Fragen an eine Tabelle stellen sich im eigenen Alltag immer wieder?</summary>

Was ist am häufigsten, was ist gestiegen, was fällt aus der Reihe, wie viel macht das insgesamt aus. Genau diese Fragen beantwortet Copilot in Excel in Alltagssprache.

</details>

<details>
<summary>Warum hilft es beim Rechnen, Zwischenschritte aufzuschreiben?</summary>

Weil sich jeder Zwischenschritt einzeln prüfen lässt. Ein Fehler fällt dann an der Stelle auf, an der er entsteht, nicht erst im Ergebnis.

</details>

<details>
<summary>Ist ein Trend schon eine Empfehlung?</summary>

Nein. Ein Trend beschreibt, was passiert ist. Eine Empfehlung braucht zusätzlich Ursache, Aufwand und Ziel; diese Abwägung bleibt beim Menschen.

</details>

- Copilot in Excel beantwortet Fragen an eine Tabelle, schlägt Formeln und Diagramme vor und findet Auffälligkeiten.
- Copilot rechnet nicht „im Kopf", sondern lässt Excel rechnen; „Schritt für Schritt" macht die Begründung prüfbar.

## Begriffe

| Begriff | Bedeutung |
| ------- | --------- |
| Excel-Tabelle | Ein als Tabelle formatierter Bereich (Einfügen → Tabelle) mit Namen und eindeutigen Spaltenüberschriften, z. B. `TicketsJeMonat`. |
| Formel | Rechenanweisung in einer Zelle, z. B. `=SUMME(B2:B13)`; Excel rechnet sie bei jeder Änderung neu. |
| Auffälligkeit (Ausreißer) | Ein Wert, der deutlich vom üblichen Bereich abweicht, z. B. ein Monat mit dreimal so vielen Tickets. |
| Schritt für Schritt (Chain-of-Thought) | Prompt-Technik: Copilot zeigt seinen Lösungsweg in Zwischenschritten, bevor es das Ergebnis nennt; wie ein Rechenweg in der Schule. |

## Excel mit Copilot 2026

Copilot öffnet sich über das Copilot-Symbol unten rechts in Excel. Unter dem Eingabefeld wird festgelegt, ob Copilot die Datei ändern darf.

![Auswahl der Copilot-Modi in Excel: Allow editing, Plan, Chat only](https://support.microsoft.com/en-us/excel/media/copilot-in-excel-modes.png)

_Quelle: Microsoft Support, „Get started with Copilot in Excel" (https://support.microsoft.com/en-us/excel/copilot/get-started-with-copilot-in-excel), abgerufen am 31.10.2026._

| Modus | Was passiert | Passt für |
| ----- | ------------ | --------- |
| Allow editing | Copilot ändert die Arbeitsmappe direkt (Formeln, Diagramme, Formatierung) | Diagramm oder Hilfsspalte anlegen |
| Plan | Copilot schlägt zuerst einen Plan vor, geändert wird erst nach Bestätigung | größere Umbauten; Human in the Loop wie in Lab 3.1 |
| Chat only | Copilot antwortet nur im Chat und ändert nichts | Fragen an die Daten |

## Neu 2026 in Excel

- **Drei Modi:** „Allow editing", „Plan" und „Chat only" stehen in Excel für Windows, Mac und im Web zur Verfügung ([Microsoft Support](https://support.microsoft.com/en-us/excel/copilot/get-started-with-copilot-in-excel)).
- **Python beim Bearbeiten:** Seit August 2026 kann Copilot für Statistik, Simulationen und Visualisierungen Code in der Programmiersprache Python ausführen und die Ergebnisse in die Arbeitsmappe schreiben ([Release Notes, 25.08.2026](https://learn.microsoft.com/en-us/microsoft-365/copilot/release-notes)).
- **Änderungen nachvollziehen:** Seit September 2026 führen Links in der Copilot-Antwort direkt zu geänderten Blättern und Bereichen; der Bereich „Änderungen anzeigen" kennzeichnet, was Copilot geändert hat ([Release Notes, 23.09.2026](https://learn.microsoft.com/en-us/microsoft-365/copilot/release-notes)).

Stand: 31.10.2026. Oberfläche und Funktionsumfang hängen von Lizenz, Tenant-Einstellungen und Rollout ab; vor dem Kurs im eigenen Tenant prüfen.

## Voraussetzungen für gute Antworten

- Die Datei liegt in OneDrive oder SharePoint und hat ein aktuelles Format (`.xlsx`, `.xlsm`, `.xlsb`).
- Die Daten stehen als Excel-Tabelle oder als sauberer Bereich: eine Überschriftenzeile, eindeutige Spaltennamen, keine verbundenen Zellen, keine Leerzeilen. Früher war eine formatierte Tabelle Pflicht; sie bleibt die sicherste Grundlage.
- Spalten oder Tabellen im Prompt beim Namen nennen („Tabelle TicketsJeMonat, Spalte VPN").

## Copilot lässt rechnen, statt zu rechnen

Ein Sprachmodell sagt das wahrscheinlichste nächste Wort voraus (Lab 1.1). Eine Summe „errät" es deshalb nur. Copilot in Excel geht anders vor: Es arbeitet wie eine Projektleitung, die eine Aufgabe weitergibt.

```text
Frage in Alltagssprache  →  Copilot schreibt Formel oder Code  →  Excel rechnet  →  Copilot erklärt das Ergebnis
```

Daraus folgt für die Prüfung: Die Formel ist sichtbar und lässt sich lesen. Copilot im Prompt bitten, die Berechnung als Formel in die Tabelle zu schreiben, macht jedes Ergebnis nachprüfbar.

## Prompt-Technik: Schritt für Schritt

Die Technik fordert den Rechenweg vor dem Ergebnis an: „Gehe Schritt für Schritt vor und zeige jeden Zwischenschritt mit Zahlen, bevor du das Ergebnis nennst."

Beispielfrage an `nordwind-it-tickets.xlsx`: Ist der September 2026 ungewöhnlich?

| Ohne Schritt für Schritt | Mit Schritt für Schritt |
| ------------------------ | ----------------------- |
| „Ja, im September gab es auffällig viele Tickets." | „1. September: 185 Tickets. 2. Monatsdurchschnitt: 1.907 ÷ 12 ≈ 159. 3. Differenz: rund +26. 4. Größter Beitrag: Onboarding mit 24 statt durchschnittlich knapp 8. Ergebnis: Der Anstieg kommt vor allem aus Onboarding. Mögliche Ursache (Vermutung): mehr neue Mitarbeitende." |

| Vorteile | Nachteile |
| -------- | --------- |
| jeder Zwischenschritt ist einzeln prüfbar | längere Antworten |
| Fehler werden dort sichtbar, wo sie entstehen | ein falscher Weg kann trotzdem überzeugend klingen |

**Wann ja:** bei Fragen mit mehreren Rechenschritten, Vergleichen und Empfehlungen.
**Wann nicht:** bei einer einzelnen Zahl („Wie viele VPN-Tickets im März?"); dort reicht die Formel.

> **Merksatz:** Schritt für Schritt macht ein Ergebnis prüfbar, nicht automatisch richtig.

## Vom Trend zur Empfehlung

| Stufe | Frage | Wer liefert |
| ----- | ----- | ----------- |
| Befund | Was zeigen die Zahlen? | Copilot mit Formel |
| Ursache | Warum ist das so? | Copilot nur als Vermutung, bestätigt durch Fachwissen oder Quelle |
| Empfehlung | Was soll passieren? | Mensch, mit Copilot als Sparringspartner |

## Typische Fehler

| Symptom | Ursache | Lösung |
| ------- | ------- | ------ |
| „Summe" erscheint als häufigste Kategorie | Copilot behandelt die Summenspalte wie eine Kategorie | im Prompt „die Spalte Summe ist keine Kategorie" ergänzen |
| Copilot ändert die Datei bei einer reinen Frage | Modus „Allow editing" aktiv | „Chat only" wählen oder Änderung rückgängig machen (Strg+Z) |
| Copilot ist ausgegraut oder findet keine Daten | Datei lokal gespeichert oder altes Format | Datei im eigenen OneDrive öffnen, als `.xlsx` speichern |
| Ursache wird als Tatsache genannt | Copilot ergänzt eine plausible Erklärung | „Kennzeichne Ursachen als Vermutung" ergänzen, Ursache an einer Quelle prüfen |
| Formel heißt `SUM` statt `SUMME` | englische Funktionsnamen | gleiche Funktion; Excel zeigt die Formel in der eingestellten Sprache |

## Grenzen

- Copilot sieht die Daten der Arbeitsmappe, aber nicht die Ursachen dahinter.
- Ein Diagramm ist ein Vorschlag; Diagrammtyp und Achsen entscheidet der Mensch.
- Ergebnisse ohne sichtbare Formel werden mindestens an einem Wert von Hand gegengerechnet.

## Fazit

- Copilot beantwortet Fragen an eine saubere Tabelle und lässt Excel rechnen.
- Die Formel macht ein Ergebnis prüfbar; ein Wert wird immer von Hand gegengerechnet.
- „Schritt für Schritt" legt den Weg zur Empfehlung offen; die Entscheidung bleibt beim Menschen.

In der Übung wird `nordwind-it-tickets.xlsx` ausgewertet: häufigste Kategorie, eine Auffälligkeit, ein Diagramm und eine begründete Empfehlung.
