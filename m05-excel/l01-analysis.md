# Lab 5.1: Excel – Budgetabweichungen berechnen und auswerten

**Leitfragen:**

<details>
<summary>Welche Fragen an eine Kostentabelle stellen sich jeden Monat wieder?</summary>

Wo liegen wir über Budget, um wie viel, und welche Objekte sind kritisch?

</details>

<details>
<summary>Ist die größte Überschreitung in Euro auch die größte in Prozent?</summary>

Nicht unbedingt. Ein großes Objekt überschreitet in Euro schnell viel, ein kleines in Prozent. Beide Sichten zählen.

</details>

<details>
<summary>Woran ist erkennbar, ob eine berechnete Zahl stimmt?</summary>

An einer Stichprobe: eine Zeile selbst nachrechnen.

</details>

![Copilot in Excel mit den Modi Allow editing, Plan und Chat only](https://support.microsoft.com/en-us/excel/media/copilot-in-excel-modes.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/excel/media/copilot-in-excel-modes.png), abgerufen am 25.11.2026._

Copilot in Excel ergänzt Spalten mit Formeln, erklärt sie, findet Auffälligkeiten und erstellt Diagramme.

| Voraussetzung | Warum |
| ------------- | ----- |
| Datei liegt im OneDrive oder in SharePoint | sonst ist Copilot in Excel nicht aktiv |
| Daten als Tabelle mit eindeutigen Spaltenüberschriften | Copilot erkennt so, was jede Spalte bedeutet |
| einheitliche Datentypen, keine verbundenen Zellen | sonst rechnet Copilot falsch oder gar nicht |

Die Übungsdatei erfüllt alles bereits (Tabelle `Schulungsdaten`).

## Beispiel A · Abweichungen ermitteln

```text
Ergänze eine Spalte „Budgetabweichung in Euro“. Berechne die Ist-Kosten abzüglich des Budgets.
```

Danach:

```text
Ergänze eine weitere Spalte „Budgetabweichung in Prozent“ und erkläre mir die verwendete Formel.
```

## Beispiel B · Auffälligkeiten erkennen

```text
Analysiere die Tabelle. Welche drei Objekte weisen die größten Budgetüberschreitungen auf? Nenne die Abweichung in Euro und Prozent und beschreibe mögliche Auffälligkeiten in den Daten. Erfinde keine Ursachen, die nicht aus der Tabelle hervorgehen.
```

## Beispiel C · Managementauswertung

```text
Erstelle eine kurze Managementzusammenfassung. Nenne die Gesamtbudgets, die gesamten Ist-Kosten, die größten Abweichungen und alle Objekte mit dem Status „kritisch“. Verwende maximal acht Stichpunkte.
```

## Beispiel D · Visualisierung

```text
Erstelle ein geeignetes Diagramm, das Budget und Ist-Kosten je Objekt gegenüberstellt.
```

Zum Diagramm besprechen: Passt der Diagrammtyp? Sind die Beschriftungen verständlich? Nach Betrag oder Abweichung sortieren? Taugt es für die Geschäftsführung?

## Übung Excel

**Datei:** `Projektkosten – Übung.xlsx` (im eigenen OneDrive)

1. Lass die Spalten zur Budgetabweichung aus Beispiel A ergänzen.
2. Lass die drei Objekte mit den größten Überschreitungen ermitteln.
3. Rechne ein Ergebnis von Copilot stichprobenartig selbst nach.

| Typischer Fehler | Lösung |
| ---------------- | ------ |
| Copilot ist ausgegraut | Datei aus dem OneDrive öffnen, nicht vom Desktop |
| Prozentspalte zeigt 0,22 statt 22 % | Zelle als Prozent formatieren oder Copilot darum bitten |

## Musterergebnis

<details>
<summary>Musterergebnis anzeigen</summary>

Copilot formuliert jedes Mal etwas anders; entscheidend ist, was enthalten ist.

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

</details>
