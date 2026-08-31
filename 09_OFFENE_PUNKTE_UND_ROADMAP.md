# Offene Punkte und Roadmap

**Stand:** 31.08.2026  
**Status:** in Arbeit  
**Pflegeregel:** Jeder offene Punkt erhält eine unveränderliche ID, Priorität, Abnahmekriterium und nächste Handlung. Nach Abschluss bleibt der Eintrag erhalten und wird auf `gültig`, `verworfen` oder `archiviert` gesetzt.

## Prioritätslogik

- **P0:** blockiert einen belastbaren produktiven Durchlauf oder kann wesentliche Falschaussagen verursachen.
- **P1:** für Release, Skalierung oder stabile Nutzung erforderlich.
- **P2:** verbessert Wartbarkeit, Komfort oder Erweiterbarkeit, blockiert den Kernbetrieb aber nicht unmittelbar.

## P0 – Vor produktiver Freigabe

### OPEN-003 – Quellenoptimierten APL-Master produktiv zuordnen

- Status: offen
- Priorität: P0
- Evidenzstatus: direkt belegt
- Problem: FILE-005 ist jünger und strenger als FILE-004; eine ausdrückliche Produktivfreigabe und Routing-Zuordnung ist nicht dokumentiert.
- Risiko: unterschiedliche APL-Ergebnisse je verwendeter Master-Prompt-Datei.
- Abhängigkeiten: OPEN-006; OPEN-013.
- Nächste Handlung: FILE-004 und FILE-005 fachlich diffen, gewünschte Produktionsfassung festlegen und FILE-003 aktualisieren.
- Abnahmekriterium: genau eine als produktiv gekennzeichnete APL-Fassung; alte Fassung mit Status `ersetzt` und Verweis.
- Verknüpfungen: DEC-009; DEC-021; TEST-013.

### OPEN-004 – Hybrid mit Copilot v1.1 End-to-End abnehmen

- Status: offen
- Priorität: P0
- Evidenzstatus: historisch dokumentiert
- Problem: v1 war zu streng; v1.1 liegt vor, aber ein kompletter Lauf vom freigegebenen Markdown bis zur geprüften Excel-Datei ist nicht belegt.
- Risiko: unbrauchbare Datei, unerwartete Hard Stops oder fachliche Veränderung bei der Übertragung.
- Abhängigkeiten: OPEN-006; OPEN-013.
- Nächste Handlung: Referenz-Markdown aus RUN-007 mit FILE-015 verarbeiten und Zellen, Farben, Links, Warnungen und Fallbacks prüfen.
- Abnahmekriterium: reproduzierbare Excel-Ausgabe ohne fachliche Umdeutung; nur technische Hard Stops; dokumentiertes Testprotokoll bestanden.
- Verknüpfungen: DEC-016; DEC-017; TEST-010; TEST-011; ERR-013.

### OPEN-005 – Bilinguale 2.1-Migration abschließen

- Status: in Arbeit
- Priorität: P0
- Evidenzstatus: direkt belegt
- Problem: ein englischer System Prompt liegt vor, Routing, Fachprompts, Mapping und Regression sind nicht vollständig migriert.
- Risiko: Ausgabe bleibt deutsch oder Fachbedeutungen driften zwischen DE und EN.
- Abhängigkeiten: OPEN-002; OPEN-006.
- Nächste Handlung: zentrale Sprachressource erstellen, FILE-003, FILE-005 und FILE-006 migrieren und denselben Testkorpus zweisprachig ausführen.
- Abnahmekriterium: fachlich identische DE-/EN-Ergebnisse, kanonische Statuswerte, keine sprachbedingten Deltas, TEST-012 bestanden.
- Verknüpfungen: DEC-018 bis DEC-020; FILE-002; FILE-009; TEST-012; ERR-014.

### OPEN-008 – Verifikationsbaseline auf 6+1-Sheet-Vertrag migrieren

- Status: offen
- Priorität: P0
- Evidenzstatus: direkt belegt
- Problem: FILE-006 verlangt sechs Pflicht-Sheets plus optionale Summary; FILE-008 besitzt fünf Sheets und bildet Vorher/Nachher nicht ab.
- Risiko: unvollständiger Datenvertrag, falsche Deltaquelle und nicht prüfbare Freigabe.
- Abhängigkeiten: OPEN-006; OPEN-009; OPEN-013.
- Nächste Handlung: Baseline-Migrationsregeln definieren, Kandidaten in Vorher-Sheets übernehmen, Nachher-Sheets leer beziehungsweise QG-konform erzeugen und E2E testen.
- Abnahmekriterium: strukturell valide Baseline mit sechs Pflicht-Sheets; Delta und Summary ausschließlich aus Nachher-Sheets; dokumentierter Regressionstest.
- Verknüpfungen: DEC-014; FILE-006; FILE-008; TEST-003 bis TEST-005.

