# Lab 3.2 – Lösung: Aus dem Bericht eine Präsentation

Die Lösung beruht auf `nordwind-statusbericht-referenz.docx`. Ein eigener Bericht aus Lab 3.1 führt zu ähnlichen, aber nicht identischen Folien.

## Aufgabe 1: Präsentation erstellen

Mögliche Rückfragen von Copilot und Antworten:

| Rückfrage | Antwort |
| --------- | ------- |
| Wer ist das Publikum? | Lenkungskreis der Stadtwerke Nordhafen |
| Welcher Stil oder welche Vorlage? | Unternehmensvorlage, falls vorhanden; sonst schlicht |
| Sollen Bilder eingefügt werden? | nein |

Erwartete Folien (Titel und Kernaussage):

| Folie | Titel | Kernaussage | Inhalt (höchstens vier Stichpunkte) |
| ----- | ----- | ----------- | ----------------------------------- |
| 1 | Kernbotschaft | Im Budget, Verzug sinkt auf etwa zwei Wochen, wenn der 09.10. hält. | Projekt im Budget · Verzug von drei bis vier auf etwa zwei Wochen · Bedingung: Freigabe AP2 am 09.10. · Bitte um Absicherung |
| 2 | Entscheidungsbedarf | Der Lenkungskreis sichert den Freigabetermin AP2 am 09.10.2026 ab. | Freigabe Anforderungskatalog (AP2) durch Fachbereich Betrieb · Termin 09.10.2026, noch nicht bestätigt |
| 3 | Stand der Arbeitspakete | AP1 fertig, AP2 bei ca. 90 %, AP3 jetzt mit Testsystem validierbar. | AP1 abgeschlossen · AP2 ca. 90 %, ergänzte Fassung am 02.10. · AP3 ca. 35 %, Testsystem seit 01.10. · AP4/AP5 nicht begonnen, AP4 ab 12.10. |
| 4 | Budget | 38,9 % verbraucht, passend zum Fortschritt. | 184.000 € Auftragsvolumen · 71.500 € verbraucht (38,9 %, Stand 23.09.2026) · unauffällig |
| 5 | Risiken und nächste Schritte | Platzt der 09.10., wächst der Verzug wieder auf drei bis vier Wochen. | Risiko Freigabe AP2 · Datenmigration: Datenliste vom Betrieb offen · zwei Fachinterviews offen · 02.10. Versand, 09.10. Freigabe, ab 12.10. Rollout-Planung, 15.10. Jour fixe |

## Aufgabe 2: Prüfung je Folie (Beispiel)

| Folie | Ergebnis | Grund |
| ----- | -------- | ----- |
| 1 | trägt | Bedingung 09.10. ist enthalten |
| 2 | trägt nicht | „nicht bestätigt" fehlt; die Folie klingt, als stehe der Termin fest |
| 3 | trägt | fünf Arbeitspakete in vier Stichpunkten zusammengefasst |
| 4 | trägt | Stand 23.09.2026 genannt |
| 5 | trägt nicht | sechs Stichpunkte, Risiko und Termine vermischt |

## Aufgabe 3: Folie überarbeiten

Gewählt: Folie 2, weil eine fehlende Einschränkung die Entscheidung verfälscht.

```text
Überarbeite nur Folie 2. Ihre Kernaussage lautet: „Der Lenkungskreis sichert den Freigabetermin AP2 am 09.10.2026 ab." Richte die Folie auf genau diese Aussage aus, höchstens drei Stichpunkte, keine neuen Zahlen. Verschiebe Details in die Sprechernotiz.
```

Ergebnis (Beispiel):

- **Bitte an den Lenkungskreis:** Freigabetermin AP2 am 09.10.2026 absichern
- Termin ist angepeilt, aber noch nicht bestätigt
- Ohne Freigabe wächst der Verzug wieder auf drei bis vier Wochen

Sprechernotiz: „Die Freigabe des Anforderungskatalogs steht seit 11.09. aus. Der Fachbereich hatte am 29.09. zwei Rückfragen; die ergänzte Fassung geht am 02.10. raus."

Bewertung: Die Sprechernotiz enthält Daten aus den Stichpunkten, nicht aus dem Referenzbericht (11.09., 29.09.). Sie sind korrekt, aber nur belegbar, wenn die Stichpunkte als Quelle mitgenannt werden; sonst streichen.

## Aufgabe 4: Zahl und Termin prüfen

| Angabe | Folie | Bericht | Ergebnis |
| ------ | ----- | ------- | -------- |
| Budget verbraucht | 71.500 € (38,9 %) | 71.500 € (38,9 %, Stand 23.09.2026) | stimmt |
| Freigabetermin AP2 | 09.10.2026 | 09.10.2026, nicht bestätigt | stimmt nach Überarbeitung von Folie 2 |

Häufige Abweichungen: „39 %" statt „38,9 %" (gerundet, Stand fehlt) und „Freigabe am 09.10." ohne „nicht bestätigt". Beides wird von Hand korrigiert.

## Erweiterung: Zusammenfassung als Gegenprobe

Zusammenfassung von Copilot (Beispiel): „Das Projekt Hafenmodernisierung liegt im Budget und der Verzug sinkt auf etwa zwei Wochen. Voraussetzung ist die Freigabe des Anforderungskatalogs am 09.10., die noch nicht bestätigt ist. Weitere offene Punkte sind die Datenmigration und zwei Fachinterviews."

Bewertung: Die ersten zwei Sätze entsprechen der Kernbotschaft; die Präsentation trägt. Nennt die Zusammenfassung dagegen zuerst Datenmigration oder Fachinterviews, ist Folie 5 zu stark gewichtet und wird gekürzt.

Abweichungstabelle der Profi-Variante ohne Befund: „Keine Abweichungen zwischen Folien und Bericht gefunden." Diese Aussage von Copilot ersetzt nicht die eigene Stichprobe aus Aufgabe 4.
