# Projekt und Zielbild

**Stand:** 31.08.2026  
**Status:** gültig  
**Evidenzstatus:** mehrfach bestätigt

## 1. Projektdefinition

Der PM Research Partner ist ein spezialisierter Market-Intelligence- und Marktrecherche-Assistent für KROHNE Messtechnik. Er wurde für technische Markt- und Wettbewerbsanalysen in der Prozessmesstechnik entwickelt und soll belastbare, strukturierte und intern nutzbare Entscheidungsgrundlagen erzeugen.

Seine Kernaufgabe ist nicht das bloße Finden von Informationen. Er verbindet:

- themenspezifische Recherchelogik,
- offizielle und nachvollziehbare Quellen,
- konservative Fachbewertung,
- Vergleich mit einem dokumentierten Ausgangsstand,
- Delta-/Change-Logik,
- Sicherheitslevel,
- Quality Gate,
- Matrix- und Excel-Ausgabe.

Der zentrale Anwendungsfall lautet:

> Eine vorhandene Baseline-Matrix wird mit dem neuesten belastbar belegten Informationsstand aktualisiert und die relevanten Veränderungen werden nachvollziehbar dokumentiert.

## 2. Entstehung und Problemstellung

Ausgangspunkt war eine manuelle Marktanalyse zu Ethernet-APL, PoE, PoDL und Ethernet-basierten Kommunikationsprofilen bei Messgeräten. Die wiederkehrende Aktualisierung zeigte typische Probleme:

- hoher Zeitaufwand für wiederholte Herstellerrecherche,
- uneinheitliche Quellenqualität,
- Verwechslung benachbarter Technologien,
- fehlende Trennung von neu gefundenen und wirklich neuen Marktinformationen,
- schwer nachvollziehbare Produkt-/Quellenzuordnung,
- Medienbrüche zwischen Recherche, Matrix und Präsentation,
- Verlust von Wissen zwischen einzelnen Durchläufen.

Aus einer einzelnen Recherche entstand schrittweise ein modularer Research Partner mit System Prompt, Routing Index, themenspezifischen Master Prompts und Baselines.

## 3. Geschäftlicher Zweck

Der PM Research Partner soll wiederkehrende Markt- und Wettbewerbsanalysen standardisieren und beschleunigen. Der Nutzen liegt insbesondere in:

- regelmäßigen Marktupdates statt isolierter Einmalrecherchen,
- reduzierter manueller Wiederholungsarbeit,
- nachvollziehbaren Direktquellen,
- vergleichbarer Bewertung über Zeit,
- strukturiertem KROHNE-vs.-Wettbewerber-Vergleich,
- Speicherung von Marktkenntnissen in Baselines und Change-Logs,
- schnellerer Erkennung relevanter Produkt- und Technologieentwicklungen,
- Erweiterbarkeit auf weitere Technologien oder Märkte,
- besserer Übergabefähigkeit im Team.

## 4. Zielgruppen

Die Ergebnisse sollen nutzbar sein für:

- Produktmanagement,
- Produktstrategie und Roadmaps,
- Produktentwicklung,
- Wettbewerbsanalyse,
- Marketing,
- Vertrieb,
- interne Managemententscheidungen.

Die Positionierung lautet sinngemäß:

- Built by KROHNE employees for KROHNE employees.
- Für branchenspezifische industrielle Recherche entwickelt.
- An KROHNE-Anforderungen angepasst.
- Für interne Nutzung vorgesehen.
- Für zusätzliche Technologien und zu beobachtende Märkte erweiterbar.

## 5. Aktuelle Recherchebereiche

### 5.1 Ethernet-APL, PoE und PoDL

Priorität 1 ist Ethernet-APL. Die Hauptmatrix bewertet ausschließlich ausdrücklich belegte Ethernet-APL-Unterstützung je Unternehmen und Messprinzip.

Priorität 2 sind PoE und PoDL. Sie werden in einer separaten Matrix erfasst und dürfen keinen positiven Ethernet-APL-Status auslösen.

Priorität 3 sind Kommunikationsprofile wie PROFINET, Modbus TCP, EtherNet/IP, OPC UA oder allgemeines Industrial Ethernet. Sie sind Zusatzinformationen und dürfen nur dann in einer positiven APL-Zelle erscheinen, wenn Ethernet-APL selbst belastbar belegt ist.

### 5.2 Diagnose und Verifikation

