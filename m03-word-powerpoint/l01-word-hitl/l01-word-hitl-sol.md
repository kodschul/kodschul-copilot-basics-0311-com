# Lab 3.1 – Lösung: Vom Stichpunkt zum Bericht – der Mensch entscheidet

Die Lösung zeigt einen möglichen Durchlauf. Copilot formuliert bei jedem Lauf etwas anders; entscheidend sind die Entscheidungen in Schritt 1–3 und der Prüfschritt.

## Aufgabe 1: Kernbotschaft

**Eigene Fassung (ohne Copilot):**

> Das Projekt liegt im Budget, der Verzug schrumpft auf etwa zwei Wochen. Dafür muss die Freigabe des Anforderungskatalogs am 09.10. halten.

**Alternativen von Copilot (Beispiel):**

1. „Das Projekt Hafenmodernisierung liegt im Budget. Der Verzug sinkt von drei bis vier auf etwa zwei Wochen, sofern der Freigabetermin für AP2 am 09.10. gesichert wird."
2. „Budget im Plan, Verzug halbiert – vorausgesetzt, der Lenkungskreis sichert den Freigabetermin am 09.10."

**Gewählt:** Alternative 1, ergänzt um die Bitte an den Lenkungskreis. Grund: Sie nennt Zahl, Bedingung und Termin; Alternative 2 klingt griffig, aber „halbiert" ist ungenau (aus drei bis vier Wochen werden zwei).

## Aufgabe 2: Gliederung mit Rückfragen

**Rückfragen von Copilot und Antworten (Beispiel):**

| Frage von Copilot | Antwort |
| ----------------- | ------- |
| Wer liest den Bericht? | Lenkungskreis der Stadtwerke Nordhafen |
| Soll der Bericht eine Entscheidung anstoßen? | ja: Freigabetermin AP2 am 09.10. absichern |
| Arbeitspakete als Tabelle oder Text? | Tabelle, eine Zeile je AP |
| Risiken mit Gegenmaßnahmen? | nur die drei wichtigsten, kurz |
| Gibt es eine Vorlage? | nein, höchstens eine Seite |

**Vorschlag von Copilot und Kürzung:**

| Vorgeschlagener Abschnitt | Entscheidung |
| ------------------------- | ------------ |
| Kernbotschaft | behalten |
| Entscheidungsbedarf | behalten, direkt nach der Kernbotschaft |
| Projektüberblick und Ziele | gestrichen: bekannt |
| Stand der Arbeitspakete | behalten |
| Budget | behalten |
| Risiken und offene Punkte | behalten |
| Stimmung und Zusammenarbeit | gestrichen: keine Entscheidung |
| Nächste Schritte | behalten |

Ergebnis: sechs Abschnitte. Der Entscheidungsbedarf rückt nach oben, weil der Lenkungskreis genau dafür liest.

## Aufgabe 3: Kernaussagen und ausformulierter Bericht

| Abschnitt | Kernaussage |
| --------- | ----------- |
| Kernbotschaft | Im Budget, Verzug sinkt auf etwa zwei Wochen, wenn der 09.10. hält. |
| Entscheidungsbedarf | Der Lenkungskreis sichert den Freigabetermin AP2 am 09.10. ab. |
| Stand der Arbeitspakete | AP1 fertig, AP2 bei ca. 90 %, AP3 jetzt mit Testsystem validierbar. |
| Budget | 38,9 % verbraucht, unauffällig. |
| Risiken und offene Punkte | Platzt der 09.10., wächst der Verzug wieder auf drei bis vier Wochen. |
| Nächste Schritte | Versand 02.10., Freigabe 09.10., Start Rollout-Planung ab 12.10. |

Rückmeldung von Copilot auf Schritt 3 (Beispiel): „Alle Kernaussagen sind belegt. Hinweis: Der Freigabetermin 09.10. ist laut Stichpunkten noch nicht bestätigt." Daraus folgt der Zusatz „nicht bestätigt" im Bericht.

**Bericht nach Schritt 4 (geprüft, eine Seite):**

