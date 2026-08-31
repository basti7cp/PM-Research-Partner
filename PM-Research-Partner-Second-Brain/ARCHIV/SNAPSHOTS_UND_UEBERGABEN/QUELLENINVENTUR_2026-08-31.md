# Quelleninventur – PM Research Partner Second Brain

**Stand:** 31.08.2026  
**Status:** gültig  
**Einordnung:** Quelleninventur für die Initialbefüllung  
**Zweck:** Transparente Datenbasis des Second Brain

## Evidenzklassen

- **direkt belegt:** Datei wurde in der Initialbefüllung vollständig oder strukturell ausgewertet.
- **mehrfach bestätigt:** Sachverhalt wird von mehreren Projektartefakten gestützt.
- **historisch dokumentiert:** Inhalt stammt aus einer datierten Übergabe oder eindeutig zuordenbaren Projektchronik.
- **zu verifizieren:** Datei oder Aussage ist bekannt, wurde aber nicht vollständig fachlich geprüft.
- **Duplikat:** inhaltsgleiche oder sehr wahrscheinlich inhaltsgleiche Kopie einer anderen Quelle.

## Aktuell bereitgestellte Kernquellen

### SRC-001 – System Prompt.md

- Typ: Markdown; globale Custom-GPT-Steuerung
- Dateistand: bereitgestellt 31.08.2026; Library-Ursprung 15.07.2026
- Umfang: 128 Zeilen; 6.728 Bytes
- Rolle: Rollenbeschreibung, Routingpflicht, Prioritätenhierarchie, Update-Standard, Pflichtangaben, Schutzregeln und Arbeitsstil
- Evidenzstatus: direkt belegt
- Verwendung: Architektur, Regelwerk, Datei- und Versionsregister
- Hinweis: lange deutsche Fassung; Produktivstatus gegenüber kompaktem Kandidaten weiterhin nicht ausdrücklich entschieden.

### SRC-002 – System_Prompt_en(1).md

- Typ: Markdown; englische System-Prompt-Fassung
- Dateistand: 31.08.2026
- Umfang: 114 Zeilen; 5.607 Bytes
- Rolle: englische Übertragung der globalen Steuerungslogik
- Evidenzstatus: direkt belegt
- Verwendung: Sprachstrategie, Datei- und Versionsregister
- Hinweis: belegt einen Fortschritt der Architekturübersetzung; belegt noch keine vollständige produktive DE/EN-Funktion oder Regressionstest-Freigabe.

### SRC-003 – 00_Routing-Index.md

- Typ: Markdown; Routing
- Dateistand: Library-Ursprung 15.07.2026
- Umfang: 59 Zeilen; 1.803 Bytes
- Rolle: Zuordnung Ethernet-APL → Master Prompt/Baseline 01 sowie Diagnose & Verifikation → Master Prompt/Baseline 02
- Evidenzstatus: direkt belegt
- Verwendung: Architektur, Entscheidung, Regelwerk
- Hinweis: referenziert Baselines teilweise ohne Dateiendung; Dateinamengovernance bleibt offen.

### SRC-004 – Master-Prompt Ethernet-APL.md

- Typ: Markdown; ursprünglicher ausführlicher Fachstandard
- Dateistand: Library-Ursprung 15.07.2026
- Umfang: 712 Zeilen; 34.964 Bytes
- Rolle: Recherche-, Bewertungs-, Quellen-, Delta- und Excel-Logik für Ethernet-APL, PoE und PoDL
- Evidenzstatus: direkt belegt
- Verwendung: Architekturhistorie, Fachregeln, Dateiregister
- Hinweis: unterstützt Erst- und Update-Recherche; dadurch möglicher Konflikt mit Update-only-Kandidaten.

### SRC-005 – Master-Prompt Ethernet-APL Quellen optimiert.md

- Typ: Markdown; quellenoptimierte Weiterentwicklung
- Dateistand: 27.08.2026
- Umfang: 1.443 Zeilen; 60.437 Bytes
- Rolle: verschärfte direkte Belegketten, atomare Evidenz, Produkt-/Variantenbezug und Quellenqualität
- Evidenzstatus: direkt belegt
- Verwendung: aktueller Entwicklungsstand, Quellenstrategie, Fehlerprävention, Roadmap
- Hinweis: jünger und umfangreicher als SRC-004. Ob diese Datei den produktiven Master bereits verbindlich ersetzt, ist nicht ausdrücklich dokumentiert; deshalb `zu prüfen` statt automatisch `gültig`.

