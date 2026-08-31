# Prompt- und Dateienregister

**Stand:** 31.08.2026  
**Zweck:** Eindeutige Rollen-, Versions- und Gültigkeitsübersicht ohne inhaltliche Duplikation der operativen Dateien

## Aktuelle Kernarchitektur

### FILE-001 – System Prompt.md

- Status: zu prüfen
- Typ: globale Steuerung, Deutsch
- Stand: 128 Zeilen / 6.728 Bytes
- Zugehörige Version: VER-002
- Funktion: Rolle, Routingpflicht, Standardmodus, Pflichtangaben, globale Qualitäts- und Schutzregeln
- Abhängigkeiten: FILE-003, themenspezifische Master Prompts und Baselines
- Bekannte Probleme: Produktivstatus gegenüber FILE-016 nicht entschieden; keine vollständige zentrale Sprachsteuerung
- Nachfolger/Kandidat: FILE-002 für englische Architektur; FILE-016 als kompakter Kandidat
- Tests: TEST-001, TEST-006, TEST-012
- Evidenzstatus: direkt belegt

### FILE-002 – System_Prompt_en(1).md

- Status: in Arbeit
- Typ: globale Steuerung, Englisch
- Stand: 114 Zeilen / 5.607 Bytes; 31.08.2026
- Zugehörige Version: VER-004
- Funktion: englische Fassung der Systemsteuerung
- Abhängigkeiten: Sprachplan FILE-009; noch fehlendes zentrales Mapping und englischfähige Master-Prompt-/Outputlogik
- Bekannte Probleme: Vorhandensein der Übersetzung ist kein bestandener Sprachregressionstest
- Vorgänger: FILE-001 als inhaltliche Ausgangsfassung
- Tests: TEST-012, geplante DE/EN-Regression
- Evidenzstatus: direkt belegt

### FILE-003 – 00_Routing-Index.md

- Status: gültig
- Typ: Routing
- Stand: 59 Zeilen / 1.803 Bytes
- Zugehörige Versionen: VER-002, VER-003, VER-004
- Funktion: zwei aktive Recherchebereiche mit Master Prompt und Baseline; Konflikt-, Matrix- und Fallback-Regel
- Abhängigkeiten: FILE-004, FILE-005, FILE-006, FILE-007, FILE-008
- Bekannte Probleme: nennt FILE-004 statt des quellenoptimierten Kandidaten FILE-005; Baselines teilweise ohne exakte Dateiendung; Sprachmapping nicht eingebunden
- Tests: TEST-001
- Evidenzstatus: direkt belegt

### FILE-004 – Master-Prompt Ethernet-APL.md

- Status: gültig
- Einordnung: gemäß aktuellem Routing produktiv referenziert.
- Typ: ausführlicher Fachstandard Ethernet-APL/PoE/PoDL
- Stand: 712 Zeilen / 34.964 Bytes
- Zugehörige Version: VER-002
- Funktion: Erst-/Update-Modus, Scope, Status, Delta, Quellen, Quality Gate und 5-Sheet-Ausgabe
- Abhängigkeiten: FILE-003, FILE-007
- Bekannte Probleme: jüngerer quellenoptimierter Kandidat FILE-005 nicht im Routing; Moduskonflikt zu kompaktem Update-only-Strang
- Nachfolgekandidat: FILE-005
- Tests: TEST-002, TEST-008, TEST-009, TEST-013
- Evidenzstatus: direkt belegt

### FILE-005 – Master-Prompt Ethernet-APL Quellen optimiert.md

- Status: zu prüfen
- Typ: quellenoptimierter Fachstandard Ethernet-APL/PoE/PoDL
- Stand: 1.443 Zeilen / 60.437 Bytes; 27.08.2026
- Zugehörige Version: VER-002
- Funktion: FILE-004 plus verschärfte Belegstellen-, Atomisierungs-, Produkt-/Varianten- und Quellenregeln
- Abhängigkeiten: FILE-003 und FILE-007 müssten bei Freigabe angepasst beziehungsweise regressionsgeprüft werden
- Bekannte Probleme: ausdrückliche Produktivfreigabe und Routing-Anpassung fehlen
- Vorgänger: FILE-004
- Tests: Quellenoptimierung entstand aus TEST-008, TEST-009 und TEST-013; eigener kompletter Regressionstest offen
- Evidenzstatus: direkt belegt

### FILE-006 – Master-Prompt Verifikation.md

