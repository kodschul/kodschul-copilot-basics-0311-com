# Lab 2.2 – Lösung: Besprechungen nachbereiten und Aufgaben ableiten

## Aufgaben

### 1. „Was wurde bisher besprochen?"

Das Ergebnis hängt von der jeweiligen Besprechung ab. Typisch ist eine Liste der Themen in zeitlicher Reihenfolge mit Sprechernamen und nummerierten Verweisen auf das Transkript. Läuft keine Transkription, antwortet Copilot nur, solange die Besprechung läuft (Einstellung „Only during the meeting"), danach nicht mehr.

### 2. Prompt-Karte 3 (Basis)

Typisches erstes Ergebnis: sechs bis acht Zeilen. Die ausdrücklichen Zusagen sind meist richtig; häufige Fehler sind in Aufgabe 3 beschrieben.

### 3. Geprüfte Aufgabenliste

| # | Aufgabe | Verantwortlich | Frist | Status | Uhrzeit |
| - | ------- | -------------- | ----- | ------ | ------- |
| 1 | Ergänzte Fassung des Anforderungskatalogs mit Störungsmanagement schicken | T. Okonkwo | Freitag, 02.10.2026 | zugesagt | 10:02 |
| 2 | Freigabetermin im Fachbereich Betrieb am 09.10.2026 anfragen | K. Sievers | 09.10.2026 (Termin angestrebt) | zugesagt, Ergebnis offen („Ich versuche …") | 10:04 |
| 3 | Zugangsdaten für das Testsystem per Mail an T. Okonkwo schicken | R. Lammers | 01.10.2026 („heute noch") | zugesagt | 10:08 |
| 4 | Testsystemzugang testen | T. Okonkwo | 01.10.2026 nachmittags | zugesagt | 10:09 |
| 5 | Drei Terminvorschläge für die Fachinterviews Leitstand und Instandhaltung an K. Sievers schicken | M. Brandt | offen | zugesagt | 10:22 |
| 6 | Liste der Altdaten, die migriert werden müssen | K. Sievers (Betrieb) | gewünscht bis nächster Jour fixe, 15.10.2026 | nur angedeutet („mal sehen, das ist knapp") | 10:15–10:17 |
| 7 | Neue Termine für die ausgefallenen Fachinterviews finden | K. Sievers | offen | nur angedeutet („müsste man mal"); von M. Brandt mit Nr. 5 übernommen | 10:21 |
| 8 | Rollout-Planung starten | Nordwind (M. Brandt) | Woche ab 12.10.2026 | nur angedeutet, bedingt: nur wenn die Freigabe am 09.10. kommt (Profi-Variante: „bedingt") | 10:05 |

**Termin:** nächster Jour fixe am 15.10.2026 (10:33).
**Keine Aufgabe, sondern Klärung:** Datenmigration macht technisch die IT, der Betrieb sagt, welche Altdaten mitmüssen (10:13).

Häufige Fehler im Copilot-Ergebnis und Korrektur:

| Fehler | Korrektur |
| ------ | --------- |
| Nr. 6 als „zugesagt, bis 15.10." | Sievers sagt nur „Wir schauen uns das mal an" und „mal sehen, das ist knapp": nur angedeutet, Frist ist ein Wunsch von M. Brandt |
| Nr. 2 als „Freigabe am 09.10." | zugesagt ist nur der Versuch, einen Termin zu bekommen, nicht die Freigabe |
| Nr. 7 fehlt oder steht bei K. Sievers als Zusage | Sievers deutet nur an; die Zusage stammt von M. Brandt (Nr. 5) |
| Nr. 8 als feste Aufgabe ohne Bedingung | Start ab 12.10. gilt nur bei Freigabe am 09.10. |
| Nr. 3 fehlt | Lammers' Zusage steht in einem Nebensatz („Die Zugangsdaten gehen heute noch per Mail …") und wird leicht übersehen |

### 4. Von Hand ergänzt

Welche Zeilen ergänzt werden, hängt vom Copilot-Ergebnis ab. Am häufigsten fehlen Nr. 3 (Zugangsdaten), Nr. 7 (angedeutete Interviewtermine) und Nr. 8 (bedingter Start der Rollout-Planung). Jede ergänzte Zeile trägt den Vermerk „von Hand ergänzt" und eine Uhrzeit aus dem Transkript.

## Checkpoint

- Acht Zeilen, davon fünf zugesagt (eine mit offenem Ergebnis) und drei nur angedeutet (eine davon bedingt).
- Keine erfundene Frist; „offen" bei Nr. 5 und Nr. 7.
- Nächster Jour fixe: 15.10.2026.

## Erweiterung

Abgleich der Zusammenfassung von M. Brandt um 10:33 mit dem Transkript:

| Aussage um 10:33 | Transkript | Bewertung |
| ---------------- | ---------- | --------- |
| „Katalog kommt bis Freitag" | Okonkwo, 10:02: bis 02.10. | stimmt |
| „Freigabe möglichst am 09.10." | Sievers, 10:04: „Ich versuche, einen Termin am 09.10. zu bekommen." | stimmt, „möglichst" trifft es |
| „Testsystem läuft" | Lammers, 10:08: Zugang eingerichtet, Test durch Okonkwo steht noch aus | zu stark: eingerichtet, aber noch nicht getestet |
| „Migration ist geklärt" | 10:13–10:17: Zuständigkeit geklärt, Liste der Altdaten offen, „mal sehen" | zu stark: nur die Zuständigkeit ist geklärt |
| fehlt | Brandt, 10:22: drei Terminvorschläge für Fachinterviews | eigene Zusage nicht erwähnt |

Beispiel für die Teams-Nachricht:

> Hallo zusammen, danke für den Jour fixe. Zwei Punkte sind noch offen:
> 1. Herr Sievers, schaffen Sie die Liste der Altdaten für die Migration bis zum Jour fixe am 15.10., oder welches Datum ist realistisch?
> 2. Rollout-Planung: Wir starten in der Woche ab 12.10., sobald die Freigabe am 09.10. bestätigt ist. Bitte kurze Rückmeldung, sobald der Termin steht.
> Die drei Terminvorschläge für die Fachinterviews kommen separat von mir.
> Viele Grüße, M. Brandt

Versandfähig nach Prüfung: ja, wenn jede Frage einer Zeile der Aufgabenliste entspricht und kein neues Datum hinzugekommen ist.

## Fallback

Mit der Registerkarte Recap einer vergangenen Besprechung liefert Aufgabe 1 dieselbe Art von Antwort. Die Aufgaben 2–4 und ihre Lösung bleiben unverändert.