### SRC-006 – Master-Prompt Verifikation.md

- Typ: Markdown; aktueller Verifikations-Fachstandard
- Dateistand: 27.08.2026
- Umfang: 550 Zeilen; 49.537 Bytes
- Rolle: Verifikation vor/nach Quality Gate, direkte Produkt-Tool-Belegkette, Kriterienvergleich, Diagnose/Monitoring nur ergänzend
- Evidenzstatus: direkt belegt
- Verwendung: Architektur, Verifikationsregeln, Datei- und Versionsregister
- Hinweis: hebt die Einschränkung der Übergabe vom 27.08.2026 auf, nach der der Verifikations-Master nicht lesbar war.

### SRC-007 – Ausgangsmatrix 01.xlsx

- Typ: Excel; Ethernet-APL-/PoE-/PoDL-Baseline
- Fachlicher Stand: 29.06.2026
- Sheets: `Ethernet-APL Matrix`, `PoE-PoDL Matrix`, `Quellenverzeichnis`, `Delta- und Change-Log`, `Management Summary`
- Rolle: Vergleichsstand für Ethernet-APL-Updates
- Evidenzstatus: direkt belegt
- Verwendung: Baselinehistorie, Recherchehistorie, Regelwerk
- Hinweis: enthält acht Kategorien und 193 Zeilen im Quellenverzeichnis; Scope-Erweiterung 08.06.→29.06.2026 wurde konservativ behandelt.

### SRC-008 – Ausgangsmatrix_02.xlsx

- Typ: Excel; Verifikationsbaseline
- Fachlicher Stand: 06.07.2026
- Sheets: `Verifikations-Matrix`, `Kriterien-Matrix`, `Quellenverzeichnis`, `Delta- und Change-Log`, `Management Summary`
- Rolle: Vergleichsstand für Verifikationsupdates
- Evidenzstatus: direkt belegt
- Verwendung: Baselinehistorie, Verifikationsregeln, offene Quellenarbeit
- Hinweis: Teile beruhen auf internen Wettbewerberpräsentationen und liegen unter dem später verbindlich geforderten 95-%-Standard; Baseline ist deshalb nicht automatisch final freigegeben.

### SRC-009 – PLAN_Sprache(1).md

- Typ: Markdown; Umsetzungsplan
- Dateistand: 27.08.2026; ursprünglicher Plan 13.08.2026
- Umfang: 485 Zeilen; 25.784 Bytes
- Rolle: gemeinsamer bilingualer GPT, zentrale Sprachsteuerung, kanonische Statuswerte, DE/EN-Mapping, Test- und Rollbackplan
- Evidenzstatus: direkt belegt
- Verwendung: Version 2.1, Entscheidungen, Tests, Roadmap
- Duplikat: `PLAN_Sprache.md` in der Library ist in Größe und Inhalt als frühere/gleichartige Kopie dokumentiert.

## Projektübergreifende Primärartefakte

### SRC-010 – PM Research Partner functionality.docx

- Typ: Word; englische Funktionsbeschreibung
- Dateistand: 14.08.2026
- Umfang: sieben Seiten
- Rolle: beschreibt aktuelle Fähigkeiten, zwei Recherchebereiche, Standard-Scope, Workflow, Qualitätslogik, Quality Gate, Eingaben und Excel-Ausgaben
- Evidenzstatus: direkt belegt
- Verwendung: Projektziel, Architektur, Business Value, Qualitätsmodell

### SRC-011 – PM_Research_Partner_Gesamtuebergabe.md

- Typ: Markdown; historische Gesamtübergabe
- Dateistand: 27.08.2026
- Umfang: 1.938 Zeilen; 72.989 Bytes
- Rolle: Projektchronik, Tests, Fehler, Lessons Learned, Business Case und offene Punkte
- Evidenzstatus: direkt belegt
- Verwendung: Initialbefüllung aller Register
- Hinweis: kein aktueller operativer Standard; spätere Dateien und Nutzerentscheidungen haben Vorrang.

### SRC-012 – Quality-Gate-Protokoll_Ethernet-APL_2026-08-06.md

- Typ: Markdown; Ex-post-Audit
- Dateistand: 06.08.2026
- Umfang: 22.514 Bytes
- Rolle: Audit der Datei vom 03.08.2026; dokumentiert KROHNE-H250-, ABB-Vortex-, Datums-, Sheet- und Quality-Gate-Probleme
- Evidenzstatus: mehrfach bestätigt
- Verwendung: Test-, Fehler- und Lessons-Learned-Register

