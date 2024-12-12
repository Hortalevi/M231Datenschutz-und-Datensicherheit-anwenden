# M231Datenschutz-und-Datensicherheit-anwenden

## Levi Agostinho Horta

## Grafische_Ablagekonzept.md
https://github.com/Hortalevi/M231Datenschutz-und-Datensicherheit-anwenden/blob/main/Grafische_Ablagekonzept.md

## GitÜbung als Ablage- und Versionsverwaltung kennenlernen
https://github.com/Hortalevi/M231Datenschutz-und-Datensicherheit-anwenden/blob/main/Git%C3%9Cbung_als_Ablage-_und_Versionsverwaltung_kennenlernen.md

## Fragen_DSG_DVS_EDB
https://github.com/Hortalevi/M231Datenschutz-und-Datensicherheit-anwenden/blob/main/Fragen_DSG_DVS_ED%C3%96B.md

## Backup.md
https://github.com/Hortalevi/M231Datenschutz-und-Datensicherheit-anwenden/blob/main/Backup.md

## Backup-Konzept
https://github.com/Hortalevi/M231Datenschutz-und-Datensicherheit-anwenden/blob/main/Backup_Konzept.md

## Aufgabe A: Was ist Git?

**Git** ist ein verteiltes Versionskontrollsystem, das von **Linus Torvalds** entwickelt wurde, dem Schöpfer des Linux-Kernels. Es wurde erstmals im Jahr 2005 veröffentlicht.

Mit Git können Sie:

- Änderungen an Dateien verfolgen.
- Versionen eines Projekts verwalten und wiederherstellen.
- Gleichzeitig mit mehreren Personen an einem Projekt arbeiten.
- Branches erstellen, um parallel an verschiedenen Features oder Fixes zu arbeiten.

---

## Aufgabe B: Wichtige Git-Befehle

```bash
# Git-Repository initialisieren
git init

# Änderungen verfolgen und hinzufügen
git add .

# Änderungen committen
git commit -m "Commit-Nachricht"

# Repository klonen
git clone <repository-url>

# Änderungen auf einen Remote-Server pushen
git push

# Änderungen von einem Remote-Repository abrufen
git pull

# Neuen Branch erstellen
git branch <branch-name>

# Zu einem Branch wechseln
git checkout <branch-name>

Aufgabe C: Branches in Git
Ein Branch (Zweig) ist eine unabhängige Entwicklungsumgebung innerhalb eines Git-Repositories. Branches ermöglichen es Entwicklern, an neuen Features, Bugfixes oder Experimenten zu arbeiten, ohne den Hauptcode (z. B. main) zu beeinflussen.

Weitere Details finden Sie in der Datei branches.md.

Aufgabe D: Linksammlung
Eine Sammlung nützlicher Links zu Git und Markdown finden Sie in der Datei links.md.

Abschluss-Arbeit
Verwenden Sie die folgenden Befehle, um Ihre Arbeit zu sichern:

bash
Copy code
git add .
git commit -m "Alle Aufgaben abgeschlossen"
git push
Review
Laden Sie eine:n Klassenkamerad:in ein, Ihr Projekt zu klonen:

bash
Copy code
git clone <repository-url>
Reviewer: [Name des Reviewers]
Datum: [Datum]
yaml
Copy code

---

Zusätzlich die beiden Dateien:

### `branches.md`
```markdown
# Branches in Git

## Was sind Branches?

Ein **Branch** (Zweig) ist eine unabhängige Entwicklungsumgebung innerhalb eines Git-Repositories. Branches ermöglichen es Entwicklern, an neuen Features, Bugfixes oder Experimenten zu arbeiten, ohne den Hauptcode (z. B. `main`) zu beeinflussen.

## Wichtige Befehle zu Branches

```bash
# Neuen Branch erstellen
git branch <branch-name>

# Zu einem Branch wechseln
git checkout <branch-name>

# Branch zusammenführen (Merge)
git merge <branch-name>

# Branch löschen
git branch -d <branch-name>