- Status: gültig
- Einordnung: aktuell bereitgestellte Fassung; Baseline-Migration bleibt offen.
- Typ: Fachstandard Diagnose & Verifikation
- Stand: 550 Zeilen / 49.537 Bytes; 27.08.2026
- Zugehörige Version: VER-002
- Funktion: direkte Produkt-Tool-Belegkette, Kandidaten vor QG, finale Nachher-Sheets, Kriterienvergleich, Quellen, Delta und Quality Gate
- Abhängigkeiten: FILE-003, FILE-008
- Bekannte Probleme: verlangt sechs Pflicht-Sheets plus optionales siebtes; Baseline 02 besitzt nur fünf; technische Migration und End-to-End-Test fehlen
- Vorgänger: FILE-018 und frühere `Master-Prompt_Verifikation.md`-Fassung
- Tests: TEST-003 bis TEST-005
- Evidenzstatus: direkt belegt

### FILE-007 – Ausgangsmatrix 01.xlsx

- Status: gültig
- Typ: Ethernet-APL-/PoE-/PoDL-Baseline
- Fachlicher Stand: 29.06.2026
- Zugehörige Versionen: VER-002, VER-003
- Funktion: alter Vergleichsstand und Formatvorlage
- Struktur: fünf Sheets
- Bekannte Probleme: Baseline-Datum kann vom vom Nutzer definierten letzten Abruf abweichen; spätere Runs müssen dies ausdrücklich behandeln
- Tests: TEST-002, TEST-008, TEST-009
- Evidenzstatus: direkt belegt

### FILE-008 – Ausgangsmatrix_02.xlsx

- Status: gültig
- Einordnung: als Baseline gültig; fachliche Inhalte teilweise zu prüfen.
- Typ: Verifikationsbaseline
- Fachlicher Stand: 06.07.2026
- Zugehörige Version: VER-002
- Funktion: alter Vergleichsstand für Verifikation
- Struktur: fünf Sheets
- Bekannte Probleme: interne Sekundärquellen, 85–90-%-Einträge und Strukturkonflikt zu FILE-006
- Tests: TEST-003 bis TEST-005
- Evidenzstatus: direkt belegt

### FILE-009 – PLAN_Sprache(1).md

- Status: in Arbeit
- Typ: Umsetzungs- und Testplan
- Stand: 485 Zeilen / 25.784 Bytes; 27.08.2026
- Zugehörige Version: VER-004
- Funktion: gemeinsamer bilingualer GPT, Sprachauswahl, Mapping, Dateinamen und Regression
- Abhängigkeiten: FILE-001 bis FILE-008; geplante Mapping-Datei
- Bekannte Probleme: Plan ist nicht vollständig umgesetzt; Checkbox-/Abnahmestand nicht als abgeschlossen belegt
- Tests: TEST-012 und geplanter Testsatz
- Evidenzstatus: direkt belegt

## Funktions-, Test- und Übergabedokumente

### FILE-010 – PM Research Partner functionality.docx

- Status: gültig
- Typ: englische Funktionsbeschreibung
- Stand: sieben Seiten; 14.08.2026
- Zugehörige Version: VER-002
- Funktion: Fähigkeiten, Recherchebereiche, Workflow, Qualität, Inputs und Outputs erklären
- Bekannte Probleme: bildet nicht alle Änderungen vom 27.–31.08.2026 ab
- Evidenzstatus: direkt belegt

### FILE-011 – PM_Research_Partner_Gesamtuebergabe.md

- Status: archiviert
- Typ: historische Gesamtübergabe
- Stand: 27.08.2026; 1.938 Zeilen
- Funktion: vorheriger zentraler Wissensstand
- Nachfolger: dieses Second Brain
- Bekannte Probleme: einige damalige Blockaden sind inzwischen gelöst; keine modulare laufende Pflege
- Evidenzstatus: direkt belegt

### FILE-012 – Quality-Gate-Protokoll_Ethernet-APL_2026-08-06.md

- Status: archiviert
- Typ: Ex-post-Audit
- Zugehörige Version: VER-002
- Funktion: Prüfung und Nichtfreigabe des Laufs vom 03.08.2026
- Ergebnis: mehrere fachliche und strukturelle Fehler; Grundlage für Korrekturen
- Verknüpfungen: TEST-008, ERR-001 bis ERR-005
- Evidenzstatus: historisch dokumentiert

### FILE-013 – Ethernet-APL_Marktrecherche_Update_2026-08-06.md

- Status: archiviert
- Typ: korrigierter Recherchelauf
- Zugehörige Version: VER-002
- Funktion: korrigierter Stand nach FILE-012
- Duplikat: `(1)`-Kopie gleicher Größe
- Verknüpfungen: RUN-007, TEST-009
- Evidenzstatus: direkt belegt

## Hybrid- und Kompaktdateien

### FILE-014 – Copilot-v1-Prompt_Ethernet-APL_Markdown-zu-Excel.md

- Status: ersetzt
- Typ: Excel-Übergabeprompt
- Zugehörige Version: VER-003
- Problem: zu strenger Preflight; verwertbare Daten konnten durch kleine Auffälligkeiten blockiert werden
- Ersetzt durch: FILE-015
- Tests: TEST-010
- Evidenzstatus: historisch dokumentiert