### SRC-013 – Ethernet-APL_Marktrecherche_Update_2026-08-06.md

- Typ: Markdown; korrigierter Recherchelauf
- Dateistand: 06.08.2026
- Umfang: 81.036 Bytes
- Rolle: korrigierter APL-Stand nach Quality-Gate-Audit
- Evidenzstatus: direkt belegt
- Verwendung: Recherche- und Testchronik
- Duplikat: `Ethernet-APL_Marktrecherche_Update_2026-08-06(1).md` besitzt gleiche Größe und ist als Kopie zu behandeln.

### SRC-014 – Copilot-v1-Prompt_Ethernet-APL_Markdown-zu-Excel.md

- Typ: Markdown; Hybrid-Übergabeprompt v1
- Dateistand: 07.08.2026
- Umfang: 17.135 Bytes
- Rolle: Übertragung von freigegebenem Evidence-Markdown in eine Excel-Baseline
- Evidenzstatus: historisch dokumentiert
- Verwendung: Hybridversion, Test- und Fehlerregister
- Hinweis: als zu streng bewertet und durch v1.1 ersetzt.

### SRC-015 – Copilot-v1.1-Prompt_Ethernet-APL_Markdown-zu-Excel.md

- Typ: Markdown; Hybrid-Übergabeprompt v1.1
- Dateistand: 11.08.2026
- Umfang: 21.285 Bytes
- Rolle: technischer Preflight ohne fachliches Vetorecht, Warnungen statt unnötiger Hard-Stops, strukturgetreue Excel-Erzeugung
- Evidenzstatus: mehrfach bestätigt
- Verwendung: aktuelle Hybrid-Arbeitsfassung, Entscheidung, Test, Roadmap
- Hinweis: reproduzierbare End-to-End-Abnahme auf Copilot Chat Basic fehlt weiterhin.

### SRC-016 – System-Prompt_new.md / System-Prompt_new(1).md

- Typ: Markdown; kompakter System-Prompt-Kandidat
- Dateistand: 06.08.2026
- Umfang: 2.769 bzw. 2.793 Bytes
- Rolle: reduzierte globale Steuerung, Update-only, Routing und Schutzregeln
- Evidenzstatus: mehrfach bestätigt
- Verwendung: Architekturhistorie, Prompt-Kürzung, Moduskonflikt
- Duplikat: zwei nahezu gleich große Varianten; Produktivstatus unklar.

### SRC-017 – Master-Prompt Ethernet-APL(2).md

- Typ: Markdown; kompakter Ethernet-APL-Master
- Dateistand: 06.08.2026
- Umfang: 10.635 Bytes
- Rolle: Kontext-reduzierte Hybrid-/Free-Variante
- Evidenzstatus: historisch dokumentiert
- Verwendung: Prompt-Kürzung und Hybridhistorie
- Hinweis: nicht mit SRC-005 verwechseln; unterschiedliche Entwicklungsziele.

### SRC-018 – Master-Prompt_Verifikation(1).md

- Typ: Markdown; kompakter/zwischenzeitlicher Verifikationsstand
- Dateistand: 06.08.2026
- Umfang: 43.020 Bytes
- Rolle: frühere Verifikationsfassung
- Evidenzstatus: historisch dokumentiert
- Verwendung: Versionshistorie
- Hinweis: durch den jüngeren aktuellen Stand SRC-006 überholt, soweit nicht anders freigegeben.

### SRC-019 – Master-Prompt_Verifikation.md

- Typ: Markdown; frühere Verifikationsdatei mit Versionierung
- Dateistand: 15./16.07.2026; Library-Version 3
- Umfang: 66.154 Bytes
- Rolle: früher ausführlicher Verifikations-Fachstandard
- Evidenzstatus: historisch dokumentiert
- Verwendung: Versionshistorie
- Hinweis: Dateiname kollidiert mit der späteren Schreibweise `Master-Prompt Verifikation.md`.

### SRC-020 – Verifikationsmatrix_Rechercheprotokoll_2026-07-16.md

- Typ: Markdown; Rechercheprotokoll
- Dateistand: 16.07.2026
- Umfang: 37.615 Bytes
- Rolle: dokumentiert den Verifikations-Updateversuch und seine Grenzen
- Evidenzstatus: direkt belegt
- Verwendung: Recherche- und Testchronik

### SRC-021 – 2026-07-16-verbindlicher-rechercheablauf-master-prompt.md

