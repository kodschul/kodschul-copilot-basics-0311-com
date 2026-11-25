# Teil 1 · Copilot verstehen und gut fragen

Modul 1 und 2: was Copilot ist, wo es sitzt und wie ein guter Auftrag aussieht.

| Lab | Thema |
| --- | ----- |
| 1.1 | Was ist Microsoft Copilot? |
| 1.2 | Copilot Chat und Copilot in den Apps |
| 2.1 | Die Prompt-Formel |
| 2.2 | Übung Koch29: ein Prompt für die Geschäftsführung |
| 2.3 | Prompt-Techniken und Folgeprompts |

## Lab 1.1: Was ist Microsoft Copilot?

**Leitfragen:**

<details>
<summary>Welche Aufgaben im Arbeitsalltag kosten viel Zeit, ohne viel Denkarbeit zu brauchen?</summary>

Lange Mails lesen, Protokolle schreiben, Berichte beginnen, Zahlen sortieren. Genau dort hilft Copilot.

</details>

<details>
<summary>Würde jemand einen Text unterschreiben, den ein neuer Kollege am ersten Tag geschrieben hat, ohne ihn zu lesen?</summary>

Nein. Mit Copilot ist es genauso: Der Text ist ein Entwurf, die Verantwortung bleibt bei dem Menschen, der ihn verwendet.

</details>

