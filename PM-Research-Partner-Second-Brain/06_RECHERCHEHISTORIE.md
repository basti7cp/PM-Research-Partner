# Recherchehistorie

**Stand:** 31.08.2026  
**Grundsatz:** Nur dokumentierbare Durchläufe oder klar erkennbare Entwicklungsphasen werden aufgenommen. Fehlende Zeiträume und Ergebnisdateien werden nicht erfunden.

## Chronologische Übersicht

| ID | Zeitraum/Abruf | Bereich | Baseline | Ergebnisstatus |
|---|---|---|---|---|
| RUN-001 | bis 10/2025 | ursprüngliche Ethernet-/Energieversorgung-Marktstudie | keine standardisierte Baseline belegt | historische Ausgangsphase |
| RUN-002 | 01.10.2025–01.06.2026 | Ethernet-APL Deep Research | frühere Marktstudie | historische Ergebnisdatei vorhanden |
| RUN-003 | 08.06.–29.06.2026 | Ethernet-APL/PoE/PoDL Update | Stand 08.06.2026 | Baseline 01 erzeugt |
| RUN-004 | Stand 06.07.2026 | Verifikation | interne Wettbewerber-Decks | Baseline 02 erzeugt, provisorisch |
| RUN-005 | 16.07.2026 | Verifikationsupdate | Baseline 02 | blockiert/unvollständig |
| RUN-006 | Datei 03.08.; Audit 06.08.2026 | Ethernet-APL Update | Baseline 01 | nicht freigegeben |
| RUN-007 | 06.08.2026 | korrigierter Ethernet-APL-Update | Baseline 01 | freigegeben mit offenem Hinweis |
| RUN-008 | 10.–13.08.2026 | Ethernet-APL Update-Testserie | verschiedene alte Abrufstände | Quellenkonsistenz nicht stabil |
| RUN-009 | 27.08.2026 | Verifikationsmatrix-Update | letzter Abruf 06.07.2026 | Anfrage belegt; finale Ergebnisdatei nicht verfügbar |

## Detailregister

### RUN-001 – Ursprüngliche Marktstudie

- Status: archiviert
- Datum/Phase: bis Oktober 2025
- Evidenzstatus: historisch dokumentiert
- Thema: Ethernet-APL, PoE, PoDL und Ethernet-basierte Kommunikation bei Durchflussmessgeräten
- Letzter/Aktueller Abruf: nicht als standardisiertes Update-Intervall dokumentiert
- Baseline: noch keine heutige Standardbaseline
- Master Prompt: frühe Projektphase vor finaler modularer Architektur
- Kernergebnis: unter elf Wettbewerbern wurden als damaliger Arbeitsstand zwei PoE-Geräte und eine PoDL-Lösung dokumentiert; genaue aktuelle Gültigkeit nicht ungeprüft übernehmen.
- Bedeutung: fachlicher Ursprung von Matrix, Quellen- und Updatekonzept.
- Freigabestatus: historische Referenz
- Verknüpfungen: VER-001; FILE-023.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-001_URSPRUENGLICHE_MARKTSTUDIE.md`

### RUN-002 – Ethernet-APL Deep Research 2025/2026

- Status: archiviert
- Datum: 02.06.2026
- Evidenzstatus: direkt belegt
- Thema: Ethernet-APL-Evidenz im Zeitraum 01.10.2025–01.06.2026
- Baseline: frühere Marktstudie
- Master Prompt: früher Research-Stand
- Ergebnisdatei: FILE-023 `deep-research-report.md`; damalige Excel-Ausgabe erwähnt
- Kernergebnis: datierte APL-Evidenzen für mehrere Hersteller; mehrere plausible Funde unter 95 % oder ohne passenden Zeitnachweis nicht positiv übernommen.
- Qualitätsmerkmal: konservative Schwelle und Trennung von Abruf-/Veröffentlichungszeit.
- Freigabestatus: historische Referenz; nicht aktueller Marktstand
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-002_2026-06-01_APL_DEEP_RESEARCH.md`

### RUN-003 – Ethernet-APL-Baseline-Update