Die Hauptbewertung bezieht sich auf Geräteverifikation: eine aktiv initiierte oder geführte Prüfung gegen einen Referenzzustand beziehungsweise eine definierte Prüflogik mit dokumentiertem Ergebnis, etwa Pass/Fail, Report, Prüfprotokoll oder Zertifikat.

Diagnose, NE107, Condition Monitoring, Predictive Maintenance und Kalibrierung sind zusätzliche Vergleichsdimensionen, aber kein Ersatznachweis für Verifikation.

KROHNE OPTICHECK und `OPTICHECK Technology built in` dienen als interne Benchmarks, werden aber nach denselben Belegregeln wie Wettbewerber bewertet.

## 6. Standard-Scope

### Unternehmen

1. KROHNE
2. Endress+Hauser
3. Emerson
4. VEGA
5. WIKA
6. ABB
7. Honeywell
8. Yokogawa
9. Siemens
10. Schneider Electric
11. JUMO
12. ifm electronic

### Messprinzipien und Kategorien

1. Coriolis
2. Magnetisch-induktiv
3. Schwebekörper
4. Ultraschall
5. Vortex
6. Druck
7. Füllstand
8. Temperatur

Der Nutzer kann Scope und Reihenfolge auftragsbezogen ändern.

## 7. Erwartete Ergebnisse

### Ethernet-APL

- Ethernet-APL-Matrix,
- getrennte PoE-/PoDL-Matrix,
- atomar aufgebautes Quellenverzeichnis,
- Delta- und Change-Log,
- optional Management Summary.

### Verifikation

Der aktuelle Master-Prompt-Stand vom 27.08.2026 sieht vor:

- Verifikations-Matrix vor Quality Gate,
- Verifikations-Matrix nach Quality Gate,
- Kriterien-Matrix vor Quality Gate,
- Kriterien-Matrix nach Quality Gate,
- Quellenverzeichnis,
- Delta- und Change-Log,
- optional Management Summary.

Diese Zielstruktur ist jünger als die fünfteilige Verifikationsbaseline vom 06.07.2026 und muss in einem End-to-End-Test praktisch bestätigt werden.

## 8. Qualitätsversprechen

- keine Spekulation,
- keine erfundenen Informationen,
- offizielle Hersteller- und Primärquellen bevorzugen,
- unter 95 % Sicherheit keine Aussage als bestätigten Fakt darstellen,
- `keine Infos` bei unzureichender Evidenz,
- `nicht vorhanden` nur mit ausdrücklichem Negativnachweis,
- `Neu` nur mit belastbarem Zeitnachweis im Update-Zeitraum,
- direkte Belegkette zum Produkt, zur Variante und zum Messprinzip,
- dokumentierte Prüfung vor Freigabe.

## 9. Menschliche Verantwortung

Der PM Research Partner ist eine Arbeits- und Entscheidungsunterstützung, keine autonome Freigabestelle.

- Mitarbeitende prüfen geschäftskritische Aussagen.
- Sicherheitslevel ersetzen keine fachliche Stichprobe.
- Neue, geänderte oder strategisch relevante Ergebnisse benötigen besondere Prüfung.
- Das interne Quality Gate ist ein strukturierter KI-/Workflow-Review und keine Prüfung durch mehrere unabhängige menschliche Experten.

## 10. Langfristiges Zielbild

Das langfristige Ziel ist eine wiederverwendbare interne Research- und Knowledge-Engine:

- modulare Erweiterung um neue Master Prompts und Baselines,
- einheitliche Release- und Dateigovernance,
- stabile DE/EN-Ausgabe aus einer gemeinsamen Fachlogik,
- reproduzierbarer Hybrid-Workflow zur Excel-Erzeugung,
- prüfbarer Gold-Standard und Regressionstests,
- perspektivisch maschinenlesbarer Datenvertrag und Validator,
- dauerhafte Speicherung von Entscheidungen, Fehlern und Lessons Learned im Second Brain.

## 11. Nicht-Ziele

- autonome fachliche Freigabe ohne Mitarbeitende,
- positive Matrixzellen um jeden Preis,
- Vermischung ähnlicher Technologien,
- Ersatz sämtlicher operativer Dateien durch einen Mega-Prompt,
- ungeprüfte Übernahme alter Baselines als Wahrheit,
- doppelte Fachrecherche nur wegen einer anderen Ausgabesprache.

