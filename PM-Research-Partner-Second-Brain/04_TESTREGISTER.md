# Testregister

**Stand:** 31.08.2026  
**Hinweis:** Das Register rekonstruiert dokumentierte Tests. Fehlende Originaleingaben oder Ergebnisdateien sind ausdrücklich gekennzeichnet.

## Übersicht

| ID | Datum/Zeitraum | Test | Version | Ergebnis |
|---|---|---|---|---|
| TEST-001 | Juni 2026 | Architektur und Routing | VER-002 | bestanden |
| TEST-002 | 08.–29.06.2026 | Ethernet-APL-Baseline-Update | VER-002 | bestanden mit späteren Quellenrisiken |
| TEST-003 | 06.07.2026 | Verifikationsbaseline | VER-002 | teilweise bestanden / provisorisch |
| TEST-004 | 16.07.2026 | Verifikations-Update | VER-002 | blockiert |
| TEST-005 | Juli 2026 | Verifikations-Belegkette | VER-002 | Probleme identifiziert; Regeln verschärft |
| TEST-006 | August 2026 | Prompt-Kürzung / Kontextbudget | VER-005 | teilweise bestanden |
| TEST-007 | August 2026 | Free-Plan-Kurzanfrage | VER-005 | regelkonform, aber zu starr |
| TEST-008 | 06.08.2026 | Ex-post-QG des Laufs 03.08. | VER-002 | nicht bestanden |
| TEST-009 | 06.08.2026 | korrigierter Ethernet-APL-Lauf | VER-002 | bestanden mit offenem Baseline-Hinweis |
| TEST-010 | 07.–11.08.2026 | Copilot-Prompt v1 | VER-003 | nicht geeignet; zu streng |
| TEST-011 | ab 11.08.2026 | Copilot-Prompt v1.1 | VER-003 | Logik verbessert; End-to-End offen |
| TEST-012 | 13.08.2026 | englische Anfrage | VER-002 | nicht bestanden |
| TEST-013 | 10.–13.08.2026 | Update- und Quellenkritik | VER-002 | Quellenpräsentation nicht stabil |
| TEST-014 | 31.08.2026 | Vollprüfung Fachaufgabe/Business Case | VER-002 | nicht bestanden; Zahlen inkonsistent |

## Detailregister

### TEST-001 – Architektur- und Routingtest

- Status: archiviert
- Datum: Juni 2026
- Evidenzstatus: historisch dokumentiert
- Version: VER-002
- Zweck: Systemsteuerung von Fachdetails entkoppeln und zwei Recherchebereiche routen.
- Eingabe: mehrere Architektur- und Routingprüfungen; exakte vollständige Eingaben nicht archiviert.
- Erwartung: eindeutige Auswahl von Master Prompt und Baseline; Rückfrage bei Gleichrangigkeit; Fallback ohne Improvisation.
- Ergebnis: Grundarchitektur funktionierte; zwei Bereiche verständlich; Konflikt- und Fallbackregeln ergänzt.
- Bewertung: bestanden.
- Lessons: LESSON-018 bis LESSON-023.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-001_ARCHITEKTUR_ROUTING.md`

### TEST-002 – Ethernet-APL-Baseline-Update 08.06.→29.06.2026

- Status: archiviert
- Datum: 29.06.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-002
- Dateien: FILE-004, FILE-007
- Zweck: Baseline aktualisieren, Scope um Druck/Füllstand/Temperatur erweitern und PoE/PoDL getrennt halten.
- Erwartung: acht Kategorien, fünfteilige Excel-Struktur, keine falschen Marktneuheiten aus Scope-Erweiterung.
- Ergebnis: acht Kategorien; 14 positive APL- und sechs positive PoE/PoDL-Kombinationen; Scope-Funde als `Unklar`.
- Bewertung: bestanden; einzelne Quellen-/Produktzuordnungen mussten in späteren Tests erneut geprüft werden.
- Fehler/Lessons: ERR-006, ERR-007; LESSON-015 bis LESSON-017.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-002_APL_BASELINE_2026-06-29.md`

### TEST-003 – Verifikationsbaseline