- Status: archiviert
- Datum: 29.06.2026
- Evidenzstatus: direkt belegt
- Thema: Ethernet-APL/PoE/PoDL
- Letzter Abruf: 08.06.2026
- Aktueller Abruf: 29.06.2026
- Baseline: Matrix vom 08.06.2026
- Master Prompt: FILE-004
- Ergebnisdatei: FILE-007
- Kernergebnis: Scope um Druck, Füllstand, Temperatur erweitert; 14 positive APL- und sechs PoE/PoDL-Kombinationen; unveränderte Einträge nicht im Delta.
- Delta: neue Scope-Funde als `Unklar`; keine falsche Marktneuheit.
- Freigabestatus: Baseline 01
- Verknüpfungen: TEST-002; ERR-006, ERR-007; LESSON-015 bis LESSON-017.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-003_2026-06-29_APL_UPDATE.md`

### RUN-004 – Verifikationsbaseline

- Status: archiviert
- Datum: 06.07.2026
- Evidenzstatus: direkt belegt
- Thema: Diagnose & Verifikation
- Letzter Abruf: nicht als klassisches Updateintervall dokumentiert
- Aktueller Stand: 06.07.2026
- Baseline: interne Wettbewerber-Recherchepräsentationen 2024–2026
- Master Prompt: damaliger Verifikationsstand
- Ergebnisdatei: FILE-008
- Kernergebnis: 15 positive Kandidatenzellen und Kriterienprofile für sechs Hersteller.
- Qualitätsproblem: interne Sekundärquellen und Sicherheitslevel unter 95 %; alle positiven Kandidaten offiziell nachzubelegen.
- Freigabestatus: provisorische Baseline
- Verknüpfungen: TEST-003; ERR-010.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-004_2026-07-06_VERIFIKATIONSBASELINE.md`

### RUN-005 – Verifikationsupdateversuch

- Status: archiviert
- Datum: 16.07.2026
- Evidenzstatus: direkt belegt
- Thema: Verifikationsmatrix aktualisieren
- Letzter Abruf: 06.07.2026 beziehungsweise Baseline 02; genaue Anfragefelder nicht vollständig belegt
- Aktueller Abruf: 16.07.2026
- Baseline: FILE-008
- Master Prompt: im Lauf nicht eindeutig verfügbar
- Ergebnisdatei: FILE-019
- Kernergebnis: belastbare Aktualisierung nicht freigegeben; Regel-/Dateizugriff war nicht eindeutig.
- Freigabestatus: blockiert
- Verknüpfungen: TEST-004, TEST-005; ERR-011.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-005_2026-07-16_VERIFIKATIONSUPDATE.md`

### RUN-006 – Ethernet-APL-Lauf vom 03.08.2026

- Status: archiviert
- Datum: Datei 03.08.2026; Audit 06.08.2026
- Evidenzstatus: historisch dokumentiert
- Thema: Ethernet-APL-Update
- Baseline: FILE-007
- Master Prompt: Ethernet-APL-Fachlogik
- Ergebnisdatei: Originaldatei nicht als eigene aktuelle Quelle im Second Brain; Audit FILE-012
- Kernergebnis: zunächst ausgegebener Stand enthielt mehrere Fehler.
- Fehler: H250 M40 falsch positiv; ABB Vortex indirekt; Datum/PoE-PoDL-Sheet inkonsistent; QG nicht nachweisbar; Summary falsch.
- Freigabestatus: nicht freigegeben
- Verknüpfungen: TEST-008; ERR-001 bis ERR-005.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-006_2026-08-03_APL_NICHT_FREIGEGEBEN.md`

### RUN-007 – Korrigierter Ethernet-APL-Lauf

