# FAQ

## Copilot allgemein

**Was ist der Unterschied zwischen Copilot Chat und Copilot in den Apps?**
Copilot Chat ist ein Gespräch über mehrere Quellen hinweg. Copilot in Outlook, Word oder Excel arbeitet direkt mit dem Inhalt, der gerade geöffnet ist ([Lab 1.1](../m01-copilot-intro/l01-ai-learning/l01-ai-learning-thx.md)).

**Lernt Copilot aus den eigenen Eingaben?**
Nein. Das Modell ist nach dem Training fertig; Prompts und Antworten werden nicht zum Training der Basismodelle genutzt. Innerhalb eines Chats zählt der bisherige Verlauf ([Lab 1.1](../m01-copilot-intro/l01-ai-learning/l01-ai-learning-thx.md)).

**Sieht Copilot Dateien, auf die die Person keinen Zugriff hat?**
Nein. Copilot sucht über Microsoft Graph nur in Inhalten, die die angemeldete Person ohnehin sehen darf.

**Warum findet `/` eine Datei nicht?**
Meist liegt sie nicht im eigenen OneDrive oder in SharePoint, oder sie wurde gerade erst kopiert und ist noch nicht auffindbar. Datei ins OneDrive kopieren, einige Minuten warten und den Namen neu eingeben ([Lab 1.2](../m01-copilot-intro/l02-first-prompt/l02-first-prompt-thx.md)).

**Warum sieht die Oberfläche anders aus als im Handout?**
Microsoft ändert Copilot laufend; Funktionen hängen außerdem von Lizenz und Tenant ab. Alle „Neu 2026"-Abschnitte tragen deshalb ein Datum.

## Ergebnisse

**Warum erfindet Copilot manchmal Zahlen oder Termine?**
Ein Sprachmodell wählt die wahrscheinlichste Fortsetzung und prüft keine Fakten. Hilfreich: Quelle per `/` angeben, „nutze nur die Quelle" verlangen und jedes Ergebnis prüfen ([Lab 1.1](../m01-copilot-intro/l01-ai-learning/l01-ai-learning-thx.md)).

**Wie lange dauert es, bis Prompts gut werden?**
Die Prompt-Formel wirkt sofort. Eine eigene Sammlung bewährter Prompts, z. B. auf Basis von [prompt-karten.md](../prompt-karten.md), spart danach am meisten Zeit.

**Darf ein Copilot-Entwurf unverändert verschickt werden?**
Technisch ja, verantwortlich bleibt aber die Person, die sendet. Vorher mindestens Zahlen, Termine und Namen gegen die Quelle prüfen ([Lab 6.1](../m06-ai-policy/l01-ai-policy/l01-ai-policy-thx.md)).

## Excel

**Warum rechnet Copilot in Excel manchmal falsch?**
Copilot schreibt Formeln oder Code und lässt Excel rechnen; falsch wird es meist durch einen falschen Zellbereich. Ergebnis gegen eine Kontrollsumme prüfen ([Lab 4.1](../m04-excel/l01-excel-analysis/l01-excel-analysis-thx.md)).

**Warum läuft das Makro nicht?**
Makros laufen nur in Excel Desktop, die Datei muss als `.xlsm` gespeichert sein, und Makros aus dem Internet sind standardmäßig blockiert ([Lab 4.2](../m04-excel/l02-excel-macros/l02-excel-macros-thx.md)).

## Agenten

**Wer sieht einen selbst gebauten Agenten?**
Nach dem Anlegen ist er privat. Erst beim Teilen sehen ihn andere, und zwar mit dem hinterlegten Wissen ([Lab 5.2](../m05-custom-agents/l02-agent-builder/l02-agent-builder-thx.md)).

**Kann der Agent aus Lab 5.2 selbst Tickets anlegen?**
Nicht im Agent Builder. Aktionen und MCP-Verbindungen kommen über Copilot Studio oder Entwicklungswerkzeuge dazu und brauchen eine Freigabe ([Lab 5.3](../m05-custom-agents/l03-mcp-actions/l03-mcp-actions-thx.md)).

**Wann lohnt sich ein Agent statt eines gespeicherten Prompts?**
Wenn dieselbe Frage oft wiederkommt, die Antwort immer in derselben Quelle steht und klare Regeln gelten ([Lab 5.1](../m05-custom-agents/l01-agent-basics/l01-agent-basics-thx.md)).

## Sicherheit

**Darf eine Mail mit Kundennamen zusammengefasst werden?**
Das Auswerten vorhandener Inhalte im freigegebenen System ist in der Regel erlaubt; das aktive Einfügen personenbezogener Daten nur nach Klärung mit der zuständigen Stelle. Maßgeblich ist die eigene KI-Richtlinie ([Lab 6.1](../m06-ai-policy/l01-ai-policy/l01-ai-policy-thx.md)).

**Wen fragen bei Unsicherheit?**
Die Ansprechpersonen, die die eigene KI-Richtlinie nennt, oder die Führungskraft – vor der Nutzung, nicht danach.
