# Teil 3 · Spickzettel, Prüf-Checkliste und Lösungen

Modul 8 zum Mitnehmen und die Lösungen zu allen Übungen aus Teil 1 und 2.

## Lab 8.1: Prüf-Checkliste und Zusammenfassung

**Leitfragen:**

<details>
<summary>Welches Ergebnis von heute wäre ohne Prüfen fehlerhaft weitergegeben worden?</summary>

Meist eine Zahl, ein Termin oder ein Name. Genau dort setzt die Prüf-Checkliste an.

</details>

<details>
<summary>Welche Aufgabe der nächsten Woche eignet sich als erster Versuch?</summary>

Eine, die oft vorkommt und wenig Risiko hat: Mailverlauf zusammenfassen, Protokoll aufbereiten, Bericht beginnen.

</details>

### Fünf Kernpunkte zu Copilot

1. Copilot ist ein Assistent, der Entwürfe liefert. Die Verantwortung bleibt beim Menschen.
2. Gute Prompts folgen der Formel **Aufgabe + Kontext + Quelle + gewünschtes Ergebnis**.
3. Mit Folgeprompts wird ein Ergebnis Schritt für Schritt besser.
4. Copilot hilft in Outlook, Teams, Excel, Word und PowerPoint jeweils anders.
5. Ergebnisse werden immer geprüft, besonders Zahlen, Termine und Namen.

### Prüf-Checkliste

| Vor dem Weitergeben prüfen | ✓ |
| -------------------------- | - |
| Zahlen und Berechnungen stimmen (Stichprobe nachgerechnet) | |
| Fristen und Termine stehen so in der Quelle | |
| Namen und Zuständigkeiten sind richtig | |
| Aussagen zu Verträgen und Recht sind fachlich geprüft | |
| keine vertraulichen Inhalte an falsche Empfänger | |
| fehlende Angaben sind gekennzeichnet, nicht erfunden | |

### Qualitätsregeln für jeden Prompt

```text
Verwende nur Informationen aus der angegebenen Quelle.
Kennzeichne fehlende Angaben.
Erfinde keine fehlenden Angaben.
```

> **Merksatz:** Klar fragen, kritisch prüfen, verantwortungsvoll nutzen.

---

## Lösungen

Copilot formuliert jedes Mal etwas anders. Die Beispielergebnisse zeigen, was enthalten sein muss, nicht den genauen Wortlaut.

### Lab 2.2: Übung Koch29

**Musterprompt:**

```text
Erstelle auf Grundlage des Dokuments Koch29 eine kurze Zusammenfassung des aktuellen Projektstands für die Geschäftsführung. Konzentriere dich auf Projektfortschritt, Budget, Termine, Risiken und erforderliche Entscheidungen. Fasse das Ergebnis in maximal acht Stichpunkten zusammen. Stelle wichtige Zahlen und Termine deutlich heraus. Trenne bestätigte Informationen von noch ungeklärten Punkten. Erfinde keine fehlenden Angaben.
```

| Teil | im Musterprompt |
| ---- | --------------- |
| Aufgabe | kurze Zusammenfassung des Projektstands |
| Kontext | für die Geschäftsführung |
| Quelle | das Dokument Koch29 |
| Ergebnis | höchstens acht Stichpunkte, Zahlen und Termine hervorgehoben, bestätigt und offen getrennt |

**Beispielergebnis:**

- **Bestätigt:** 48 Wohnungen in Modernisierung, Beginn März 2026, ca. **70 %** fertig
- **Bestätigt:** Budget **2,4 Mio. €**, davon ca. **1,85 Mio. €** ausgegeben oder beauftragt
- **Bestätigt:** Elektroarbeiten ca. **drei Wochen** hinter dem Zeitplan
- **Offen:** Fertigstellung Ende Dezember 2026 gefährdet, möglich ist **Januar 2027**
- **Offen:** angekündigte Mehrkosten ca. **120.000 €**, noch nicht geprüft
- **Nächster Schritt:** genaue Kostenaufstellung bis **30.11.2026**
- **Entscheidung:** Budgeterhöhung ja oder nein, spätestens bis **05.12.2026**

### Lab 3.1: Übung Outlook

1. **Zusammenfassung:** höchstens fünf Stichpunkte, danach eine Liste mit offenen Entscheidungen, Aufgaben, Personen und Terminen; bestätigt und ungeklärt getrennt.
2. **Antwort:** ein Entwurf, dann z. B. „Formuliere die Antwort kürzer und weniger formell. Die Frist muss erhalten bleiben.“ oder „Schreibe die Antwort in höchstens 80 Wörtern.“
3. **Prüfen:** jeden Termin, Namen und jede Aufgabe im Originalverlauf suchen. Was dort nicht steht, wird gestrichen oder als offen markiert.