- Status: archiviert
- Datum: 06.08.2026
- Evidenzstatus: direkt belegt
- Thema: Korrektur des Ethernet-APL-Updates
- Letzter Abruf/Baseline: FILE-007; Abweichung zwischen Baseline-Stand und Nutzerintervall wurde als offener Hinweis dokumentiert
- Aktueller Abruf: 06.08.2026
- Ergebnisdatei: FILE-013
- Kernergebnis: H250 zurückgestuft; Siemens Druck datiertes Delta; VEGA-Profil Baseline-Korrektur; PoE/PoDL getrennt; Summary differenziert.
- Freigabestatus: freigegeben mit offenem Baseline-Datumshinweis
- Verknüpfungen: TEST-009; LESSON-028.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-007_2026-08-06_APL_KORRIGIERT.md`

### RUN-008 – Ethernet-APL-Update-Testserie

- Status: archiviert
- Zeitraum: 10.–13.08.2026
- Evidenzstatus: historisch dokumentiert
- Thema: kurze Matrixupdates und Quellenkritik
- Belegte Einzelanfragen: Abrufstände am 10., 11., 12. und 13.08.2026; unter anderem letzter Abruf 01.07.2026 am 11.08. sowie Baseline 29.06.2026 in weiteren Läufen.
- Baselines: FILE-007 beziehungsweise vom Nutzer testweise bereitgestellte Matrix
- Master Prompt: FILE-004
- Ergebnisdateien: nicht vollständig als zusammenhängender Satz verfügbar
- Kernergebnis: Siemens Druck wurde zwischen Chats unterschiedlich überzeugend belegt; allgemeine Quellen reichten nicht, direkte Siemens-Dokumentation war erforderlich.
- Freigabestatus: Testserie, kein gemeinsamer produktiver Release
- Verknüpfungen: TEST-013; ERR-017; FILE-005.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-008_2026-08-10_BIS_13_APL_TESTSERIE.md`

### RUN-009 – Verifikationsmatrix-Update 27.08.2026

- Status: zu prüfen
- Datum: 27.08.2026
- Evidenzstatus: historisch dokumentiert
- Thema: Verifikationsmatrix aktualisieren
- Letzter Abruf: 06.07.2026
- Aktueller Abruf: 27.08.2026
- Baseline: FILE-008
- Master Prompt: FILE-006 lag am 27.08.2026 als aktuelle Datei vor
- Ergebnisdatei: im verfügbaren Korpus nicht vorhanden
- Kernergebnis: Anfrage ist belegt; finale Ausführung und Freigabe können ohne Ergebnisdatei nicht behauptet werden.
- Freigabestatus: zu verifizieren
- Verknüpfungen: OPEN-009.
- Archiv: `ARCHIV/RECHERCHE_DURCHLAEUFE/RUN-009_2026-08-27_VERIFIKATIONSUPDATE.md`

## Fachliche Baseline-Anker

### Ethernet-APL – Stand 29.06.2026

FILE-007 dokumentiert unter anderem positive APL-Kombinationen für KROHNE Coriolis, mehrere Endress+Hauser-Messprinzipien, VEGA Füllstand, ABB Coriolis/MID/Vortex, Yokogawa Coriolis/Druck und Siemens Coriolis. Diese Zeilen sind ein historischer Baseline-Stand, kein Ersatz für einen neuen Abruf.

### PoE/PoDL – Stand 29.06.2026

Dokumentiert sind unter anderem Emerson Coriolis (PoE), ABB Coriolis/MID (PoE) und JUMO MID/Druck/Temperatur (PoDL). Diese Technologien bleiben von APL getrennt.

### Verifikation – Stand 06.07.2026

FILE-008 enthält Kandidaten für KROHNE OPTICHECK, Endress+Hauser Heartbeat, Emerson SMV, ABB My Measurement Assistant, Yokogawa FSA130 und Siemens-Verifikationslösungen. Die damalige Baseline besitzt ausdrücklich Nachbelegungsbedarf.

## Noch nicht vollständig rekonstruierbare Läufe

- einzelne kurze Wiederholungen derselben Update-Anfrage ohne gespeicherte Ergebnisdatei,
- genaue Originaleingaben mehrerer Juni-/Juli-Architekturtests,
- vollständiger Ergebnisstand des angefragten Verifikationsupdates vom 27.08.2026,
- mögliche weitere Custom-GPT-Tests außerhalb des verfügbaren Projektkorpus.

Diese Lücken sind kein Grund, Inhalte zu erfinden. Neue Funde werden mit vorhandenen IDs ergänzt oder als neuer Lauf angelegt.