### FILE-015 – Copilot-v1.1-Prompt_Ethernet-APL_Markdown-zu-Excel.md

- Status: in Arbeit
- Typ: Excel-Übergabeprompt
- Stand: 11.08.2026
- Zugehörige Version: VER-003
- Funktion: technischer Preflight, vier globale Blocker, Warnungs-/Fallbacklogik, keine Fachneubewertung
- Bekannte Probleme: End-to-End-Abnahme auf Copilot Chat Basic fehlt
- Vorgänger: FILE-014
- Tests: TEST-011
- Evidenzstatus: mehrfach bestätigt

### FILE-016 – System-Prompt_new.md / System-Prompt_new(1).md

- Status: zu prüfen
- Typ: kompakter System-Prompt-Kandidat
- Zugehörige Versionen: VER-003, VER-005
- Funktion: reduzierte Routing-, Update- und Schutzlogik
- Bekannte Probleme: zwei leicht unterschiedliche Kopien; Update-only-Konflikt; Produktivstatus unklar
- Evidenzstatus: direkt belegt

### FILE-017 – Master-Prompt Ethernet-APL(2).md

- Status: archiviert
- Typ: kompakter Ethernet-APL-Master
- Zugehörige Versionen: VER-003, VER-005
- Funktion: Kontextreduktion; Rechercheausgabe als Markdown statt direkter Excel-Schwerpunkt
- Bekannte Probleme: nicht mit dem späteren quellenoptimierten FILE-005 verwechseln
- Evidenzstatus: historisch dokumentiert

### FILE-018 – frühere Verifikations-Master-Prompts

- Status: ersetzt
- Typ: `Master-Prompt_Verifikation.md` und `(1)`-Varianten
- Zeitraum: 15.07.–06.08.2026
- Funktion: frühere Fach- und Kompaktstände
- Ersetzt durch: FILE-006
- Risiko: abweichende Dateinamen und Versionen in alten Routing-/Übergabetexten
- Evidenzstatus: direkt belegt

### FILE-019 – Verifikationsmatrix_Rechercheprotokoll_2026-07-16.md

- Status: archiviert
- Typ: Rechercheprotokoll
- Funktion: dokumentiert Verifikations-Updateversuch und Methodenprobleme
- Verknüpfungen: RUN-005, TEST-004, TEST-005
- Evidenzstatus: direkt belegt

## Business-, Design- und Governance-Dateien

### FILE-020 – Fachaufgabe.pptx

- Status: in Arbeit
- Typ: interne Präsentation / Fachaufgabe
- Stand: 43 Folien; Library-Dateistand 16.07.2026; Folien enthalten den Datumsplatzhalter `2027-01-XX`
- Funktion: Business Case, Value, Roadmap und Make-or-Buy-Kommunikation
- Kernaussagen: Make erreicht im Nutzwertvergleich 4,25 vor Buy mit 3,75 und manueller Recherche mit 3,25; historisches Kostenmodell nennt 420,72 €, 4.686,72 € und 6.400 € für zwölf Monate.
- Bekannte Probleme: manuelle Recherche wird zugleich mit vier Läufen à 50 Stunden, 300 Stunden/Jahr und 50 Stunden Einsparung pro Monat beschrieben; diese Werte sind rechnerisch und semantisch nicht konsistent. Finale Zahlen und Lizenzstände sind zeitabhängig.
- Tests: TEST-014
- Evidenzstatus: direkt belegt

### FILE-021 – Second-Brain-Design-Spezifikation

- Status: gültig
- Typ: Governance-Spezifikation
- Stand: 31.08.2026
- Funktion: Architektur, ID-/Status-/Evidenzmodell und Abnahmekriterien des Second Brain
- Evidenzstatus: direkt belegt

### FILE-022 – Second-Brain-Umsetzungsplan

- Status: gültig
- Typ: Ausführungsplan
- Stand: 31.08.2026
- Funktion: zehn Arbeitspakete und Validierungsanforderungen
- Evidenzstatus: direkt belegt

### FILE-023 – deep-research-report.md

- Status: archiviert
- Typ: früher Ethernet-APL-Deep-Research-Lauf
- Stand: 02.06.2026; Zeitraum 01.10.2025–01.06.2026
- Funktion: frühe Marktaktualisierung und Excel-Ausgabe
- Risiko: nicht mit aktuellem Master-Prompt- und Baseline-Stand gleichsetzen
- Evidenzstatus: direkt belegt

## Fehlende oder geplante Dateien

- `00_Language-Mapping-DE-EN.md`: geplant, nicht als vorhandene produktive Datei belegt.
- kanonisches `00_File-Manifest.md`: durch dieses Register teilweise vorweggenommen, als operative Manifestdatei aber noch nicht eingeführt.
- formales `CHANGELOG.md`: noch nicht eingeführt.
- Gold-Standard-Datensatz für Regression: noch nicht verbindlich festgelegt.