- Status: archiviert
- Datum: 06.07.2026
- Evidenzstatus: direkt belegt
- Version: VER-002
- Zweck: interne Wettbewerber-Decks in Verifikations- und Kriterienmatrix überführen.
- Erwartung: Verifikation von Diagnose/Monitoring trennen; Vergleichsdimensionen strukturieren.
- Ergebnis: 15 positive Baseline-Zellen; Kriterien für KROHNE, E+H, Emerson, ABB, Yokogawa und Siemens; sechs Unternehmen offen.
- Abweichung: Quellen teilweise nur interne Sekundärquellen mit 85–90 %, trotz späterer 95-%-Schwelle.
- Bewertung: provisorische Baseline, keine finale Marktfreigabe.
- Fehler/Lessons: ERR-010; LESSON-004, LESSON-005, LESSON-013.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-003_VERIFIKATIONSBASELINE_2026-07-06.md`

### TEST-004 – Verifikations-Updateversuch

- Status: archiviert
- Datum: 16.07.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-002
- Dateien: FILE-019; damaliger Master-Prompt-Zugriff unklar
- Zweck: Verifikationsbaseline aktualisieren.
- Ergebnis: belastbare Ausführung blockiert, weil verbindlicher Master Prompt nicht eindeutig verfügbar war.
- Bewertung: blockiert; keine fachliche Improvisation zulässig.
- Fehler/Lessons: ERR-011; LESSON-020, LESSON-023.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-004_VERIFIKATIONSUPDATE_2026-07-16.md`

### TEST-005 – Verifikations-Quellen- und Belegkettentest

- Status: archiviert
- Datum: Juli 2026
- Evidenzstatus: historisch dokumentiert
- Version: VER-002
- Zweck: Qualität von Suchbegriffen, Produkt-Tool-Zuordnung und Delta prüfen.
- Ergebnis: zu breite Begriffe, transitive Produkt-Tool-Verbindungen, Marketingbegriffe und allgemeine Portfolios erzeugten Fehlklassifikationsrisiken.
- Bewertung: Testziel erreicht; Fachlogik wurde verschärft.
- Korrektur: direkte geschlossene Belegkette, Ankerquelle, visuelle PDF-Prüfung und Baseline-Korrektur statt falschem `Neu`.
- Fehler/Lessons: ERR-008, ERR-009, ERR-017; LESSON-004, LESSON-008 bis LESSON-012.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-005_VERIFIKATION_BELEGKETTE.md`

### TEST-006 – Prompt-Kürzung und Kontextbudget

- Status: archiviert
- Datum: August 2026
- Evidenzstatus: historisch dokumentiert
- Version: VER-005
- Zweck: aktive Anweisungen für kleinere Kontextbudgets reduzieren und Excel an Copilot auslagern.
- Zielbudgets: System Prompt ca. 3.300 Zeichen; Routing ca. 900; Fachmaster jeweils ca. 10.500–11.500.
- Ergebnis: Modularisierung sinnvoll; zu starke Kürzung gefährdet Schutzregeln und erzeugte Modus-/Strengekonflikte.
- Bewertung: teilweise bestanden; kein eigenständiger produktiver Release.
- Fehler/Lessons: ERR-012; LESSON-018 bis LESSON-024.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-006_PROMPT_KUERZUNG.md`

### TEST-007 – Free-Plan-Test „Marktrecherche Ethernet-APL“

- Status: archiviert
- Datum: August 2026; exaktes Datum nicht vollständig belegt
- Evidenzstatus: historisch dokumentiert
- Version: VER-005
- Testeingabe: `Marktrecherche Ethernet-APL`
- Erwartung: sinnvoller Einstieg in die Recherche mit knapper Klärung fehlender Angaben.
- Ergebnis: Assistent verlangte sofort letzten und aktuellen Abruf und erklärte ausführlich, dass ohne Zeitraum nicht begonnen werden dürfe.
- Bewertung: fachlich regelkonform, aber zu starr und zu erklärungsreich.
- Korrekturrichtung: kurze gezielte Rückfrage, sinnvolle Defaults und klarere Erst-/Update-Trennung.
- Fehler/Lessons: ERR-012; LESSON-024.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-007_FREE_PLAN_KURZANFRAGE.md`

### TEST-008 – Ex-post-Quality-Gate des Laufs vom 03.08.2026

- Status: archiviert
- Datum: Prüfung 06.08.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-002
- Erwartung: fachlich korrekte Matrix, konsistente Daten, belastbare Quellen und nachvollziehbare Freigabe.
- Ergebnis: nicht freigegeben.
- Hauptabweichungen: H250 M40 falsch positiv; ABB Vortex indirekt; Abrufdatum inkonsistent; PoE/PoDL-Sheet veraltet; QG nicht dokumentiert; Summary übernahm falschen Fund.
- Bewertung: nicht bestanden.
- Fehler/Lessons: ERR-001 bis ERR-005; LESSON-010, LESSON-011, LESSON-025 bis LESSON-030.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-008_EX_POST_QG_2026-08-06.md`

### TEST-009 – Korrigierter Ethernet-APL-Lauf