> **Statusbericht „Hafenmodernisierung" – Lenkungskreis 06.10.2026**
> Projekt: Hafenmodernisierung – Digitalisierungsphase · Kunde: Stadtwerke Nordhafen · Stand: 02.10.2026 · Verfasser: M. Brandt, Nordwind Consulting
>
> **Kernbotschaft**
> Das Projekt liegt im Budget. Der Verzug durch die ausstehende Freigabe des Anforderungskatalogs schrumpft von drei bis vier auf etwa zwei Wochen – vorausgesetzt, der Freigabetermin am 09.10. hält. Der Lenkungskreis wird gebeten, diesen Termin abzusichern.
>
> **Entscheidungsbedarf**
> - Absicherung des Freigabetermins für den Anforderungskatalog (AP2) am 09.10.2026 durch den Fachbereich Betrieb.
>
> **Stand der Arbeitspakete**
>
> | AP | Bezeichnung | Stand | Bemerkung |
> | -- | ----------- | ----- | --------- |
> | AP1 | Ist-Analyse Betriebsprozesse | abgeschlossen | seit Ende August |
> | AP2 | Anforderungskatalog Leitstand | ca. 90 % | ergänzte Fassung mit Störungsmanagement am 02.10.; Freigabe angepeilt 09.10. (nicht bestätigt) |
> | AP3 | Schnittstellenkonzept Sensorik | ca. 35 % | Testsystem seit 01.10. verfügbar, Validierung beginnt |
> | AP4 | Rollout-Planung | nicht begonnen | Start frühestens ab 12.10. |
> | AP5 | Schulungskonzept | nicht begonnen | planmäßig |
>
> **Budget**
> 184.000 € Auftragsvolumen, davon 71.500 € verbraucht (38,9 %, Stand 23.09.2026). Der Verbrauch entspricht dem Projektfortschritt.
>
> **Risiken und offene Punkte**
> - Freigabe AP2: Verschiebt sich der Termin am 09.10., wächst der Verzug wieder auf drei bis vier Wochen.
> - Datenmigration: IT technisch, Betrieb fachlich zuständig; die Liste der zu migrierenden Daten vom Betrieb ist offen, eine Frist fehlt.
> - Fachinterviews: Zwei Interviews (Leitstand, Instandhaltung) stehen aus; Terminvorschläge sind in Vorbereitung.
>
> **Nächste Schritte**
> - 02.10.: Versand der ergänzten Fassung des Anforderungskatalogs (T. Okonkwo)
> - 09.10.: Freigabetermin AP2 im Fachbereich Betrieb (K. Sievers)
> - ab 12.10.: Start der Rollout-Planung (Nordwind)
> - 15.10.: nächster Jour fixe

Die Fassung entspricht inhaltlich `nordwind-statusbericht-referenz.docx`, dem Fallback für Lab 3.2.

Typische Abweichungen im eigenen Ergebnis und ihre Bewertung:

| Abweichung | Bewertung |
| ---------- | --------- |
| Abschnitt „Stimmung im Projekt" ist geblieben | zulässig, wenn bewusst entschieden; kostet Platz auf der einen Seite |
| Testsystem steht als „beantragt" | falsch: Stand 02.10. ist der Zugang da (Stichpunkte); die ältere Projektnotiz wurde verwendet |
| Namen bei den nächsten Schritten fehlen | zulässig: Die Stichpunkte nennen keine Verantwortlichen. Die Namen in der Musterlösung stammen aus dem Jour-fixe-Transkript (`nordwind-meeting-transkript.docx`, Lab 2.2) und wurden von Hand ergänzt |
| Copilot ergänzt Namen ohne Quelle | Copilot hat geraten; Namen streichen oder gegen das Transkript prüfen |

## Aufgabe 4: Prüfschritt

| Geprüfte Angabe | Bericht | `nordwind-projektnotizen.docx` | Ergebnis |
| --------------- | ------- | ------------------------------ | -------- |
| Budget verbraucht | 71.500 € (38,9 %) | 71.500 € (38,9 %), Berichtsstand 23.09.2026 | stimmt |
| Fortschritt AP2 | ca. 90 % | 70 %, Stand 23.09.2026 | weicht ab |

Bewertung der Abweichung: Die Projektnotizen haben Stand 23.09., die Stichpunkte Stand 02.10. Seitdem kam die Ergänzung Störungsmanagement hinzu. Der Bericht verwendet die neuere Angabe und nennt den Stand.

**Beispiel für die Notiz bzw. den optionalen Kommentar:** „Geprüft: AP2 ca. 90 % laut Stichpunkten (02.10.2026); Projektnotizen nennen 70 % mit Stand 23.09.2026 – neuere Angabe verwendet."

## Erweiterung: Fassung für die Geschäftsführung

> **Statusbericht Hafenmodernisierung – Kurzfassung Geschäftsführung (Stand 02.10.2026)**
>
> **Entscheidungsbedarf:** Der Freigabetermin für den Anforderungskatalog (AP2) am 09.10.2026 muss halten; der Lenkungskreis wird am 06.10. um Absicherung gebeten.
>
> **Kernbotschaft:** Das Projekt liegt im Budget, der Verzug sinkt von drei bis vier auf etwa zwei Wochen, wenn der 09.10. hält.
>
> **Budget:** 71.500 € von 184.000 € verbraucht (38,9 %, Stand 23.09.2026), passend zum Fortschritt.
>
> **Größtes Risiko:** Platzt der Freigabetermin, wächst der Verzug wieder auf drei bis vier Wochen.

Weggefallen sind Arbeitspaket-Tabelle, Datenmigration, Fachinterviews und nächste Schritte. Das ist bewusst: Die Geschäftsführung braucht die Entscheidung und das Risiko, nicht den Arbeitsstand.