- Typ: Markdown; Methoden-/Ablaufdokument
- Dateistand: 16.07.2026
- Umfang: 21.336 Bytes
- Rolle: frühere Festlegung des Rechercheablaufs und der Belegkette
- Evidenzstatus: direkt belegt
- Verwendung: Architektur- und Quellenhistorie

### SRC-022 – deep-research-report.md

- Typ: Markdown; früher Ethernet-APL-Recherchebericht
- Dateistand: 02.06.2026; betrachteter Zeitraum 01.10.2025–01.06.2026
- Umfang: 17.866 Bytes
- Rolle: früher Deep-Research-Lauf mit zeitlich eingeordneten APL-Evidenzen und Excel-Ausgabe
- Evidenzstatus: direkt belegt
- Verwendung: frühe Recherchehistorie
- Hinweis: Ergebnisse werden nicht ungeprüft in den aktuellen Marktstand übernommen.

### SRC-023 – Fachaufgabe.pptx

- Typ: PowerPoint; IHK-/Business-Case-Präsentation
- Dateistand: 16.07.2026
- Umfang: ca. 3,2 MB; 43 Folien
- Rolle: interne Fachaufgabe und Business-Case-Kommunikation
- Evidenzstatus: direkt belegt
- Verwendung: Dateiregister, Business Case, TEST-014, ERR-019 und OPEN-018
- Hinweis: am 31.08.2026 vollständig gerendert, visuell geprüft und textuell extrahiert. Die Präsentation enthält einen historischen Kostenvergleich, aber auch widersprüchliche Zeitangaben und Datumsplatzhalter; konkrete finale Zahlen bleiben zu verifizieren.

## Metaquellen des Second Brain

### SRC-024 – Projektübergreifende Gesprächshistorie

- Typ: personalisierter Gesprächskontext
- Stand: bis 31.08.2026
- Rolle: ergänzt Nutzerentscheidungen, Datumsangaben, Testbeobachtungen und Begriffszuordnungen
- Evidenzstatus: historisch dokumentiert
- Verwendung: alle Register
- Schutzregel: frühere Assistentenvorschläge werden nicht automatisch als Nutzerentscheidung behandelt.

### SRC-025 – Second-Brain-Design-Spezifikation

- Typ: Markdown; freigegebene Designspezifikation
- Dateistand: 31.08.2026
- Rolle: verbindliche Struktur, IDs, Status, Evidenzmodell, Pflege- und Abnahmeregeln
- Evidenzstatus: direkt belegt
- Verwendung: Aufbau und Validierung des Second Brain

### SRC-026 – Second-Brain-Umsetzungsplan

- Typ: Markdown; freigegebener Arbeitsplan
- Dateistand: 31.08.2026
- Rolle: zehn Arbeitspakete zur vollständigen Befüllung und Prüfung
- Evidenzstatus: direkt belegt
- Verwendung: Ausführungssteuerung

## Nicht als eigene Wissensquelle verwendete Dubletten

- `00_Routing-Index(2).md` entspricht nach Größe dem aktuellen Routing Index.
- `Master-Prompt Ethernet-APL(1).md` entspricht nach Größe dem ursprünglichen ausführlichen Master Prompt.
- `PLAN_Sprache.md` und `PLAN_Sprache(1).md` besitzen denselben dokumentierten Umfang.
- `System Prompt.md` und `System Prompt(1).md` besitzen denselben dokumentierten Umfang.
- `Ethernet-APL_Marktrecherche_Update_2026-08-06.md` und die `(1)`-Kopie besitzen denselben Umfang.
- Bilddateien und Layoutgrafiken im Ordner `market research` werden im Dateiregister nur aufgenommen, wenn sie für Roadmap oder Business-Case-Kommunikation relevant sind; sie sind keine fachlichen Quellen für Matrixbewertungen.

## Aufgelöste Widersprüche gegenüber der Übergabe vom 27.08.2026

1. **Verifikations-Master nicht lesbar:** überholt. SRC-006 ist am 31.08.2026 direkt verfügbar und wurde ausgewertet.
2. **Englische Architektur nur geplant:** teilweise überholt. SRC-002 belegt eine vorhandene englische System-Prompt-Fassung; vollständige DE/EN-Produktion und Tests bleiben offen.
3. **Quellenoptimierung nur offene Idee:** teilweise überholt. SRC-005 liegt als konkrete optimierte Datei vor; die produktive Freigabe gegenüber SRC-004 bleibt offen.
