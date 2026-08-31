# Glossar und verbindliches Regelwerk

**Stand:** 31.08.2026  
**Status:** gültig

## 1. Projektbegriffe

| Begriff | Verbindliche Bedeutung |
|---|---|
| Baseline | dokumentierter alter Recherche- und Bewertungsstand; Vergleichsbasis, nicht automatisch Wahrheit |
| Preflight | Eingangskontrolle von Route, Dateien, Zeitraum, Scope und technischer Lesbarkeit |
| Fallback | konservatives Verhalten bei fehlenden oder unklaren Eingaben; keine improvisierte Fachlogik |
| Routing Index | Wegweiser zum passenden Master Prompt und zur Baseline |
| Master Prompt | verbindliche Fach-, Bewertungs-, Quellen-, Quality-Gate- und Ausgabelogik eines Recherchebereichs |
| Update-Recherche | Vergleich einer Baseline mit dem aktuellen belastbar recherchierten Stand |
| Erst-Recherche | vollständige Recherche ohne alte Baseline; Delta nur bei definiertem Startpunkt |
| Delta | relevante Änderung gegenüber der Baseline |
| Baseline-Korrektur | Korrektur eines alten Fehlers oder einer alten Lücke; keine automatische Marktneuheit |
| Scope-Erweiterung | zusätzliche Unternehmen oder Kategorien; keine automatische Marktneuheit |
| atomare Evidenz | eine eindeutig zuordenbare Bewertungszeile pro Unternehmen × Messprinzip × Technologie/Tool |
| Ankerquelle | direkte offizielle Quelle, die die zentrale Produkt-Technologie- oder Produkt-Tool-Verbindung belegt |
| Sicherheitslevel | dokumentierte Einschätzung der Belastbarkeit einer konkreten Aussage; kein Ersatz für Quellenprüfung |
| Quality Gate | mehrstufige Prüfung von Evidenz, Status, Delta und Nutzbarkeit vor Freigabe |
| Evidence-Markdown | fachlich freigegebene strukturierte Schnittstelle zwischen ChatGPT-Recherche und Copilot-Excel-Erzeugung |

## 2. Technologische Abgrenzung

### Ethernet-APL

Ethernet-APL ist die zentrale bewertete Technologie der Hauptmatrix. Ein positiver Status ist nur zulässig, wenn Ethernet-APL für das konkrete Produkt oder eine eindeutig abgegrenzte Variante ausdrücklich und belastbar belegt ist.

### PoE und PoDL

Power over Ethernet und Power over Data Line werden separat bewertet. Ein PoE- oder PoDL-Nachweis ist kein Ethernet-APL-Nachweis.

### Kommunikationsprofile

PROFINET, Modbus TCP, EtherNet/IP, OPC UA, Ethernet TCP/IP oder allgemeines Industrial Ethernet sind Kommunikationsprofile beziehungsweise Ethernet-basierte Schnittstellen. Sie sind nicht automatisch Ethernet-APL.

**Harte Regel:** Ein Kommunikationsprofil, PoE oder PoDL darf nicht zu `verfügbar` in der Ethernet-APL-Hauptmatrix führen. Das Profil darf nur als sichtbarer Zellwert einer positiven Zelle erscheinen, wenn Ethernet-APL zusätzlich ausdrücklich belegt ist.

## 3. Verifikation und benachbarte Funktionen

### Verifikation

Verifikation ist im Projekt eine aktiv initiierte oder geführte Prüfung eines konkreten Messgeräts gegen einen Referenzzustand oder eine definierte Prüflogik mit dokumentiertem Ergebnis, beispielsweise:

- Pass/Fail,
- Prüfprotokoll,
- Report,
- Zertifikat.

### Diagnose

Diagnose erkennt oder klassifiziert Gerätezustände und Fehler. Diagnose allein ist kein Ersatz für Verifikation und kein Verifikationsnachweis.

### Condition Monitoring und Predictive Maintenance

Trend- und Zustandsüberwachung können wertvolle Zusatzinformationen liefern, sind aber kein Verifikationsnachweis.

### Kalibrierung

Kalibrierung, Rekalibrierung oder Calibration Check sind nicht automatisch Verifikation. Eine offiziell belegte Anerkennung einer Verifikation zur Verlängerung von Rekalibrationsintervallen wird als Kriterieninformation erfasst, nicht als alleiniger Statusnachweis.

### Marketingbegriffe

`Health Check`, `Smart Diagnostics`, `Asset Health` und ähnliche Begriffe sind ohne Funktionsbeschreibung, aktive Auslösung, Produktbezug und dokumentiertes Ergebnis kein Verifikationsnachweis.

## 4. Direkte Belegkette Verifikation

Für final `verfügbar` müssen mindestens verbunden sein:

1. Unternehmen,
2. konkretes Produkt oder klar abgegrenzte Gerätefamilie,
3. Messprinzip,
4. konkretes Tool, Verifikationsmodus oder Funktion,
5. direkte Produkt-Tool-Verbindung,
6. aktive oder geführte Prüfung,
7. Referenzbedingung oder definierte Prüflogik,
8. dokumentiertes Prüfergebnis.

Unzulässig ist die transitive Annahme: Hersteller bietet Produkt X und Tool Y an, daher funktioniert Y mit X.

## 5. Statuswerte Ethernet-APL

| Status | Bedeutung |
|---|---|
| `verfügbar` | konkreter Ethernet-APL-Nachweis für mindestens ein Produkt des Messprinzips |
| `in Planung` | belastbare offizielle Ankündigung oder Roadmap |
| `keine Infos` | kein ausreichend belastbarer positiver oder negativer Nachweis |
| `nicht vorhanden` | ausdrücklicher belastbarer Negativnachweis |

## 6. Werte PoE-/PoDL-Matrix

- `PoE`
- `PoDL`
- `PoE + PoDL`
- `in Planung`
- `keine Infos`
- `nicht vorhanden`

Farblogik:

- Grün = PoE
- Blau = PoDL
- Türkis = PoE + PoDL
- Gelb = in Planung
- Grau = keine Infos
- Rot = nicht vorhanden

## 7. Status Verifikation

Die finale Verifikationsmatrix verwendet:

- `verfügbar`
- `in Planung`
- `keine Infos`
- `nicht vorhanden`

Der sichtbare Zellwert zeigt das belegte Tool oder die Funktion. Externe Tools erhalten den Zusatz `(extern)`.

Im aktuellen Master Prompt gelten Vorher-Sheets als Kandidatenraum. Eine vorläufig grüne Zelle ist keine finale Freigabe. Nur das Nachher-Sheet nach dokumentiertem Quality Gate ist fachlich maßgeblich.

## 8. Delta-Logik

Verbindliche Werte:

| Delta | Bedeutung |
|---|---|
| `Neu` | neue Marktverfügbarkeit oder neue belegte Funktion mit Zeitnachweis im Update-Zeitraum |
| `Geändert` | relevanter Status-, Produkt-, Profil-, Funktions- oder Kriterienwechsel |
| `Entfernt / abgekündigt` | belastbar entfernte oder abgekündigte Lösung |
| `Unklar` | Unterschied vorhanden, aber zeitliche oder fachliche Einordnung nicht belastbar |

`Unverändert` ist im Delta- und Change-Log verboten. Unveränderte Einträge werden geprüft, aber nicht ausgegeben.

### Abgrenzungen

- Neu gefunden ≠ neu veröffentlicht.
- Scope-Erweiterung ≠ Marktneuheit.
- Baseline-Korrektur ≠ Marktneuheit.
- Neuer Link ohne Statusänderung ≠ Delta.
- Vorläufiger Verifikationskandidat ≠ Delta; maßgeblich sind die finalen Nachher-Ergebnisse.

## 9. Zeitregeln

- Letzter Abruf definiert den Start des Update-Zeitraums.
- Aktueller Abruf definiert den Berichtsstand.
- Veröffentlichungs-/Dokumentdatum und Abrufdatum sind getrennt zu dokumentieren.
- `Neu` benötigt einen belastbaren zeitlichen Nachweis innerhalb des betrachteten Intervalls.
- Ist der alte Vergleichsstand fachlich älter oder jünger als der vom Nutzer genannte letzte Abruf, muss die Abweichung sichtbar dokumentiert werden.
- Die inklusive oder exklusive Behandlung der Intervallgrenzen ist als offene Governance-Entscheidung markiert.

## 10. Quellenpriorität

1. offizielle produkt- oder variantenspezifische Herstellerquelle,
2. offizielles Datenblatt, Handbuch oder technische Dokumentation,
3. offizielle Pressemitteilung,
4. offizielle Broschüre oder Katalog,
5. offizielle Zertifizierungs-, Partner- oder Technologieseite,
6. seriöse Fachpublikation ergänzend,
7. weitere Drittquellen nur zur Discovery oder als gekennzeichnete Ergänzung.

Eine seriöse Quelle kann trotzdem ungeeignet sein, wenn sie nicht exakt die behauptete Kombination belegt.

## 11. Belegstellenregeln

- Direktlink statt allgemeiner Start- oder Produktgruppenseite.
- Produkt, Variante, Messprinzip und Technologie müssen eindeutig zugeordnet sein.
- Bei PDFs relevante Seite und Produktblock visuell prüfen.
- Textnähe in einem mehrspaltigen PDF ist keine sichere Zuordnung.
- Snippets dienen zur Discovery, nicht allein zur Freigabe.
- Mehrere Messprinzipien oder Produkte nicht in einer Quellenzeile zusammenfassen, wenn sie getrennt bewertet werden.
- Abgelehnte Quellen und Suchlücken bei kritischen Fällen dokumentieren.