- Status: archiviert
- Datum: 06.08.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-002
- Erwartung: Fehler aus TEST-008 korrigieren und Änderungen sauber klassifizieren.
- Ergebnis: KROHNE Schwebekörper `keine Infos`; Siemens Druck datiertes Produktdelta; VEGA-Profil Baseline-Korrektur; PoE/PoDL getrennt; Summary differenziert.
- Bewertung: bestanden mit dokumentiertem offenen Punkt zur Baseline-Datumsabweichung.
- Fehler/Lessons: Korrektur ERR-001, ERR-003; LESSON-015 bis LESSON-017, LESSON-028.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-009_APL_KORREKTURLAUF_2026-08-06.md`

### TEST-010 – Copilot-Prompt v1

- Status: archiviert
- Datum: 07.–11.08.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-003
- Zweck: Evidence-Markdown und Baseline in exakt fünf Sheets übertragen.
- Ergebnis: Preflight blockierte bei kleineren Unterschieden, optionalen Feldern oder fehlenden Quellen-IDs zu leicht die gesamte Ausgabe.
- Bewertung: nicht geeignet; durch v1.1 ersetzt.
- Fehler/Lessons: ERR-013; LESSON-035, LESSON-036.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-010_COPILOT_V1.md`

### TEST-011 – Copilot-Prompt v1.1

- Status: in Arbeit
- Datum: ab 11.08.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-003
- Erwartung: nur technische globale Blocker; sonst Warnungen und robuste Datei-Erzeugung.
- Ergebnis: Promptlogik implementiert; vier Blocker, Fallbacks, Detailvorrang und technische Abschlussprüfung definiert.
- Bewertung: Design verbessert; vollständige reproduzierbare Excel-End-to-End-Abnahme auf Copilot Chat Basic nicht belegt.
- Fehler/Lessons: Korrektur ERR-013; LESSON-031 bis LESSON-038.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-011_COPILOT_V1_1.md`

### TEST-012 – Englischer Sprachtest

- Status: archiviert
- Datum: 13.08.2026
- Evidenzstatus: mehrfach bestätigt
- Version: VER-002
- Erwartung: englische Anfrage → englische Chat- und Matrixausgabe.
- Ergebnis: Chat und Matrix blieben deutsch.
- Bewertung: nicht bestanden.
- Ursache: keine zentrale Sprachsteuerung; deutsche Knowledge-Dateien und Baselines dominierten.
- Korrektur: VER-004, FILE-009 und FILE-002; Regression bleibt offen.
- Fehler/Lessons: ERR-014; LESSON-039 bis LESSON-043.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-012_ENGLISCHE_AUSGABE.md`

### TEST-013 – Update- und Quellenkritiktests

- Status: archiviert
- Datum: 10.–13.08.2026
- Evidenzstatus: historisch dokumentiert
- Version: VER-002
- Zweck: kurze APL-Updates und direkte Belegqualität prüfen.
- Ergebnis: Siemens Druck wurde in verschiedenen Chats unterschiedlich überzeugend belegt; allgemeine Quellen waren intern nicht ausreichend, direkte Dokumentation dagegen überzeugend.
- Bewertung: Fachstatus kann korrekt sein, ist mit schwacher Quellenpräsentation aber praktisch nicht belastbar nutzbar.
- Korrektur: FILE-005 und strengere direkte Belegstellen.
- Fehler/Lessons: ERR-017; LESSON-008 bis LESSON-014.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-013_QUELLENKRITIK_2026-08-10_BIS_13.md`

### TEST-014 – Vollprüfung Fachaufgabe und Business Case

- Status: archiviert
- Datum: 31.08.2026
- Evidenzstatus: direkt belegt
- Version: VER-002
- Datei: FILE-020
- Zweck: alle 43 Folien vollständig auf Business-Case-Annahmen, Konsistenz und verwertbare Projektgeschichte prüfen.
- Erwartung: Zeit-, Kosten- und Nutzenangaben sind rechnerisch konsistent und besitzen einen eindeutigen Stand.
- Ergebnis: Make wird mit Nutzwert 4,25 und 420,72 € für zwölf Monate als beste Variante dargestellt. Vier manuelle Läufe à 50 Stunden widersprechen jedoch der Angabe 300 Stunden/Jahr und der Aussage 50 Stunden Ersparnis pro Monat; Datumsplatzhalter sind nicht aufgelöst.
- Bewertung: nicht bestanden als finaler monetärer Business Case; als historische Prozess- und Lösungsdokumentation verwertbar.
- Fehler/Lessons: ERR-019; LESSON-044.
- Archiv: `ARCHIV/TESTDURCHLAEUFE/TEST-014_FACHAUFGABE_BUSINESS_CASE.md`

## Offene Pflicht-Tests

- vollständiger Regressionstest FILE-005 gegen FILE-004,
- Routingtest nach möglicher Freigabe neuer Dateinamen,
- vollständiger Verifikations-End-to-End-Test mit 6+1 Sheets,
- Copilot-v1.1-End-to-End-Test mit Excel-Zellvergleich,
- vollständiger DE/EN-Regressionssatz,
- Gold-Standard-Vergleich der vorgesehenen Modelle.
- korrigierter und mit aktuellen Annahmen freigegebener Business-Case-Rechentest.
