# Fehler und Lessons Learned

**Stand:** 31.08.2026

## Fehlerregister

### ERR-001 – H250 M40 fälschlich APL-positiv

- Status: ersetzt
- Datum: erkannt 06.08.2026
- Evidenzstatus: historisch dokumentiert
- Ursache: APL-Angabe aus benachbartem Coriolis-Produktblock übernommen.
- Auswirkung: falsche Matrixzelle, falsches Delta und falsche Management Summary.
- Korrektur: auf `keine Infos` zurückgesetzt; Produktblock und Belegstelle direkt zuordnen.
- Tests: TEST-008, TEST-009.

### ERR-002 – ABB Vortex nur indirekt belegt

- Status: offen
- Datum: 06.08.2026
- Evidenzstatus: historisch dokumentiert
- Ursache: ProcessMaster-Quelle auf VortexMaster übertragen.
- Auswirkung: positive Aussage nicht direkt nachvollziehbar.
- Korrektur: direkte VortexMaster-Quelle oder Rückstufung.
- Tests: TEST-008.

### ERR-003 – „Stand heute“ nicht auf tatsächliches Datum aktualisiert

- Status: ersetzt
- Evidenzstatus: direkt belegt
- Datum: 06.08.2026
- Ursache: Ergebnisstand 03.08. trotz Auftrag 06.08.
- Auswirkung: falscher Berichtsstand.
- Korrektur: aktuelles Abrufdatum im Preflight und in allen Sheets abgleichen.
- Tests: TEST-008, TEST-009.

### ERR-004 – PoE-/PoDL-Sheet zeitlich älter als Hauptsheet

- Status: offen
- Evidenzstatus: direkt belegt
- Datum: 06.08.2026
- Ursache: Teilupdate ohne konsistente Sheet-Datierung.
- Auswirkung: unklarer Gesamtstand.
- Korrektur: jedes Sheet aktualisieren oder Unverändertheit mit identischem Berichtsstand dokumentieren.
- Tests: TEST-008.

### ERR-005 – Quality Gate nur behauptet

- Status: offen
- Evidenzstatus: direkt belegt
- Datum: 06.08.2026
- Ursache: kein prüfbares Reviewprotokoll.
- Auswirkung: falscher Eindruck einer vollständigen Freigabe.
- Korrektur: Einwände, Änderungen und Final Approval dokumentieren.
- Tests: TEST-008.

### ERR-006 – Neu gefunden als Marktneuheit behandelt

- Status: ersetzt
- Evidenzstatus: mehrfach bestätigt
- Ursache: fehlender Zeitnachweis.
- Auswirkung: falsches Delta.
- Korrektur: `Unklar`, Baseline-Korrektur oder kein Delta.
- Tests: TEST-002, TEST-009.

### ERR-007 – Scope-Erweiterung als Marktbewegung interpretiert

- Status: ersetzt
- Evidenzstatus: direkt belegt
- Ursache: neue Kategorien fehlten im Altstand.
- Korrektur: Scope-Erweiterung separat kennzeichnen; nicht `Neu`.
- Tests: TEST-002.

### ERR-008 – Diagnosebegriffe als Verifikationssignal

- Status: ersetzt
- Evidenzstatus: mehrfach bestätigt
- Ursache: zu breite Terminologie und Marketingbegriffe.
- Korrektur: aktive/geführte Prüfung plus dokumentiertes Ergebnis verlangen.
- Tests: TEST-003, TEST-005.

### ERR-009 – Transitive Produkt-Tool-Zuordnung

- Status: ersetzt
- Evidenzstatus: direkt belegt
- Ursache: getrennte Produkt- und Toolseiten ohne direkten Kompatibilitätsnachweis.
- Korrektur: geschlossene offizielle Belegkette mit Ankerquelle.
- Tests: TEST-005.

### ERR-010 – Verifikationsbaseline unter 95 % positiv

- Status: offen
- Evidenzstatus: direkt belegt
- Ursache: Übernahme interner Decks als Baseline.
- Auswirkung: Konflikt mit Qualitätsstandard.
- Korrektur: provisorisch behandeln und offiziell nachbelegen; sonst final zurückstufen.
- Tests: TEST-003.

