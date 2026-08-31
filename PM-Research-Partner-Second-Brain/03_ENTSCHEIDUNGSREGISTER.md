# Entscheidungsregister

**Stand:** 31.08.2026  
**Regel:** Nur ausdrücklich beschlossene oder in produktiven Dateien verbindlich verankerte Punkte erhalten `gültig`. Frühere Empfehlungen ohne Nutzerfreigabe erscheinen nicht als Entscheidung.

## Architektur und Arbeitsmodus

### DEC-001 – Modulare Knowledge-Architektur

- Status: gültig
- Datum: 25.06.2026 bis 29.06.2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: mehrfach bestätigt
- Ausgangssituation: Ein einzelner Mega-Prompt wäre schwer erweiterbar und würde das Zeichen-/Kontextbudget belasten.
- Entscheidung: Globale Steuerung, Routing, Fachlogik und Vergleichsstand werden in System Prompt, Routing Index, Master Prompts und Baselines getrennt.
- Begründung: klare Verantwortlichkeiten, Erweiterbarkeit und geringere Versionsdrift.
- Auswirkungen: FILE-001, FILE-003 bis FILE-008.
- Verknüpfungen: TEST-001; LESSON-018.

### DEC-002 – Routing vor jeder Recherche

- Status: gültig
- Datum: 29.06.2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Jede Rechercheanfrage wird zuerst über FILE-003 einem Fachbereich, Master Prompt und einer Baseline zugeordnet.
- Fallback: Bei unklarer oder fehlender Route wird gezielt nachgefragt; es wird keine Fachlogik improvisiert.
- Auswirkungen: neue Bereiche benötigen Route, Master Prompt, Baseline/Erstmodus und Test.
- Verknüpfungen: DEC-001; TEST-001; ERR-011.

### DEC-003 – Update-Recherche als Standard bei vorhandener Baseline

- Status: gültig
- Datum: 03.08.2026; in aktuellen System Prompts bestätigt
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Ist eine alte Matrix oder ein alter Recherche-Stand vorhanden, wird standardmäßig im Update-Modus gearbeitet.
- Abgrenzung: Ob die produktive Lösung zusätzlich Erst-Recherche unterstützt oder vollständig Update-only wird, bleibt OPEN-001.
- Auswirkungen: Pflicht zu Baseline-Vergleich und Delta.
- Verknüpfungen: DEC-004; OPEN-001.

### DEC-004 – Zeitraum und Baseline als Preflight-Pflicht

- Status: gültig
- Datum: 03.08.2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Bei Update-Recherche müssen letzter Abruf, aktueller Abruf, Baseline und Thema eindeutig sein; sonst kurze gezielte Rückfrage.
- Begründung: Ohne Zeitraum kein belastbares Delta; ohne Baseline kein alter Vergleichsstand.
- Auswirkungen: System- und Master-Prompts, Recherchevorlage.
- Verknüpfungen: TEST-007; LESSON-023.

## Ethernet-APL-Fachlogik

### DEC-005 – Hierarchischer Recherche-Scope

- Status: gültig
- Datum: 03.08.2026; fachlicher Ursprung 06/2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: mehrfach bestätigt
- Entscheidung: Priorität 1 Ethernet-APL; Priorität 2 PoE/PoDL in eigener Matrix; Priorität 3 Kommunikationsprofile als Zusatzinformation.
- Harte Grenze: PoE, PoDL oder allgemeines Ethernet dürfen keinen positiven APL-Status auslösen.
- Verknüpfungen: ERR-006; LESSON-001 bis LESSON-004.

### DEC-006 – Konservative APL-Statuslogik

- Status: gültig
- Datum: 06/2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Hauptmatrix verwendet ausschließlich `verfügbar`, `in Planung`, `keine Infos`, `nicht vorhanden`.
- Bedingung: `verfügbar` nur mit ausdrücklichem APL-Nachweis; `nicht vorhanden` nur mit Negativnachweis; sonst `keine Infos`.
- Verknüpfungen: DEC-010; LESSON-005 bis LESSON-007.

### DEC-007 – Fachstatus und sichtbarer Zellwert trennen

- Status: gültig
- Datum: 25.06.2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: mehrfach bestätigt
- Entscheidung: Zellfarbe repräsentiert den APL-Fachstatus; sichtbarer Text kann ein belegtes Kommunikationsprofil zeigen.
- Schutzregel: Profilanzeige nur bei gleichzeitig belegtem Ethernet-APL.
- Verknüpfungen: ERR-015; LESSON-002.

### DEC-008 – Delta ohne unveränderte Einträge

