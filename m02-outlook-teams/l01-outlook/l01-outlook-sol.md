# Lab 2.1 – Lösung: E-Mails zusammenfassen und beantworten

## Aufgaben

### 1. Zusammenfassung des Verlaufs

Beispielergebnis (Wortlaut variiert):

- **09.09., M. Brandt:** schickt den Entwurf des Anforderungskatalogs (AP2, rund 70 %); Störungsmanagement fehlt noch und wird bis zum nächsten Jour fixe ergänzt; bittet um einen Freigabetermin.
- **10.09., K. Sievers:** Entwurf angekommen, ein fester Termin ist noch nicht möglich.
- **16.09. / 17.09., M. Brandt und R. Lammers:** Antrag Testsystemzugang Sensorik ist gestellt; die Prüfung dauert laut IT fünf bis zehn Arbeitstage. Brandt schlägt für die Freigabe einen 30-Minuten-Termin am 24. oder 25.09. vor.
- **22.09., M. Brandt:** hakt nach; ohne Freigabe verschiebt sich die Rollout-Planung um drei bis vier Wochen.
- **29.09., K. Sievers (offen):** zwei Rückfragen des Fachbereichs: (1) Warum fehlt das Störungsmanagement? (2) Wie lange dauert die Rollout-Planung, wenn die Freigabe erst Mitte Oktober kommt? Freigabe vor dem 15.10. sei realistisch, wenn die Fragen geklärt sind.

### 2. Zero-Shot und Few-Shot im Vergleich

Typischer Zero-Shot-Entwurf (gekürzt):

> Sehr geehrter Herr Sievers,
> vielen Dank für Ihre ausführliche Rückmeldung und die konstruktiven Fragen des Fachbereichs, über die wir uns sehr freuen. Gerne nehmen wir dazu Stellung. Das Störungsmanagement war bewusst noch nicht Teil des Entwurfs … Die Rollout-Planung nimmt erfahrungsgemäß etwa sechs Wochen in Anspruch …

Few-Shot-Entwurf mit Prompt-Karte 2 (Basis):

> Hallo Herr Sievers,
>
> danke für Ihre Rückmeldung und die Fragen des Fachbereichs. Zu Ihren beiden Fragen:
>
> 1. Das Störungsmanagement war im Entwurf vom 09.09. noch offen. Wir ergänzen es wie angekündigt bis zum nächsten Jour fixe; danach liegt der Katalog vollständig zur Freigabe vor.
> 2. Die Rollout-Planung kann erst nach der Freigabe beginnen. Kommt die Freigabe Mitte Oktober, verschiebt sich die Rollout-Planung wie in meiner Mail vom 22.09. beschrieben um drei bis vier Wochen. Die Dauer der Rollout-Planung selbst: [ergänzen].
>
> Sobald der Fachbereich einen Termin hat, plane ich die nächsten Schritte mit Ihnen.
>
> Viele Grüße
> M. Brandt

Beispielsatz zum Unterschied: „Zero-Shot war förmlich, lang und hat eine Dauer von sechs Wochen erfunden; Few-Shot hat Länge, Anrede und die nummerierte Gliederung der Beispielmail übernommen und die fehlende Dauer als Platzhalter markiert."

### 3. Prüfung

| Prüfpunkt | Ergebnis | Beleg |
| --------- | -------- | ----- |
| Rückfrage 1 beantwortet | ja | Mail vom 09.09.: „Bereich Störungsmanagement, den wir bis zum nächsten Jour fixe ergänzen" |
| Rückfrage 2 beantwortet | teilweise; die Dauer steht nicht im Verlauf | Mail vom 22.09.: Verschiebung um drei bis vier Wochen; Dauer als `[ergänzen]` |
| Abgleich mit `nordwind-projektnotizen.docx` | Verschiebung stimmt | Risiko R1: „Rollout-Planung verschiebt sich um 3–4 Wochen" |
| Alternativer Abgleich | Testsystemzugang stimmt | Notizen: „beantragt, noch nicht erteilt"; Antrag am 16.09.2026 |
| Kein fremdes Datum | geprüft | Ein Datum wie „09.10." oder „12.10." stammt nicht aus dem Verlauf, sondern aus einer späteren Datei (Work IQ) oder ist erfunden; streichen |
| Nichts aus der Beispielmail | geprüft | kein „Frau Kramer", kein „bis Freitag", keine „zwei Wochen" |

Der Platzhalter `[ergänzen]` ist richtig: Die Dauer der Rollout-Planung kennt nur die Projektleitung. Sie entscheidet vor dem Senden.

### 4. Ungesendete Mail in Outlook

- Neue Mail, Betreff „AW: Entwurf Anforderungskatalog Leitstand (AP2)", Feld „An" leer, Text aus Aufgabe 2 nach der Prüfung.
- Die Mail bleibt als Entwurf im Ordner „Entwürfe"; Senden ist nicht Teil der Übung.

## Checkpoint

- Beide Rückfragen beantwortet, jede Angabe im Verlauf belegt, die unbekannte Dauer als `[ergänzen]` markiert.
- Keine Inhalte aus der Beispielmail im Entwurf.

## Erweiterung

### 1. Coaching

Typische Vorschläge von „Coaching by Copilot":

| Vorschlag | Entscheidung |
| --------- | ------------ |
| Bitte um konkreten Freigabetermin ergänzen | übernehmen; passt zum Ziel „Freigabe vor dem 15.10." |
| Ton wärmer formulieren | verwerfen; der Entwurf ist bereits freundlich und knapp |
| Platzhalter `[ergänzen]` füllen | nicht durch Copilot; die Dauer liefert die Projektleitung |

### 2. Interne Kurzfassung (Profi-Variante)

- **Kunde fragt:** warum das Störungsmanagement fehlt und wie lange die Rollout-Planung bei Freigabe Mitte Oktober dauert.
- **Entwurf antwortet:** Ergänzung bis zum nächsten Jour fixe; Verschiebung um drei bis vier Wochen wie am 22.09. angekündigt.
- **Projektleitung entscheidet:** Dauer der Rollout-Planung eintragen und ob ein konkreter Freigabetermin vorgeschlagen wird.

Unterschied: intern direkt, ohne Anrede und Höflichkeit, mit der offenen Entscheidung zuerst; der Kundenentwurf beantwortet Fragen und nennt den nächsten Schritt.

## Fallback

In Copilot Chat entstehen dieselben Entwürfe. Statt „Coaching by Copilot" liefert der Chat eine Rückmeldungsliste; Änderungen werden von Hand in die Mail übernommen.