### ERR-011 – Inkonsistente Dateinamen

- Status: offen
- Evidenzstatus: mehrfach bestätigt
- Ursache: Leerzeichen, Unterstrich, Endung und Nummernzusätze variieren.
- Auswirkung: Routing- und Dateizugriffsfehler.
- Korrektur: kanonische Namen, Manifest, Routingtest.
- Tests: TEST-001, TEST-004.

### ERR-012 – Erst-/Update-Modus widersprüchlich

- Status: offen
- Evidenzstatus: historisch dokumentiert
- Ursache: ausführliche Master Prompts unterstützen beide Modi; kompakter Kandidat war Update-only.
- Auswirkung: unnötige Rückfragen oder falscher Startmodus.
- Korrektur: Produktivstrategie festlegen.
- Tests: TEST-006, TEST-007.

### ERR-013 – Copilot v1 zu streng

- Status: ersetzt
- Evidenzstatus: mehrfach bestätigt
- Ursache: optionale Abweichungen wurden zu Hard-Stops.
- Auswirkung: keine Excel-Ausgabe trotz verwertbarer Daten.
- Korrektur: v1.1 mit vier echten Blockern und Warnungs-/Fallbacklogik.
- Tests: TEST-010, TEST-011.

### ERR-014 – Englische Anfrage erzeugt deutsche Ausgabe

- Status: offen
- Evidenzstatus: mehrfach bestätigt
- Ursache: zentrale Sprachlogik fehlt; deutsche Knowledge-Dateien dominieren.
- Korrektur: VER-004, zentraler Sprachlayer und Regression.
- Tests: TEST-012.

### ERR-015 – Fachstatus und sichtbares Profil vermischt

- Status: ersetzt
- Evidenzstatus: direkt belegt
- Ursache: Tabellenaufgaben nicht klar getrennt.
- Korrektur: Farbe = Fachstatus; Text = belegtes Profil/Tool.
- Tests: TEST-002.

### ERR-016 – Nicht atomare Quellenzeilen

- Status: in Arbeit
- Evidenzstatus: direkt belegt
- Ursache: mehrere Produkte oder Messprinzipien zusammengefasst.
- Auswirkung: schlechte Prüfbarkeit und Copilot-Verarbeitung.
- Korrektur: eine Bewertungszeile pro Kombination.
- Tests: TEST-005, TEST-010.

### ERR-017 – Allgemeine Produktgruppenlinks

- Status: in Arbeit
- Evidenzstatus: mehrfach bestätigt
- Ursache: Recherche endete auf Hersteller- oder Portfolioebene.
- Auswirkung: Quelle bestätigt konkrete Aussage nicht eindeutig.
- Korrektur: Direktlink und konkrete Belegstelle; FILE-005.
- Tests: TEST-013.

### ERR-018 – Sicherheitslevel als Scheingenauigkeit

- Status: offen
- Evidenzstatus: direkt belegt
- Ursache: Prozentzahl ohne ausreichend dokumentierte Kriterien.
- Auswirkung: hohe Zahl trotz Quellen-/Zuordnungsfehler.
- Korrektur: evidenzbasierte Kriterien und unabhängige Quellenprüfung.
- Tests: TEST-008.

### ERR-019 – Business-Case-Zeitmodell widersprüchlich

- Status: offen
- Evidenzstatus: direkt belegt
- Datum: erkannt 31.08.2026 bei vollständiger Prüfung von FILE-020
- Ursache: Kadenz, Stunden je Lauf, Jahresstunden und monatliche Ersparnis wurden nicht auf eine gemeinsame Einheit und Formel normalisiert.
- Auswirkung: Kosten- und Zeitersparnis können nicht als finaler Entscheidungsnachweis verwendet werden.
- Korrektur: Referenzprozess, Läufe/Jahr, Stunden/Lauf, Reviewaufwand, Jahresstunden und Einsparung mit Formeln neu aufsetzen; alle Summen automatisiert gegenrechnen.
- Tests: TEST-014.

