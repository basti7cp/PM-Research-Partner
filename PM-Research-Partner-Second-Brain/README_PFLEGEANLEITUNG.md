# Pflegeanleitung – PM Research Partner Second Brain

**Zweck:** Das Second Brain nach jedem relevanten Durchlauf konsistent aktualisieren.

## 1. Grundregeln

1. Der Zentralindex zeigt nur den aktuell gültigen Stand und aktive Risiken.
2. Details gehören in die thematischen Register oder ins Archiv.
3. Alte Entscheidungen und Ergebnisse werden nicht gelöscht, sondern als `ersetzt`, `verworfen` oder `archiviert` markiert.
4. Jede neue Entscheidung, jeder Test, Fehler, Recherche-Durchlauf und offene Punkt erhält eine unveränderliche ID.
5. Operative Prompts und Matrizen werden nicht in das Second Brain kopiert. Das Dateiregister dokumentiert ihre Rolle und Version.
6. Unbelegte Erinnerungen werden als `historisch dokumentiert` oder `zu verifizieren` markiert, nie als sicherer Fakt.

## 2. ID-Vergabe

| Typ | Präfix | Nächste ID ermitteln |
|---|---|---|
| Entscheidung | `DEC` | höchste vorhandene Nummer + 1 |
| Test | `TEST` | höchste vorhandene Nummer + 1 |
| Fehler | `ERR` | höchste vorhandene Nummer + 1 |
| Lesson Learned | `LESSON` | höchste vorhandene Nummer + 1 |
| Recherche | `RUN` | höchste vorhandene Nummer + 1 |
| Offener Punkt | `OPEN` | höchste vorhandene Nummer + 1 |
| Datei | `FILE` | höchste vorhandene Nummer + 1 |
| Version | `VER` | höchste vorhandene Nummer + 1 |

Eine einmal verwendete ID wird niemals neu vergeben.

## 3. Neuer Recherche-Durchlauf

1. Prüfe Route, Master Prompt, Baseline, letzten und aktuellen Abruf.
2. Vergib eine neue `RUN`-ID.
3. Kopiere `VORLAGEN/VORLAGE_RECHERCHE_DURCHLAUF.md` nach `ARCHIV/RECHERCHE_DURCHLAEUFE/`.
4. Benenne die Datei `RUN-NNN_YYYY-MM-DD_THEMENGEBIET.md`.
5. Dokumentiere Eingaben, verwendete Versionen, Ergebnis, Quality Gate, Delta und offene Nachprüfungen.
6. Ergänze den Durchlauf in `06_RECHERCHEHISTORIE.md`.
7. Erzeuge bei Bedarf neue `TEST`-, `ERR`-, `LESSON`-, `DEC`- oder `OPEN`-Einträge.
8. Ändere den Zentralindex nur, wenn sich der gültige Projektstand oder ein aktives Hauptrisiko ändert.

## 4. Neuer Test

1. Vergib eine `TEST`-ID.
2. Kopiere `VORLAGEN/VORLAGE_TEST.md` nach `ARCHIV/TESTDURCHLAEUFE/`.
3. Halte Erwartung und tatsächliches Ergebnis getrennt fest.
4. Verknüpfe festgestellte Fehler über `ERR`-IDs.
5. Führe nach einer Korrektur einen Retest durch; ändere nicht rückwirkend das ursprüngliche Ergebnis.
6. Ergänze die Kurzfassung in `04_TESTREGISTER.md`.

## 5. Neue oder geänderte Entscheidung

1. Vergib eine `DEC`-ID und nutze die Entscheidungsvorlage.
2. Dokumentiere Ausgangssituation, Entscheidung, Begründung und Auswirkungen.
3. Wird eine alte Entscheidung abgelöst, setze deren Status auf `ersetzt` und verlinke beide IDs.
4. Aktualisiere Architektur-, Versions- oder Dateiregister, wenn sie betroffen sind.
5. Aktualisiere den Zentralindex nur bei Änderung des gültigen Stands.

## 6. Fehlerkorrektur

1. Vergib eine `ERR`-ID.
2. Dokumentiere Fehlerbild, Ursache, Auswirkung, Korrektur und Prävention.
3. Verknüpfe den auslösenden Test oder Recherchelauf.
4. Erzeuge bei generalisierbarer Erkenntnis eine `LESSON`-ID.
5. Propagiere die Korrektur in alle abhängigen Ausgaben: Matrix, Quellenregister, Delta und Management Summary.
6. Halte den Retest separat fest.

## 7. Neue operative Dateiversion

1. Operative Datei nicht überschreiben, bevor Version und Freigabe geklärt sind.
2. Neuen `FILE`-Eintrag anlegen oder bestehenden Eintrag versionieren.
3. Vorgänger, Nachfolger, Datum, Sprache, Zweck und Status dokumentieren.
4. Betroffene `VER`-, `DEC`- und `TEST`-IDs verlinken.
5. Routing und exakte Dateinamen regressionsprüfen.

## 8. Evidenzstatus

- `direkt belegt`: aktuelle Projektdatei stützt den Inhalt.
- `mehrfach bestätigt`: mehrere Quellen stützen ihn.
- `historisch dokumentiert`: datierte Übergabe oder Gesprächschronik.
- `abgeleitet`: nachvollziehbare, aber nicht beschlossene Schlussfolgerung.
- `zu verifizieren`: Beleg fehlt oder ist nicht ausreichend.

## 9. Abschlussprüfung jeder Pflegeänderung

- IDs eindeutig?
- Links gültig?
- aktueller und historischer Stand getrennt?
- direkte Quellen korrekt zugeordnet?
- keine Technologieverwechslung?
- keine Verwechslung Diagnose/Verifikation?
- `Neu` nur mit Zeitnachweis?
- `nicht vorhanden` nur mit Negativnachweis?
- keine `Unverändert`-Einträge im Delta?
- Quality Gate dokumentiert?
- Zentralindex nur bei echter Statusänderung angepasst?

## 10. Empfohlene Lesereihenfolge für neue Teammitglieder

1. `00_SECOND_BRAIN_INDEX.md`
2. `01_PROJEKT_UND_ZIELBILD.md`
3. `02_ARCHITEKTUR_UND_VERSIONEN.md`
4. `10_GLOSSAR_UND_REGELWERK.md`
5. `07_PROMPT_UND_DATEIENREGISTER.md`
6. aktueller Master Prompt und zugehörige Baseline
7. letztes Test- und Rechercheprotokoll
8. `09_OFFENE_PUNKTE_UND_ROADMAP.md`