### OPEN-009 – Ergebnis des Verifikationsupdates vom 27.08. klären

- Status: zu prüfen
- Priorität: P0
- Evidenzstatus: historisch dokumentiert
- Problem: Auftrag und Zeitraum sind belegt, eine finale Ergebnisdatei ist im verfügbaren Korpus nicht vorhanden.
- Risiko: unbelegte Annahme eines erfolgreichen oder fehlgeschlagenen Laufs.
- Abhängigkeiten: OPEN-008.
- Nächste Handlung: Ergebnisdatei oder Chatprotokoll beschaffen; falls nicht vorhanden, Lauf mit FILE-006 reproduzieren.
- Abnahmekriterium: Ergebnis und Freigabestatus sind mit Datei/Testnachweis dokumentiert oder RUN-009 ist ausdrücklich als nicht ausgeführt abgeschlossen.
- Verknüpfungen: RUN-009.

### OPEN-010 – Verifikationsbaseline offiziell nachbelegen

- Status: offen
- Priorität: P0
- Evidenzstatus: direkt belegt
- Problem: FILE-008 enthält positive Kandidaten auf Basis interner Sekundärquellen und Sicherheitslevel unter 95 %.
- Risiko: Diagnose- oder Marketingaussagen werden fälschlich als Geräteverifikation gewertet.
- Abhängigkeiten: OPEN-008; OPEN-013.
- Nächste Handlung: jede positive Kandidatenzelle gegen direkte Herstellerquelle und DEC-011 prüfen.
- Abnahmekriterium: jede freigegebene positive Nachher-Zelle besitzt atomare offizielle Evidenz und mindestens 95 % Sicherheit; sonst `keine Infos`.
- Verknüpfungen: DEC-010 bis DEC-014; ERR-008 bis ERR-010.

### OPEN-013 – Quality-Gate-Verantwortung und Nachweis festlegen

- Status: offen
- Priorität: P0
- Evidenzstatus: mehrfach bestätigt
- Problem: der vierstufige Prozess ist definiert, aber Rolleninhaber, Chairman-/Final-Approval-Verantwortung und verbindliches Protokollformat sind nicht final festgelegt.
- Risiko: Quality Gate wird behauptet, ohne dass Einwände, Korrekturen und Freigabe nachweisbar sind.
- Abhängigkeiten: keine.
- Nächste Handlung: Rollenmatrix, Mindestprotokoll und Freigabesignale durch den Nutzer beziehungsweise Prozessverantwortlichen bestätigen lassen.
- Abnahmekriterium: benannte Verantwortlichkeiten und ein ausgefülltes, versioniertes QG-Protokoll je produktivem Lauf.
- Verknüpfungen: DEC-013; ERR-005; FILE-012.

## P1 – Release und stabile Nutzung

### OPEN-001 – Erst-Recherche versus Update-only final entscheiden

- Status: offen
- Priorität: P1
- Evidenzstatus: historisch dokumentiert
- Problem: Update mit Baseline ist Standard; ob die Produktivlösung weiterhin Erst-Recherche unterstützt, ist nicht abschließend entschieden.
- Risiko: unklare Preflight- und Routinglogik bei neuen Themen.
- Abhängigkeiten: OPEN-016.
- Nächste Handlung: Zielgruppenfälle erfassen und einen der Modi `Update-only` oder `Erst + Update` freigeben.
- Abnahmekriterium: System Prompt, Routing und Vorlagen verwenden dieselbe Modusregel; Erstmodus besitzt eigene Abnahmetests oder ist ausdrücklich ausgeschlossen.
- Verknüpfungen: DEC-003; DEC-004.

### OPEN-002 – Lange oder kompakte System-Prompt-Fassung festlegen

- Status: offen
- Priorität: P1
- Evidenzstatus: historisch dokumentiert
- Problem: lange, kompakte und englische Fassungen existieren; alleinige Produktionsfassung beziehungsweise Rollen sind nicht eindeutig festgelegt.
- Risiko: Regelverlust oder Versionsdrift.
- Abhängigkeiten: OPEN-005.
- Nächste Handlung: Funktionsumfang und Regression vergleichen; Produktiv-, Hybrid- und Archivrollen zuweisen.
- Abnahmekriterium: jede System-Prompt-Datei besitzt eindeutigen Status, Zielumgebung und Nachfolger/Quelle.
- Verknüpfungen: VER-002 bis VER-004; FILE-001; FILE-002; FILE-009.

### OPEN-006 – Kanonische Datei- und Sheetnamen vereinheitlichen