## Lessons Learned – Fachlogik

### LESSON-001 – Technologien strikt trennen
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: APL, PoE, PoDL und allgemeines Ethernet sind getrennte Bewertungsgegenstände.

### LESSON-002 – Profil ist nicht physische Schicht
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: PROFINET, Modbus TCP oder EtherNet/IP beweisen allein kein Ethernet-APL.

### LESSON-003 – PoE/PoDL separat ausgeben
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Sekundärmatrix verhindert falsche positive APL-Zellen.

### LESSON-004 – Diagnose und Verifikation definitorisch trennen
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: Diagnose/Monitoring sind Zusatznutzen, keine Verifikationsfreigabe.

### LESSON-005 – Produkt-/Variantenbezug entscheidet
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: allgemeine Herstellerfähigkeit reicht nicht für eine konkrete Matrixzelle.

### LESSON-006 – `keine Infos` ist oft korrekt
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: konservative Unklarheit ist besser als eine ungestützte positive oder negative Behauptung.

### LESSON-007 – Negativnachweis ist anspruchsvoll
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: `nicht vorhanden` erfordert ausdrückliche belastbare negative Evidenz.

## Lessons Learned – Quellen

### LESSON-008 – Direkte Primärquelle vor Portfolioseite
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: Quelle muss exakt die bewertete Produkt-/Technologiekombination stützen.

### LESSON-009 – Handbücher und Datenblätter sind häufig stärker
- Status: gültig
- Evidenzstatus: historisch dokumentiert
- Erkenntnis: technische Dokumentation liefert präzisere Varianten- und Funktionsnachweise als Marketingseiten.

### LESSON-010 – Seriös bedeutet nicht passend
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: Auch eine offizielle Quelle kann für die konkrete Behauptung zu allgemein sein.

### LESSON-011 – Snippets und benachbarte PDF-Blöcke sind riskant
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Textnähe ist keine Produktzuordnung; relevante Seite visuell prüfen.

### LESSON-012 – Fachmedien primär zur Discovery
- Status: gültig
- Evidenzstatus: historisch dokumentiert
- Erkenntnis: Fachartikel helfen beim Finden, positive Freigabe benötigt möglichst Herstellerbeleg.

### LESSON-013 – Veröffentlichungs- und Abrufdatum trennen
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: aktueller Fund ist nicht automatisch aktuelle Veröffentlichung.

### LESSON-014 – Neuer Link ist nicht automatisch Delta
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: bestätigt ein neuer Link nur den alten Status, entsteht kein Change-Log-Eintrag.

## Lessons Learned – Delta

### LESSON-015 – Neu gefunden ist nicht neu veröffentlicht
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: `Neu` braucht Zeitnachweis im Update-Zeitraum.

### LESSON-016 – Scope-Erweiterung ist keine Marktneuheit
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: neue Spalten oder Unternehmen werden separat gekennzeichnet.

### LESSON-017 – Baseline-Korrektur ist keine Marktneuheit
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: alter Fehler wird korrigiert, nicht als neue Marktentwicklung verkauft.

## Lessons Learned – Prompt und Architektur

### LESSON-018 – Modular schlägt Mega-Prompt
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: Verantwortlichkeiten getrennt halten und nur relevante Knowledge-Dateien laden.

### LESSON-019 – System Prompt bleibt global
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Systemsteuerung soll keine vollständige Fachmethodik duplizieren.

### LESSON-020 – Routing enthält Zuordnung und Fallback
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: fehlender Master Prompt darf nicht durch Modellwissen ersetzt werden.

### LESSON-021 – Master Prompt besitzt den Fachvertrag
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Status, Delta, Quellen, QG und Ausgabe gehören in den Fachmaster.

### LESSON-022 – Baseline enthält Zustand, keine Regeln
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: Baseline kann fehlerhaft sein und wird nach aktuellen Belegen korrigiert.

### LESSON-023 – Dateinamen sind Architektur
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: exakte Namen und verfügbare Dateien gehören zum Preflight.

