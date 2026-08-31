# Business Case und Wertbeitrag

**Stand:** 31.08.2026  
**Status:** zu prüfen  
**Evidenzstatus:** historisch dokumentiert  
**Einordnung:** Einzelne Nutzenhypothesen und das empfohlene Messmodell sind als Ableitungen gekennzeichnet.

## 1. Zweck dieses Dokuments

Dieses Dokument trennt den fachlich bereits erkennbaren Nutzen des PM Research Partners von noch nicht freigegebenen Wirtschaftlichkeitsannahmen. Zeit-, Kosten- und Lizenzwerte sind nur dann Entscheidungsgrundlage, wenn Bezugszeitpunkt, Nutzerzahl, Tarif, Wechselkurs und Prozessumfang aktuell verifiziert wurden.

## 2. Wertlogik

Der PM Research Partner erzeugt Wert in vier aufeinander aufbauenden Stufen:

1. **Rechercheaufwand reduzieren:** wiederkehrende Suchen, Quellenprüfung und Matrixpflege werden standardisiert.
2. **Ergebnisqualität erhöhen:** Fachgrenzen, direkte Quellen, konservative Statuslogik und Quality Gate reduzieren Fehlklassifikationen.
3. **Wissen erhalten:** Baselines, Deltas, Entscheidungen, Tests und Lessons Learned bleiben über einzelne Chats hinweg verfügbar.
4. **Entscheidungen beschleunigen:** Produktmanagement und angrenzende Funktionen erhalten vergleichbare, nachvollziehbare Marktinformationen.

Die vier Stufen dürfen nicht auf eine reine Zeitersparnis verkürzt werden. Ein schneller, aber falsch zugeordneter APL-Nachweis kann mehr Folgekosten erzeugen als er einspart.

## 3. Belegte beziehungsweise mehrfach bestätigte Nutzenfelder

| Nutzenfeld | Wertbeitrag | Evidenz | Einschränkung |
|---|---|---|---|
| Wiederkehrende Marktupdates | weniger manuelle Wiederholungsarbeit | Projektverlauf und modulare Update-Logik | tatsächliche Zeitersparnis je Bereich messen |
| Vergleich mit Baseline | echte Änderungen werden von bloß neu gefundenen Informationen getrennt | DEC-003, DEC-004, DEC-008 | setzt belastbare Baseline und Zeitraum voraus |
| Direkte Quellen | Aussagen werden prüf- und weiterverwendbar | DEC-009, DEC-021 | direkte Produktquellen sind nicht immer verfügbar |
| Konservative Bewertung | geringeres Risiko falscher Positivmeldungen | DEC-006, DEC-010, DEC-011 | `keine Infos` ist fachlich korrekt, aber nicht vollständig |
| Strukturierte Excel-Ausgabe | schnellere Nutzung in bestehenden Arbeitsabläufen | FILE-007, FILE-008, DEC-016 | Hybrid-End-to-End-Test noch offen |
| Wissenssicherung | Entscheidungen und Fehler gehen zwischen Durchläufen nicht verloren | DEC-023 | Pflegeprozess muss eingehalten werden |
| Skalierbarkeit | neue Technologien können über Route, Master Prompt und Baseline ergänzt werden | DEC-001, DEC-002 | jede Erweiterung benötigt Fachregeln und Tests |
| Teamfähigkeit | Übergabe und Review werden reproduzierbarer | vorhandene Übergabe und dieses Second Brain | Rollen und Freigabeinhaber noch festzulegen |

## 4. Historische Zeitannahme

Im bisherigen Business-Case-Verlauf wurden **44 Stunden pro Jahr** beziehungsweise ungefähr **eine Arbeitswoche pro Jahr** als potenzielle Zeitersparnis verwendet.

- Status: zu prüfen
- Evidenzstatus: historisch dokumentiert
- Aussagekraft: Planungsannahme, keine abgeschlossene Zeitmessung
- Nicht enthalten beziehungsweise nicht eindeutig abgegrenzt: Reviewzeit, Fehlerkorrektur, Promptpflege, Baselinepflege, Lizenzadministration und zusätzliche Recherchebereiche

Für eine belastbare Freigabe sollte die Annahme in mindestens drei echten Aktualisierungszyklen gemessen werden:

| Messgröße | Definition |
|---|---|
| Manueller Referenzaufwand | Zeit für Recherche, Bewertung, Quellenpflege, Excel und Review ohne Partner |
| Assistierter Aufwand | Zeit für Preflight, Lauf, Prüfung, Korrektur, Excel und Ablage |
| Nettoersparnis | Referenzaufwand minus assistierter Aufwand |
| Nacharbeitsquote | Korrekturzeit geteilt durch assistierten Gesamtaufwand |
| Wiederverwendungsquote | Anteil übernommener, erneut bestätigter Baseline-Einträge |

## 5. Historische Break-even-Angaben

Frühere Projektstände nannten ungefähr **0,31 Monate** und ungefähr **96 Monate** als Break-even-Werte für unterschiedliche Szenarien. Diese Angaben wurden später durch geänderte Annahmen relativiert und gelten deshalb **nicht als finaler Business Case**.

- Status: archiviert
- Verwendung: nur als Hinweis auf frühere Modellrechnungen
- Verbot: nicht ohne Rekonstruktion der Formeln und Aktualisierung der Preise in Präsentationen oder Freigaben übernehmen
- Nächster Schritt: Kostenmodell neu aufsetzen und Sensitivitäten dokumentieren

## 5.1 Vollständige Prüfung der Fachaufgabe-Präsentation

FILE-020 wurde am 31.08.2026 vollständig über alle 43 Folien ausgewertet. Die Präsentation enthält einen frühen Make-or-Buy-or-do-nothing-Vergleich:

| historischer Wert | Make | Buy | manuell / Do nothing |
|---|---:|---:|---:|
| Nutzwert | 4,25 | 3,75 | 3,25 |
| Ranking | 1 | 2 | 3 |
| dargestellte Gesamtkosten für zwölf Monate | 420,72 € | 4.686,72 € | 6.400,00 € |

Dokumentierte Modellannahmen:

- 7,50 € Bruttostundenlohn für Einrichtung durch einen Auszubildenden,
- 32,00 € Bruttostundenlohn für Produktmanagement,
- 900,00 € Agentur-Tagessatz,
- vier Stunden Make-Einrichtung,
- vier Tage Buy-Einrichtung,
- 0,33 Stunden je automatisiertem Durchlauf,
- 22,00 € monatliche Make-Abokosten,
- 80,00 € monatliche Buy-Wartungskosten,
- 50 Stunden je manueller Recherche.

Die Präsentation ist als Business-Case-Nachweis noch nicht freigabefähig:

- Die Tabelle nennt vier manuelle Läufe pro Jahr und 50 Stunden je Lauf. Das ergibt 200 Stunden/Jahr, nicht die ebenfalls dargestellten 300 Stunden/Jahr.
- Die Folie zum Fazit behauptet ungefähr 50 Stunden Ersparnis pro Monat. Das passt weder zu vier Läufen pro Jahr noch eindeutig zu den Tabellenannahmen.
- Die Folien enthalten den Datumsplatzhalter `2027-01-XX`; der Library-Dateistand ist 16.07.2026.
- Kosten, Tarife, Nutzerzahlen und organisatorische Randbedingungen sind zeitabhängig.

Die Werte bleiben als historischer Modellstand erhalten. TEST-014, ERR-019 und OPEN-018 steuern ihre Korrektur und Freigabe.

## 6. Make-or-Buy- und Toollogik

### Interne, spezialisierte Lösung

Potenzielle Vorteile:

- fachlich auf KROHNE und industrielle Messtechnik zugeschnitten,
- vorhandene Baselines und interne Begriffslogik nutzbar,
- Methodik kann unabhängig von einzelnen Recherchethemen erweitert werden,
- geringerer Übergabeverlust als bei isolierten Einzelrecherchen,
- keine externe Fachlogik muss vollständig neu aufgebaut werden.

Zu prüfende Kosten und Risiken:

- Prompt-, Test- und Baselinepflege,
- fachliche Freigabezeit,
- Abhängigkeit von Modell- und Produktfunktionen,
- Governance für interne Daten und Quellen,
- Versionsdrift zwischen System Prompt, Routing, Master Prompts und Baselines.

### Externe oder stärker standardisierte Lösung

Mögliche Vorteile:

- standardisierte Administration und Support,
- gegebenenfalls stärkere Integration in vorhandene Microsoft- oder Datenplattformen,
- potenziell weniger Eigenpflege für generische Aufgaben.

Mögliche Nachteile:

- branchenspezifische Fachlogik muss angepasst oder neu aufgebaut werden,
- bestehende Baselines und konservative Statusregeln lassen sich nicht automatisch übertragen,
- zusätzlicher Aufwand für Integration, Datenvertrag und Abnahme.

Die Make-or-Buy-Entscheidung darf daher nicht nur Lizenzpreise vergleichen. Relevant sind Gesamtkosten pro freigegebenem Recherchezyklus und die nachgewiesene Ergebnisqualität.

## 7. ChatGPT-/Copilot-Arbeitsteilung

Der aktuell beschlossene praktische Hybrid lautet:

- ChatGPT: Fachrecherche, Evidenzbewertung, Statuslogik, Delta und freigegebenes strukturiertes Markdown.
- Copilot Chat Basic: technische Prüfung und Übertragung dieses Markdown in Excel.
- Copilot: keine eigene Webrecherche und keine fachliche Neuinterpretation.

Diese Arbeitsteilung ist fachlich plausibel, aber der komplette Copilot-v1.1-End-to-End-Nachweis steht noch aus. Eine Premiumlizenz ist nur dann wirtschaftlich begründbar, wenn sie gegenüber dem vorhandenen Basic-Workflow einen gemessenen Zusatznutzen erzeugt.

## 8. Noch offene Investitionsentscheidungen

| Thema | Aktueller Stand | Benötigter Nachweis | Verknüpfung |
|---|---|---|---|
| finale ChatGPT-/Copilot-Lizenzierung | offen | aktuelle Preise, Nutzerzahl, Funktionsbedarf, E2E-Test | OPEN-011 |
| Modellwahl für Gold-Standard | offen | gleicher Testkorpus, Qualitäts-/Zeit-/Kostenvergleich | OPEN-012 |
| Copilot Premium | nicht freigegeben | messbarer Mehrwert gegenüber Basic | OPEN-011 |
| zusätzliche Research-Bereiche | offen | Priorität, Updatefrequenz, Baseline, erwarteter Nutzen | OPEN-016 |
| Validator/Automatisierung | perspektivisch | Fehlerreduktion und Wartungsaufwand | OPEN-017 |
| finaler monetärer Business Case | offen | konsistente Einheiten, Formeln, aktuelle Kosten und Pilotmessung | OPEN-018 |

## 9. Empfohlenes Messmodell für den nächsten Pilot

### Mindestumfang

- drei reale Update-Zyklen,
- mindestens zwei Fachbereiche, sofern Verifikation produktionsfähig ist,
- dokumentierter manueller Vergleichsaufwand,
- identische Abnahmekriterien je Lauf,
- vollständige Erfassung von Review und Nacharbeit.

### Kern-KPIs

| KPI | Berechnung | Zielrichtung |
|---|---|---|
| Nettozeitersparnis | manuelle Zeit minus assistierte Zeit | positiv und stabil |
| First-pass-Abnahmequote | ohne fachliche Korrektur akzeptierte Zellen / geprüfte Zellen | steigend |
| Quellenabdeckungsquote | direkt belegte materielle Aussagen / materielle Aussagen | steigend |
| Fehlklassifikationsquote | falsch positive oder falsch negative Zellen / geprüfte Zellen | sinkend |
| Nacharbeitsquote | Korrekturzeit / assistierter Gesamtaufwand | sinkend |
| Durchlaufzeit | Auftrag bis freigegebener Output | sinkend |
| Wiederverwendungsquote | bestätigte Baseline-Übernahmen / geprüfte Baseline-Einträge | beobachten |

Zielwerte werden erst nach einem initialen Messzyklus festgelegt; derzeit fehlen belastbare Referenzdaten.

## 10. Entscheidungsregel für eine Freigabe

Eine organisatorische Skalierung ist sinnvoll, wenn gleichzeitig:

1. die fachlichen Mindesttests bestanden sind,
2. der Freigabeprozess und die verantwortlichen Rollen feststehen,
3. die Nettozeitersparnis einschließlich Review positiv ist,
4. keine relevante Qualitätsverschlechterung gegenüber manueller Recherche entsteht,
5. Lizenz- und Betriebskosten mit aktuellen Preisen dokumentiert sind,
6. der Workflow mindestens einen vollständigen Updatezyklus reproduzierbar durchlaufen hat.

Bis dahin lautet der Status: **fachlicher und operativer Nutzen plausibel, finaler monetärer Business Case zu verifizieren**.