![Microsoft 365 Copilot App mit Chat, Agents und Notebooks in der linken Leiste](https://support.microsoft.com/en-us/microsoft-365-copilot/media/one-copilot-hero.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/microsoft-365-copilot/media/one-copilot-hero.png), abgerufen am 25.11.2026._

**Copilot** ist ein digitaler Assistent in Microsoft 365. Er fasst zusammen, formuliert Texte, wertet Zahlen aus und bereitet Präsentationen vor.

- arbeitet direkt in Outlook, Teams, Word, Excel und PowerPoint
- sieht nur, worauf die Person selbst Zugriff hat
- liefert Entwürfe, keine automatisch richtigen Ergebnisse

### Drei Botschaften zu Copilot

| Botschaft | Bedeutung |
| --------- | --------- |
| Copilot unterstützt, entscheidet aber nicht | der Entwurf kommt von Copilot, die fachliche Verantwortung bleibt beim Menschen |
| Copilot braucht klare Anweisungen | je genauer der Auftrag, desto besser das Ergebnis |
| Ergebnisse müssen geprüft werden | besonders Zahlen, Verträge, Fristen, Namen und vertrauliche Inhalte |

### Copilot Chat und Vollversion

| | Copilot Chat | Microsoft 365 Copilot (Vollversion) |
| --- | --- | --- |
| Lizenz | in Microsoft 365 enthalten | Zusatzlizenz |
| Wissen aus dem Internet | ja | ja |
| hochgeladene Dateien, geöffnetes Dokument | ja | ja |
| eigene Mails, Chats, Besprechungen, Dateien | nein | ja |
| Copilot in Outlook, Teams, Word, Excel, PowerPoint | eingeschränkt | voller Umfang |

_Stand: 25.11.2026, [Microsoft Support](https://support.microsoft.com/en-us/microsoft-365-copilot/how-copilot-chat-works-in-microsoft-365-apps). Welche Version aktiv ist, zeigt das eigene Konto._

> **Merksatz:** Copilot nimmt uns Arbeit ab, aber nicht die Verantwortung.

## Lab 1.2: Copilot Chat und Copilot in den Apps

**Leitfragen:**

<details>
<summary>Woher soll ein Assistent wissen, was im eigenen Postfach steht?</summary>

Nur, wenn er darauf zugreifen darf. In der Vollversion liest Copilot die eigenen Mails und Dateien mit, sobald Work IQ eingeschaltet ist.

</details>

<details>
<summary>Ist es ein Unterschied, ob eine Frage ans Internet geht oder an die eigenen Unterlagen?</summary>

Ja. Das Internet kennt allgemeines Wissen, die eigenen Unterlagen kennen das eigene Projekt. Work IQ schaltet zwischen beidem um.

</details>

### Wo Copilot in den Apps sitzt

| App | Copilot findet sich … |
| --- | --------------------- |
| Outlook | über der geöffneten Mail und beim Schreiben einer neuen Mail |
| Teams | in Chats, Kanälen und Besprechungen (Schaltfläche Copilot) |
| Word, Excel, PowerPoint | Schaltfläche Copilot im Menüband öffnet den Bereich rechts |
| Copilot-App | als eigene App, im Browser und in Teams |

![Word mit geöffnetem Copilot-Bereich rechts neben dem Dokument](https://support.microsoft.com/en-us/microsoft-365-copilot/media/copilot-word-chat.png)

_Quelle: Microsoft Support (https://support.microsoft.com/en-us/microsoft-365-copilot/media/copilot-word-chat.png), abgerufen am 25.11.2026._

### Bereiche der Copilot-App

| Bereich | Wofür |
| ------- | ----- |
| Neuer Chat | ein neues Gespräch ohne alten Verlauf beginnen |
| Work IQ | Schalter: an = eigene Mails, Chats, Dateien einbeziehen · aus = nur Internet und Hochgeladenes |
| **+** (Hochladen) | Datei oder Bild an die Frage anhängen |
| Suche | eigene Dateien, Mails und Besprechungen finden |
| Bibliothek | erstellte Inhalte wie Bilder und Seiten wiederfinden |
| Notebooks | Notizen und Dateien zu einem Thema sammeln und dazu fragen |
| Agents | spezialisierte Helfer mit festem Auftrag und eigenen Dokumenten |
| Create | Bilder, Grafiken und Entwürfe erstellen |

- **Work IQ** ersetzt die früheren Registerkarten „Arbeit“ und „Web“ ([Microsoft Support](https://support.microsoft.com/en-US/Microsoft-365-Copilot/what-information-does-copilot-use-to-answer-my-prompt), Stand 25.11.2026).
- Ein **Agent** ist ein Copilot mit festem Auftrag, z. B. Fragen zu einem bestimmten Dokument beantworten.
- **Einstellungen** (Profilbild → Einstellungen, Klickpfad im eigenen Konto prüfen): Personalisierung, Erinnerungen (Memory) und eigene Anweisungen an Copilot, soweit im Unternehmen freigegeben.

Bereiche und Namen ändern sich laufend; im eigenen Konto prüfen.

## Lab 2.1: Die Prompt-Formel

Ein **Prompt** ist der Auftrag an Copilot, als Text eingetippt.

**Leitfragen:**

<details>
<summary>Was braucht eine neue Kollegin, um einen Bericht ohne Rückfrage zu schreiben?</summary>

Worum es geht, für wen, welche Unterlagen sie nutzen soll und wie das Ergebnis aussehen soll. Copilot braucht dieselben Angaben.

</details>

<details>
<summary>Was kommt heraus, wenn ein Auftrag nur aus vier Wörtern besteht?</summary>

Etwas Allgemeines. Wer nichts vorgibt, bekommt einen Durchschnittstext.

</details>

### Vier Fragen für jeden Prompt

| Teil | Frage | Beispiel |
| ---- | ----- | -------- |
| **Aufgabe** | Was soll Copilot machen? | „Erstelle einen Projektstatusbericht zum Projekt Lindenhof.“ |
| **Kontext** | Für wen und wofür? | „Für das Projektteam.“ |
| **Quelle** | Welche Informationen soll Copilot nutzen? | „Die Protokolle der letzten drei Baubesprechungen.“ |
| **Ergebnis** | Wie soll die Antwort aussehen? | „Drei kurze Abschnitte mit höchstens fünf Stichpunkten.“ |

Ein Prompt muss nicht lang sein. Er muss klar und konkret sein.

### Vorher-Nachher: Projektbericht Lindenhof

Schwach:

```text
Erstelle einen Projektbericht.
```

Es fehlt: welches Projekt, für wen, welche Unterlagen, was wichtig ist, welcher Aufbau, welche Länge.

Stark:

```text
Erstelle einen Projektstatusbericht zum Projekt Lindenhof für das Projektteam. Verwende die Protokolle der letzten drei Baubesprechungen als Grundlage. Konzentriere dich auf erledigte Arbeiten, offene Aufgaben und die nächsten Termine. Gliedere den Bericht in drei kurze Abschnitte mit jeweils höchstens fünf Stichpunkten. Kennzeichne Punkte, zu denen Informationen fehlen. Erfinde keine fehlenden Angaben.
```

Die letzten zwei Sätze sind Qualitätsregeln: Lücken werden sichtbar statt erfunden.

> **Merksatz:** Aufgabe + Kontext + Quelle + gewünschtes Ergebnis.

## Lab 2.2: Übung Koch29: ein Prompt für die Geschäftsführung

**Leitfragen:**

<details>
<summary>Was will eine Geschäftsführung über ein Projekt in zwei Minuten wissen?</summary>

Stand, Geld, Termine, Risiken und was sie entscheiden muss.

</details>

<details>
<summary>Welche Angaben in einem Projektbericht sind sicher, welche noch offen?</summary>

Sicher ist, was gemessen oder beschlossen ist. Offen sind Schätzungen, angekündigte Kosten und mögliche Verschiebungen.

</details>

### Übung Koch29

**Datei:** `Übungsblatt Koch29 für Promt und Outlook.docx` ([project/](project/))

1. Öffne das Übungsblatt und lies die Ausgangsinformationen zum Projekt Koch29.
2. Formuliere einen möglichst guten Prompt für Copilot, um die Geschäftsführung über den aktuellen Stand von Koch29 zu informieren. Denke an Aufgabe + Kontext + Quelle + gewünschtes Ergebnis. Arbeite allein oder zu zweit (ca. 5–6 Minuten).
3. Prüfe den eigenen Prompt mit diesen Fragen:

| Prüffrage | ✓ |
| --------- | - |
| Ist die Aufgabe klar? | |
| Kennt Copilot Zielgruppe und Zweck? | |
| Ist die Quelle eindeutig? | |
| Ist klar, wie das Ergebnis aussehen soll? | |
| Könnte Copilot etwas falsch verstehen? | |

Musterlösung: [Teil 3, Lab 2.2](03-spickzettel-und-loesungen.md#lab-22-übung-koch29).

## Lab 2.3: Prompt-Techniken und Folgeprompts

**Leitfragen:**

<details>
<summary>Wird ein Text besser, wenn er neu geschrieben oder wenn er überarbeitet wird?</summary>

Meist durch Überarbeiten. Bei Copilot heißt das: im selben Chat nachschärfen statt neu beginnen.

</details>

<details>
<summary>Was soll ein Assistent ausdrücklich nicht tun?</summary>

Angaben erfinden, Fakten ändern, Entscheidungen treffen. Das gehört als Grenze in den Prompt.

</details>

| Technik | Beispiel |
| ------- | -------- |
| 🎯 Zielgruppe nennen | „für die Geschäftsführung“ |
| 📋 Ausgabeformat bestimmen | „maximal acht Stichpunkte“ oder „als Tabelle“ |
| 🔎 Schwerpunkt festlegen | „Konzentriere dich auf Budget und Termine.“ |
| ⚠️ Grenzen setzen | „Erfinde keine fehlenden Angaben.“ |
| 🔄 Mit Folgeprompts weiterarbeiten | „Formuliere das kürzer.“ · „Ergänze eine Empfehlung.“ |

Ein **Folgeprompt** ist ein zweiter Auftrag im selben Chat. Copilot kennt dann den ersten Text und ändert nur, was verlangt ist.

Copilot-Ergebnisse immer prüfen, besonders Zahlen, Termine und Namen.

Weiter mit den Apps: [Teil 2 · Copilot in den Apps](02-praxis.md).