### LESSON-024 – Prompt braucht Regression, nicht nur Plausibilität
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: sprachlich guter Prompt kann funktional zu streng oder sprachlich falsch reagieren.

## Lessons Learned – Quality Gate

### LESSON-025 – Rollennamen allein erhöhen Qualität nicht
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Reviewer müssen konkrete Zellen, Quellen und Deltas prüfen.

### LESSON-026 – Einwände müssen zellbezogen sein
- Status: gültig
- Evidenzstatus: historisch dokumentiert
- Erkenntnis: konkrete Belegstelle und Korrektur sind wichtiger als allgemeine Bestätigung.

### LESSON-027 – Einwände dokumentieren
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: ohne protokollierte Einwände ist das QG nicht nachvollziehbar.

### LESSON-028 – Korrekturen durch alle Outputs propagieren
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: Matrix, Quelle, Delta und Summary müssen denselben korrigierten Stand zeigen.

### LESSON-029 – Final Approval ausdrücklich protokollieren
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Chairman-/Final-Gate-Freigabe darf nicht nur behauptet werden.

### LESSON-030 – Prozentzahl ersetzt keine Quellenprüfung
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: 98 % können bei falscher Produktzuordnung trotzdem falsch sein.

## Lessons Learned – Hybrid/Copilot

### LESSON-031 – Recherche und Excel sind getrennte Aufgaben
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: fachliche Bewertung bleibt bei ChatGPT, technische Übertragung bei Copilot.

### LESSON-032 – ChatGPT bleibt Research Engine
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: quellenkritisches Reasoning darf im Hybrid nicht an Copilot Basic delegiert werden.

### LESSON-033 – Copilot Basic als Excel-Umsetzer testen
- Status: gültig
- Evidenzstatus: historisch dokumentiert
- Erkenntnis: seine Stärke liegt im dateibasierten M365-/Excel-Schritt.

### LESSON-034 – Copilot darf keine Fakten ergänzen
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: fehlende Felder bleiben leer oder werden gewarnt.

### LESSON-035 – Überstrenger Preflight blockiert Nutzen
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: technische Blocker und fachliche Warnungen trennen.

### LESSON-036 – Warnungen statt unnötiger Hard-Stops
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: nichtkritische Auffälligkeiten dürfen die Datei-Erzeugung nicht stoppen.

### LESSON-037 – Evidence-Markdown ist die Schnittstelle
- Status: gültig
- Evidenzstatus: mehrfach bestätigt
- Erkenntnis: strukturierte, freigegebene Daten sind wichtiger als freie Übergabetexte.

### LESSON-038 – Deterministische Validierung wäre stärker
- Status: zu prüfen
- Evidenzstatus: abgeleitet
- Erkenntnis: JSON-Schema und Validator könnten langfristig Prompt-Selbstauskunft ergänzen.

## Lessons Learned – Sprache

### LESSON-039 – Anfragesprache allein reicht nicht
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: deutsche Knowledge-Dateien können die Ausgabe trotz englischer Frage dominieren.

### LESSON-040 – Sprache als globale Variable setzen
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: eine Sprachentscheidung pro Auftrag verhindert Mischsprache.

### LESSON-041 – Übersetzung erzeugt kein Delta
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Fachstatus vor dem Vergleich sprachneutral normalisieren.

### LESSON-042 – Baselines historisch unverändert lassen
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Präsentationssprache darf den alten Vergleichsstand nicht überschreiben.

### LESSON-043 – DE und EN müssen fachlich identisch sein
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: gleiche Quellen, Status, Deltas und Sicherheitslevel in beiden Sprachen.

## Lessons Learned – Business Case

### LESSON-044 – Zeitgrößen vor Kostenrechnung normalisieren
- Status: gültig
- Evidenzstatus: direkt belegt
- Erkenntnis: Recherchekadenz, Stunden je Lauf, Stunden je Monat und Stunden je Jahr müssen auf einer gemeinsamen Formel beruhen; erst danach dürfen Ersparnis und Break-even berechnet werden.