- Status: gültig
- Datum: 08.–25.06.2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: mehrfach bestätigt
- Entscheidung: Delta verwendet `Neu`, `Geändert`, `Entfernt / abgekündigt`, `Unklar`; `Unverändert` wird nicht ausgegeben.
- Weitere Regel: neu gefunden, Scope-Erweiterung und Baseline-Korrektur sind nicht automatisch `Neu`.
- Verknüpfungen: TEST-002, TEST-008, TEST-009; ERR-006, ERR-007.

### DEC-009 – Direkte, atomare Belegkette

- Status: gültig
- Datum: 15.07.2026; verschärft 12.–27.08.2026
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Jede materielle Bewertung benötigt eine direkte, nachvollziehbare Belegstelle zur konkreten Produkt-/Varianten-/Messprinzip-Kombination; Quellenzeilen werden atomar geführt.
- Auswirkungen: FILE-005 entstand als quellenoptimierte Fassung.
- Verknüpfungen: TEST-005, TEST-008, TEST-013; ERR-001, ERR-002, ERR-009, ERR-016, ERR-017.

### DEC-010 – 95-%-Schwelle und Negativnachweis

- Status: gültig
- Datum: 06/2026; mehrfach bestätigt
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Informationen unter 95 % dürfen nicht als bestätigter Fakt erscheinen. `nicht vorhanden` benötigt ausdrückliche negative Evidenz.
- Einschränkung: Prozentwert ersetzt keine richtige Produkt-/Quellenzuordnung.
- Verknüpfungen: ERR-010, ERR-018; LESSON-013, LESSON-027.

## Verifikation und Quality Gate

### DEC-011 – Verifikation strikt von Diagnose und Monitoring trennen

- Status: gültig
- Datum: 29.06.–06.07.2026; verschärft 27.08.2026
- Betroffene Versionen: VER-002, VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Verifikation verlangt eine aktive/geführte Prüfung gegen Referenzbedingungen mit dokumentiertem Ergebnis. Diagnose, Monitoring, Predictive Maintenance und Kalibrierung sind kein Ersatz.
- Auswirkungen: FILE-006, FILE-008 und Verifikationsmatrix.
- Verknüpfungen: TEST-003 bis TEST-005; ERR-008, ERR-009, ERR-010.

### DEC-012 – KROHNE-Benchmark ohne Sonderbehandlung

- Status: gültig
- Datum: spätestens 27.08.2026
- Betroffene Versionen: VER-002
- Evidenzstatus: direkt belegt
- Entscheidung: OPTICHECK und `OPTICHECK Technology built in` sind interne Benchmarks, aber kein vorweggenommener Verfügbarkeitsnachweis. KROHNE wird nach denselben Belegregeln wie Wettbewerber bewertet.
- Verknüpfungen: DEC-011; ERR-009.

### DEC-013 – Vierstufiges Quality Gate

- Status: gültig
- Datum: 06/2026; in FILE-010 bestätigt
- Betroffene Versionen: VER-002 bis VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Research → Quality Review → Advisor Review → Final Approval.
- Governance: Quality Gate gilt nur als durchgeführt, wenn Einwände, Korrekturen und Freigabe nachvollziehbar dokumentiert sind.
- Verknüpfungen: TEST-008; ERR-005; LESSON-025 bis LESSON-030.

### DEC-014 – Vorher-/Nachher-Sheets für Verifikation

- Status: gültig
- Datum: 27.08.2026
- Betroffene Versionen: VER-002
- Evidenzstatus: direkt belegt
- Entscheidung: Kandidaten bleiben in Vorher-Sheets sichtbar; finale Freigabe erfolgt ausschließlich in strukturgleichen Nachher-Sheets. Delta und Summary nutzen nur Nachher-Ergebnisse.
- Auswirkungen: FILE-006 verlangt sechs Pflicht-Sheets plus optionales siebtes.
- Offene Umsetzung: Migration von FILE-008 und End-to-End-Test, OPEN-008.

## Versionen, Hybrid und Sprache

### DEC-015 – Verbindliche Versionsbegriffe

- Status: gültig
- Datum: 13.08.2026
- Betroffene Versionen: VER-002, VER-003
- Evidenzstatus: direkt belegt
- Entscheidung: `PM Research Partner 2.0` bezeichnet die Vollversion; `PM Research Partner hybrid` bezeichnet die gekürzte kompakte Copilot-Version.
- Auswirkungen: alle späteren Dokumente und Gespräche.

### DEC-016 – Recherche und Excel-Übertragung im Hybrid trennen

- Status: gültig
- Datum: 06.08.2026
- Betroffene Versionen: VER-003
- Evidenzstatus: direkt belegt
- Entscheidung: ChatGPT führt die fachliche Ethernet-APL-Recherche durch; Copilot prüft/überträgt das freigegebene Evidence-Markdown in Excel.
- Harte Grenze: Copilot darf nicht selbst im Web recherchieren oder Fachbewertungen umdeuten.
- Verknüpfungen: FILE-014, FILE-015; TEST-010, TEST-011.

