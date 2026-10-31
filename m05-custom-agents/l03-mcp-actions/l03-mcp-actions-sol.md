# Lab 5.3 – Lösung: Vom Antworten zum Handeln: Agenten mit MCP verbinden

## Aufgabe 1: Demo

Der Ablauf steht im Abschnitt „Die Demo" der Theorie.

## Aufgabe 2: Quiz

| Frage | Antwort | Erklärung |
| ----- | ------- | --------- |
| 1. Welche Aktion braucht eine Bestätigung? | **C** | Ein neues Ticket ändert das Ticketsystem; A, B und D lesen nur. |
| 2. Was ist ein MCP-Server? | **B** | Ein MCP-Server bietet Werkzeuge mit Name und Beschreibung an; der Agent liest die Beschreibung und wählt. Er trainiert kein Modell und ersetzt weder Wissen noch Freigabe. |

## Erweiterung

### 1. Stelle der Bestätigung

In Schritt 3 der Demo: Der Agent hat `ticket_anlegen` gewählt, zeigt den Entwurf (Kategorie VPN, Beschreibung) und fragt „Soll ich das Ticket so anlegen?". Erst nach „Ja" führt er das Werkzeug aus. Die Suche mit `tickets_suchen` in Schritt 2 läuft ohne Bestätigung, weil sie nur liest.

### 2. Aktion und Freigaberegel

| Aktion | Art | Freigaberegel |
| ------ | --- | ------------- |
| Ticket für ein abgelaufenes VPN-Zertifikat anlegen | ändernd | Der Agent zeigt Kategorie und Beschreibung als Entwurf und legt das Ticket erst an, wenn die fragende Person bestätigt. |
| Status des eigenen Tickets abfragen | lesend | Die IT gibt die Verbindung zum Ticketsystem einmal frei; einzelne Abfragen laufen ohne Bestätigung und zeigen nur eigene Tickets. |

Eine der beiden Zeilen genügt.

### 3. Prüffragen an den Betreiber

- Welche Werkzeuge bietet der MCP-Server an, und lassen sich ändernde Werkzeuge abschalten?
- Welche Daten sieht der Server, wo werden sie verarbeitet, und wer ist Ansprechpartner bei einem Fehler?