- Status: offen
- Priorität: P1
- Evidenzstatus: direkt belegt
- Problem: Dateinamen und erwartete Sheetstrukturen unterscheiden sich zwischen Generationen und Fachbereichen.
- Risiko: falsches Routing, gescheiterte Übergabe und fragile Automatisierung.
- Abhängigkeiten: OPEN-002; OPEN-003; OPEN-008.
- Nächste Handlung: Manifest mit kanonischem Namen, Alias, Version, Status, Sprache und Schema erstellen.
- Abnahmekriterium: alle aktiven Dateien und Sheets sind im Manifest eindeutig; Prompts referenzieren nur kanonische Namen.
- Verknüpfungen: FILE-001 bis FILE-023; LESSON-018.

### OPEN-007 – Formale Confidence-Kriterien definieren

- Status: offen
- Priorität: P1
- Evidenzstatus: abgeleitet
- Problem: die 95-%-Schwelle ist verbindlich, die Berechnung und Prüfkriterien sind noch überwiegend qualitativ.
- Risiko: gleiche Evidenz erhält zwischen Durchläufen unterschiedliche Sicherheitslevel.
- Abhängigkeiten: OPEN-013.
- Nächste Handlung: Bewertungsrubrik für Direktheit, Produktnähe, Aktualität, Variantenbezug, Widersprüche und Negativnachweis erstellen.
- Abnahmekriterium: zwei Prüfer beziehungsweise zwei kontrollierte Durchläufe bewerten denselben Gold-Standard-Korpus innerhalb definierter Toleranz gleich.
- Verknüpfungen: DEC-010; ERR-010; LESSON-027.

### OPEN-011 – Finale Lizenzentscheidung treffen

- Status: offen
- Priorität: P1
- Evidenzstatus: historisch dokumentiert
- Problem: der praktische Basic-Hybrid ist beschlossen; eine finale organisatorische Wahl zwischen verfügbaren ChatGPT-/Copilot-Lizenzen fehlt.
- Risiko: Kostenentscheidung ohne nachgewiesenen Prozessmehrwert oder unzureichende Funktionen.
- Abhängigkeiten: OPEN-004; OPEN-012.
- Nächste Handlung: aktuelle Tarife/Funktionen verifizieren und anhand dreier Pilotzyklen Gesamtkosten pro freigegebenem Lauf vergleichen.
- Abnahmekriterium: dokumentierte Entscheidung mit aktuellem Preisstand, Nutzerzahl, benötigten Funktionen und Sensitivität.
- Verknüpfungen: DEC-022; 08_BUSINESS_CASE_UND_VALUE.md.

### OPEN-012 – Gold-Standard-Modell auswählen

- Status: offen
- Priorität: P1
- Evidenzstatus: historisch dokumentiert
- Problem: GPT-5.6 Sol versus Thinking wurde als Option diskutiert, aber nicht entschieden.
- Risiko: Modellwahl nach Eindruck statt reproduzierbarem Qualitäts-/Kostenvergleich.
- Abhängigkeiten: OPEN-007; OPEN-013.
- Nächste Handlung: identischen Gold-Standard-Korpus mit gleichen Prompts, Quellen und Abnahmekriterien vergleichen.
- Abnahmekriterium: dokumentierter Vergleich von Quellenrichtigkeit, Fehlklassifikation, Reproduzierbarkeit, Laufzeit und Kosten; freigegebene Standard- und Fallbackwahl.
- Verknüpfungen: TEST-001 bis TEST-013.

### OPEN-014 – Grenzen von Updateintervallen verbindlich definieren

- Status: offen
- Priorität: P1
- Evidenzstatus: abgeleitet
- Problem: bei historischen Läufen waren Start-/Endgrenzen und Baseline-Datum teilweise inkonsistent.
- Risiko: ein Fund wird fälschlich als `Neu` eingestuft oder übersehen.
- Abhängigkeiten: OPEN-006.
- Nächste Handlung: inklusive/exklusive Datumsregel, Umgang mit undatierten Seiten und Abruf-/Veröffentlichungsdatum definieren.
- Abnahmekriterium: Grenzfalltests bestehen; Delta-Klassifikation ist bei identischen Daten reproduzierbar.
- Verknüpfungen: DEC-004; DEC-008; TEST-007 bis TEST-009; ERR-003.

### OPEN-015 – Atomisierung bei gemischter Evidenz spezifizieren

- Status: offen
- Priorität: P1
- Evidenzstatus: mehrfach bestätigt
- Problem: eine Quelle kann mehrere Produkte oder Varianten enthalten; fehlende Evidenz für eine Kombination darf andere Zeilen nicht kontaminieren.
- Risiko: falsche Übertragung benachbarter Produktblöcke oder pauschales `keine Infos`.
- Abhängigkeiten: OPEN-003; OPEN-007.
- Nächste Handlung: verbindliche Produkt–Variante–Messprinzip–Technologie-Schlüssel und Konfliktfälle im Testkorpus definieren.
- Abnahmekriterium: H250-/OPTIMASS- und vergleichbare Nachbarschaftstests ergeben korrekte getrennte Bewertungen.
- Verknüpfungen: DEC-009; ERR-001; ERR-016; LESSON-009 bis LESSON-012.

