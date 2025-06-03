# M122_Skriptsprache

## 📍 Grundlagen

- **Prompt**: `$` = Eingabeaufforderung der Shell
- **Befehlssyntax**: `befehl [optionen] [argumente]`

---

## 📁 Navigation in der Verzeichnisstruktur

| Befehl        | Erklärung                            | Beispiel              |
|---------------|---------------------------------------|-----------------------|
| `pwd`         | zeigt aktuelles Verzeichnis          | `pwd`                 |
| `ls`          | listet Dateien im Verzeichnis auf    | `ls -l`               |
| `cd [pfad]`   | wechselt Verzeichnis                 | `cd /home/user`       |
| `cd ..`       | geht ein Verzeichnis zurück          |                       |
| `cd ~`        | wechselt ins Home-Verzeichnis        |                       |
| `cd -`        | wechselt ins vorherige Verzeichnis   |                       |

---

## 📄 Dateien erstellen, lesen, editieren, löschen

| Befehl         | Erklärung                                 | Beispiel                |
|----------------|--------------------------------------------|-------------------------|
| `touch datei`  | erstellt neue Datei                        | `touch test.txt`        |
| `cat datei`    | zeigt Dateiinhalt                          | `cat test.txt`          |
| `nano datei`   | öffnet Datei im Editor (einfach)           | `nano test.txt`         |
| `vi datei`     | öffnet Datei im `vi` Editor (fortgeschritten) | `vi test.txt`       |
| `echo text`    | gibt Text aus                              | `echo Hallo Welt!`      |
| `rm datei`     | löscht Datei                               | `rm test.txt`           |
| `mv a b`       | verschiebt oder benennt Datei um           | `mv alt.txt neu.txt`    |
| `cp a b`       | kopiert Datei                              | `cp a.txt b.txt`        |
| `wc datei`     | zählt Wörter, Zeilen usw.                  | `wc -l test.txt`        |

---

## 📚 Hilfesystem (Manpages)

| Befehl                | Erklärung                           |
|-----------------------|--------------------------------------|
| `man befehl`          | zeigt Anleitung zu einem Befehl     |
| `man -k suchbegriff`  | sucht in Manpages (wie Google)      |
| `apropos suchbegriff` | wie `man -k`, zeigt relevante Befehle|

---

## 🎯 Wildcards & Tilde

| Symbol  | Bedeutung                                 | Beispiel                |
|---------|--------------------------------------------|-------------------------|
| `*`     | beliebig viele Zeichen                    | `ls *.txt`              |
| `?`     | genau ein beliebiges Zeichen              | `ls datei?.txt`         |
| `~`     | Home-Verzeichnis des aktuellen Users      | `cd ~`                  |