### DEC-017 – Copilot v1 durch v1.1 ersetzen

- Status: gültig
- Datum: 11.08.2026
- Betroffene Versionen: VER-003
- Evidenzstatus: mehrfach bestätigt
- Entscheidung: v1.1 verwendet nur technische Hard-Stop-Blocker; sonst Warnungen und Fallbacks. Details haben Vorrang vor Übersichten und eine nutzbare Datei soll trotz nichtkritischer Auffälligkeiten erzeugt werden.
- Ersetzt: Preflight-Logik aus FILE-014
- Verknüpfungen: ERR-013; TEST-010, TEST-011.

### DEC-018 – Ein gemeinsamer bilingualer GPT

- Status: gültig
- Datum: 13.08.2026
- Betroffene Versionen: VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: DE und EN werden in einem gemeinsamen PM Research Partner umgesetzt; kein dauerhaft separater EN-GPT.
- Ausnahme: nur bei fachlich/organisatorisch abweichender Zielgruppe, Logik, Compliance oder Release-Verantwortung.
- Verknüpfungen: FILE-009; TEST-012; OPEN-005.

### DEC-019 – Sprache nur in der Präsentationsschicht variieren

- Status: gültig
- Datum: 13.08.2026
- Betroffene Versionen: VER-004
- Evidenzstatus: direkt belegt
- Entscheidung: Sprachsteuerung wird einmal pro Auftrag gesetzt; Fachlogik und kanonische Statusbedeutungen bleiben identisch; Übersetzung erzeugt kein Delta.
- Auswirkungen: Ausgangsmatrizen bleiben historische Baselines und werden nicht überschrieben.
- Verknüpfungen: DEC-018; FILE-002, FILE-009.

### DEC-020 – Architektur grundsätzlich auf Englisch ausrichten

- Status: in Arbeit
- Datum: 27.–31.08.2026
- Betroffene Versionen: VER-004
- Evidenzstatus: mehrfach bestätigt
- Entscheidung: Die Architekturdateien werden schrittweise ins Englische übertragen, während eine verbindliche Sprachregel deutsche und englische Ergebnisse ermöglicht.
- Bisher umgesetzt: englische System-Prompt-Fassung.
- Noch offen: Routing, beide Master Prompts, zentrale Mapping-Ressource und Regression.
- Verknüpfungen: OPEN-005.

## Quellen, Business Case und Governance

### DEC-021 – Quellenoptimierung als eigener Entwicklungsstrang

- Status: gültig
- Datum: 12.–27.08.2026
- Betroffene Versionen: VER-002, VER-004
- Evidenzstatus: mehrfach bestätigt
- Entscheidung: allgemeine Produktgruppenlinks reichen nicht; Quellen müssen direkt, eindeutig und der konkreten Bewertung zuordenbar sein.
- Umsetzung: `Master-Prompt Ethernet-APL Quellen optimiert.md` erstellt.
- Offene Freigabe: Routing/Produktivstatus, OPEN-003.

### DEC-022 – Praktischer Hybrid-Business-Case

- Status: gültig
- Datum: 03.–06.08.2026
- Betroffene Versionen: VER-002, VER-003
- Evidenzstatus: historisch dokumentiert
- Entscheidung: Für den aktuellen praktischen Workflow bleibt ChatGPT für Recherche/Reasoning zuständig; vorhandenes Copilot Chat Basic wird als Excel-Umsetzer getestet. Copilot Premium wird erst bei nachgewiesenem Mehrwert empfohlen.
- Abgrenzung: finale organisatorische Lizenzentscheidung bleibt OPEN-011.

### DEC-023 – Second Brain als modulare Single Source of Truth

- Status: gültig
- Datum: 31.08.2026
- Betroffene Versionen: gesamtes Projekt
- Evidenzstatus: direkt belegt
- Entscheidung: Zentralindex plus thematische Dateien und chronologisches Archiv; unveränderliche IDs, Status- und Evidenzmodell; operative Prompts werden nicht dupliziert.
- Begründung: die frühere Übergabe war als Momentaufnahme zu groß und nicht dauerhaft pflegbar.
- Auswirkungen: dieses gesamte Verzeichnis und README_PFLEGEANLEITUNG.md.

## Nicht als Entscheidung gewertete frühere Vorschläge

Die folgenden Punkte bleiben offen, weil kein belastbarer finaler Nutzerbeschluss dokumentiert ist:

- 2.1 wird die einzige Vollversion und 2.0 nur Fallback,
- endgültige Modellwahl GPT-5.6 Sol versus Thinking,
- endgültige Lizenzfreigabe ChatGPT Plus versus Copilot Premium,
- lange oder kompakte System-Prompt-Fassung als alleinige Produktion,
- vollständiges Update-only ohne Erst-Recherche,
- Verantwortlicher für Chairman-/Release-Freigabe.