### Lab 4.1: Übung Teams

1. **Zusammenfassung:** drei Teile: Vorschläge, Einigkeit, noch nicht entschieden.
2. **Aufgabenliste:** Tabelle Aufgabe | verantwortlich | Termin.
3. **Prüfen:** jede Aufgabe ohne Person oder Termin zeigt „nicht festgelegt“. Fehlt das, den Satz aus Beispiel B als Folgeprompt nachreichen.

| Aufgabe | verantwortlich | Termin |
| ------- | -------------- | ------ |
| Kostenaufstellung anfordern | Projektleitung | 30.11. |
| Budgetvorlage vorbereiten | nicht festgelegt | nicht festgelegt |

### Lab 5.1: Übung Excel

1. **Neue Spalten** (Formeln, wie Copilot sie in der Tabelle `Schulungsdaten` anlegt):

| Spalte | Formel | Bedeutung |
| ------ | ------ | --------- |
| Budgetabweichung in Euro | `=[@[Ist-Kosten]]-[@Budget]` | positiv = über Budget |
| Budgetabweichung in Prozent | `=[@[Budgetabweichung in Euro]]/[@Budget]` | als Prozent formatiert |

2. **Größte Überschreitungen:**

| Rang | Objekt | Abweichung € | Abweichung % | Status |
| ---- | ------ | ------------ | ------------ | ------ |
| 1 | Turmblick | 55.000 € | 22 % | kritisch |
| 2 | Parkresidenz | 45.000 € | 25 % | kritisch |
| 3 | Sonnenbogen | 39.600 € | 18 % | verzögert |

Nach Prozent liegt **Westendhoefe** vorn (39.000 €, **30 %**). Beide Sichten nennen, wenn Copilot nur eine liefert.

3. **Stichprobe Turmblick:** 305.000 € − 250.000 € = 55.000 € · 55.000 € ÷ 250.000 € = 22 %.

Gesamt: Budget 4.085.000 €, Ist-Kosten 4.348.750 €, Überschreitung 263.750 € (ca. 6,5 %). Auffällig: Ringgaerten, Bergpanorama, Seeresidenz und Dammterrassen liegen 6–9 % über Budget und stehen trotzdem auf „planmäßig“.

### Lab 6.1: Übung Word

1. **Statusbericht:** sechs Überschriften (Projektstatus, Termine, Budget, Risiken, erforderliche Entscheidungen, nächste Schritte), nur die Fakten aus den Stichpunkten, keine neuen Zahlen.
2. **Überarbeiteter Text (Beispiel):**

> Das Projekt verläuft insgesamt gut. Verzögerungen bei den Elektroarbeiten verschieben die Fertigstellung voraussichtlich. Zudem sind die Kosten gestiegen. Die Geschäftsführung muss entscheiden, ob das Budget erhöht wird.

3. **Tabelle:**

| Objekt | Budget | geplante Fertigstellung | Status |
| ------ | ------ | ----------------------- | ------ |
| Koch29 | 2,4 Mio. € | Dezember | kritisch |
| Hafen28 | 2,1 Mio. € | Dezember | planmäßig |
| N39 | 3,2 Mio. € | März | verzögert |

### Lab 7.1: Übung PowerPoint

1. **Entwurf:** sechs Folien in dieser Reihenfolge: Ausgangslage · Aktueller Projektstand · Termine · Budgetentwicklung · Risiken · Entscheidungen und nächste Schritte. Jede Zahl stammt aus den Angaben unter dem Prompt.
2. **Gekürzte Folie (Beispiel):** „70 % fertig · Elektro drei Wochen im Verzug · Budget 2,4 Mio. € · ca. 120.000 € Mehrkosten · Entscheidung zur Budgeterhöhung nötig“.
3. **Kritische Fragen (Beispiele):**

| Frage | Antwort aus der Präsentation |
| ----- | ---------------------------- |
| Wie sicher sind die 120.000 € Mehrkosten? | als „erwartet“ angegeben; wie sicher: Information nicht vorhanden |
| Wann ist das Projekt jetzt fertig? | geplant Dezember 2026; neuer Termin: Information nicht vorhanden |
| Was passiert ohne Budgeterhöhung? | Information nicht vorhanden |
| Bis wann muss entschieden werden? | Information nicht vorhanden |

Fragen mit „Information nicht vorhanden“ zeigen, was vor dem Termin noch zu klären ist (z. B. aus dem Übungsblatt: Entscheidung bis 05.12.2026).