## 12. Sicherheits- und Negativlogik

- Unter 95 % Sicherheit darf eine materielle Aussage nicht als bestätigter Fakt erscheinen.
- Hohe Prozentwerte dürfen keine schwache oder falsch zugeordnete Quelle überdecken.
- `keine Infos` bedeutet unzureichende Evidenz, nicht nachgewiesene Abwesenheit.
- `nicht vorhanden` verlangt direkte negative Evidenz.
- Verifikationsbaseline-Einträge unter 95 % bleiben Kandidaten beziehungsweise werden final zurückgestuft, bis offizielle Evidenz vorliegt.

## 13. Quality Gate

### Phase 1 – Research

Kandidaten, Produkte, Quellen, Status, Deltas und Sicherheitslevel sammeln.

### Phase 2 – Quality Review

Jede relevante Bewertung kritisch prüfen:

- Belegt die Quelle exakt die Aussage?
- Ist das Messprinzip korrekt?
- Wurden ähnliche Technologien vermischt?
- Ist der Negativnachweis ausreichend?
- Ist das Delta zeitlich belegt?
- Ist das Sicherheitslevel realistisch?

### Phase 3 – Advisor Review

Prüfung auf Fehler/Überinterpretation, First-Principles-Evidenz, übersehene Marktchancen, Verständlichkeit und interne Nutzbarkeit.

### Phase 4 – Final Approval

Status, Delta, Quellen, Sicherheitslevel und Schlussfolgerungen bestätigen, korrigieren oder konservativ zurückstufen.

**Governance-Regel:** Ein Quality Gate gilt nur als durchgeführt, wenn Einwände, Korrekturen und Freigabe nachvollziehbar dokumentiert sind.

## 14. Excel-Regeln

### Ethernet-APL

Fünf Sheets:

1. Ethernet-APL Matrix
2. PoE-PoDL Matrix
3. Quellenverzeichnis
4. Delta- und Change-Log
5. optional beziehungsweise üblich Management Summary

### Verifikation – aktueller Zielvertrag

1. Verifikation – vor QG
2. Verifikation – nach QG
3. Kriterien – vor QG
4. Kriterien – nach QG
5. Quellenverzeichnis
6. Delta- und Change-Log
7. optional Management Summary

Vorher- und Nachher-Sheets müssen strukturell direkt vergleichbar bleiben. Das Quality Gate darf Vorher-Kandidaten nicht rückwirkend löschen.

## 15. Sprachregeln DE/EN

- ausdrückliche Sprachvorgabe des Nutzers hat Vorrang,
- sonst folgt die Ausgabe der Sprache der aktuellen Aufgabe,
- frühere Chat-, Knowledge- oder Baseline-Sprache entscheidet nicht automatisch,
- Sprache wird einmal pro Auftrag festgelegt,
- Fachstatus wird intern sprachneutral behandelt,
- Übersetzung erzeugt kein Delta,
- Produktnamen, Normen, Protokolle und offizielle Quellentitel werden nicht unnötig übersetzt,
- DE und EN müssen denselben fachlichen Stand, dieselben Quellen, Deltas und Sicherheitslevel besitzen.

### Kanonisches Mapping

| Intern | Deutsch | Englisch |
|---|---|---|
| `AVAILABLE` | verfügbar | available |
| `PLANNED` | in Planung | planned |
| `NO_INFORMATION` | keine Infos | no information |
| `NOT_AVAILABLE` | nicht vorhanden | not available |
| `NEW` | Neu | New |
| `CHANGED` | Geändert | Changed |
| `REMOVED_DISCONTINUED` | Entfernt / abgekündigt | Removed / discontinued |
| `UNCLEAR` | Unklar | Unclear |

## 16. Hybridregeln

ChatGPT ist verantwortlich für Recherche, Fachlogik, Evidenz, Status, Delta und Sicherheitslevel. Copilot ist ausschließlich für die strukturgetreue Excel-Übertragung verantwortlich.

Copilot darf nicht:

- recherchieren,
- Quellen fachlich neu bewerten,
- Informationen erfinden oder ergänzen,
- Fachstatus oder Delta umdeuten,
- die Baseline überschreiben.

## 17. Standardunternehmen und -kategorien

Standardunternehmen: KROHNE, Endress+Hauser, Emerson, VEGA, WIKA, ABB, Honeywell, Yokogawa, Siemens, Schneider Electric, JUMO, ifm electronic.

Standardkategorien: Coriolis, Magnetisch-induktiv, Schwebekörper, Ultraschall, Vortex, Druck, Füllstand, Temperatur.

## 18. Arbeitsstil

- klar,
- sachlich,
- strukturiert,
- quellenbasiert,
- konservativ,
- KROHNE-nah,
- direkt intern nutzbar,
- keine unnötigen KI-Floskeln,
- keine Sicherheit vortäuschen.