## P2 – Skalierung und Wartbarkeit

### OPEN-016 – Nächste Recherchebereiche priorisieren

- Status: offen
- Priorität: P2
- Evidenzstatus: historisch dokumentiert
- Problem: die Architektur ist erweiterbar, aber nächste Technologien beziehungsweise Märkte sind nicht priorisiert.
- Risiko: parallele Erweiterung ohne Nutzenhypothese und Baseline.
- Abhängigkeiten: OPEN-001; OPEN-011.
- Nächste Handlung: Kandidaten nach Geschäftsrelevanz, Updatefrequenz, Quellenlage und Wiederholungsaufwand bewerten.
- Abnahmekriterium: priorisierte Liste; für den nächsten Bereich existieren Owner, Route, Fachdefinition, Baseline/Erstmodus und Testplan.
- Verknüpfungen: DEC-001; DEC-002.

### OPEN-017 – Maschinenlesbaren Vertrag und Validator einführen

- Status: offen
- Priorität: P2
- Evidenzstatus: abgeleitet
- Problem: Konsistenzregeln werden heute überwiegend durch Prompt und manuelle Prüfung erzwungen.
- Risiko: IDs, Statuswerte, Quellenfelder, Dateinamen und Sheets driften.
- Abhängigkeiten: OPEN-006 bis OPEN-008.
- Nächste Handlung: Schema für Research-Evidence und Prüfskript für IDs, Statuswerte, Links, Pflichtfelder und Workbook-Struktur entwerfen.
- Abnahmekriterium: Validator erkennt bekannte Fehler aus ERR-001 bis ERR-018 und läuft vor jedem Release.
- Verknüpfungen: DEC-023; README_PFLEGEANLEITUNG.md.

### OPEN-018 – Monetären Business Case konsistent neu freigeben

- Status: offen
- Priorität: P1
- Evidenzstatus: direkt belegt
- Problem: FILE-020 enthält einen nachvollziehbaren frühen Kostenvergleich, aber widersprüchliche Zeitgrößen; die spätere Annahme von 44 Stunden/Jahr ist ebenfalls noch nicht durch echte Pilotmessung bestätigt.
- Risiko: Investitions- oder Lizenzentscheidung auf Basis rechnerisch beziehungsweise zeitlich unklarer Annahmen.
- Abhängigkeiten: OPEN-004; OPEN-011; OPEN-012.
- Nächste Handlung: Referenzprozess und Formeln neu aufsetzen, aktuelle Tarife verifizieren und mindestens drei Pilotzyklen messen.
- Abnahmekriterium: alle Zeit- und Kosteneinheiten sind konsistent; Formeln sind reproduzierbar; aktueller Preisstand und Sensitivität dokumentiert; Entscheiderfreigabe liegt vor.
- Verknüpfungen: FILE-020; TEST-014; ERR-019; LESSON-044; 08_BUSINESS_CASE_UND_VALUE.md.

## Roadmap

| Phase | Ziel | Enthaltene offene Punkte | Exit-Kriterium |
|---|---|---|---|
| A – Governance sichern | Freigabe und aktuelle Wahrheit eindeutig machen | OPEN-003, OPEN-013 | produktiver APL-Master und QG-Verantwortung bestätigt |
| B – Kernworkflows abnehmen | Hybrid und Verifikation reproduzierbar ausführen | OPEN-004, OPEN-008, OPEN-009, OPEN-010 | beide Fachworkflows besitzen bestandenen E2E-Test |
| C – 2.1 stabilisieren | gemeinsame DE/EN-Architektur fertigstellen | OPEN-002, OPEN-005, OPEN-006, OPEN-014, OPEN-015 | Regression in DE und EN bestanden |
| D – Betrieb entscheiden | Modell, Lizenz und Messmodell freigeben | OPEN-001, OPEN-007, OPEN-011, OPEN-012, OPEN-018 | dokumentierte Betriebsentscheidung und Pilot-KPIs |
| E – Skalieren | weitere Bereiche und Validator ergänzen | OPEN-016, OPEN-017 | nächster Bereich integriert; automatische Vorprüfung aktiv |

## Empfohlene unmittelbare Reihenfolge

1. OPEN-013 – Verantwortlichkeit und QG-Nachweis klären.
2. OPEN-003 – genau einen APL-Produktionsmaster festlegen.
3. OPEN-004 – Copilot-v1.1-Hybrid mit RUN-007 end-to-end testen.
4. OPEN-008 und OPEN-010 – Verifikationsbaseline migrieren und offiziell nachbelegen.
5. OPEN-005 – bilinguale 2.1-Migration mit Regression abschließen.
