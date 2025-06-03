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


---


## 📜 Skript erstellen

```bash
#!/bin/bash
# Kommentarzeile
echo "Hallo Welt"
````

* Datei erstellen: `nano mein_script.sh`
* Ausführbar machen: `chmod +x mein_script.sh`
* Ausführen: `./mein_script.sh`

---

## 🧮 Variablen

```bash
name="Max"
echo "Hallo $name"
```

* Kein Leerzeichen um `=`
* Zugriff mit `$variablenname`

---

## ✍️ Editor: nano, vi, vim

| Editor | Aufruf          | Hinweis                          |
| ------ | --------------- | -------------------------------- |
| nano   | `nano datei.sh` | einfachster Editor               |
| vi     | `vi datei.sh`   | fortgeschrittener Editor         |
| vim    | `vim datei.sh`  | "verbesserter vi" mit mehr Tools |

---

## ➕ Arithmetische Operatoren

```bash
a=5
b=2
ergebnis=$((a + b))
echo $ergebnis  # Ausgabe: 7
```

| Operator | Bedeutung      |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraktion    |
| `*`      | Multiplikation |
| `/`      | Division       |
| `%`      | Modulo (Rest)  |

---

## 🔤 Zeichenketten (Strings)

```bash
text="Hallo"
echo "${text} Welt!"  # Ausgabe: Hallo Welt!
```

| Ausdruck   | Bedeutung                     |
| ---------- | ----------------------------- |
| `${var}`   | Sicherer Zugriff auf Variable |
| `${#text}` | Länge des Strings             |

---

## 🧱 Arrays

```bash
fruits=("Apfel" "Banane" "Kirsche")
echo ${fruits[1]}        # Banane
echo ${#fruits[@]}       # Anzahl Elemente
echo ${fruits[@]}        # Alle Elemente
```

| Ausdruck       | Bedeutung           |
| -------------- | ------------------- |
| `array=(...)`  | Array definieren    |
| `${array[0]}`  | Erstes Element      |
| `${#array[@]}` | Anzahl der Elemente |
| `${array[@]}`  | Alle Elemente       |

---

## 🧭 Kontrollstrukturen: if, then, else, elif

```bash
if [ $x -eq 5 ]; then
  echo "x ist 5"
elif [ $x -gt 5 ]; then
  echo "x ist größer als 5"
else
  echo "x ist kleiner als 5"
fi
````

### Vergleichsoperatoren

| Operator | Bedeutung      |
| -------- | -------------- |
| `-eq`    | gleich         |
| `-ne`    | ungleich       |
| `-lt`    | kleiner als    |
| `-le`    | kleiner/gleich |
| `-gt`    | größer als     |
| `-ge`    | größer/gleich  |

---

## 🔁 Schleifen

```bash
for i in {1..5}; do
  echo $i
done
```

```bash
while [ $x -le 5 ]; do
  echo $x
  x=$((x+1))
done
```

---

## 📤 Ein-/Ausgabe & Umleitungen

| Begriff     | Bedeutung                    | Beispiel                   |
| ----------- | ---------------------------- | -------------------------- |
| `stdin`     | Standardeingabe              | `read name`                |
| `stdout`    | Standardausgabe              | `echo "Hallo"`             |
| `stderr`    | Standardfehlerausgabe        | `ls datei 2> fehler.txt`   |
| `>`         | Ausgabe überschreiben        | `echo Test > ausgabe.txt`  |
| `>>`        | Ausgabe anhängen             | `echo Mehr >> ausgabe.txt` |
| `<`         | Eingabe aus Datei            | `wc -l < datei.txt`        |
| `2>`        | nur Fehlermeldungen umleiten |                            |
| `/dev/null` | schwarzes Loch (ignorieren)  | `befehl 2> /dev/null`      |

---

## 🧱 Pipe `|` – Befehle verbinden

```bash
cat datei.txt | grep "Suche"
```

| Symbol | Bedeutung |                                    |
| ------ | --------- | ---------------------------------- |
| \`     | \`        | Ausgabe von links → Eingabe rechts |

---

## 🪲 Debugging & Fehlersuche

| Methode                      | Beispiel                    |
| ---------------------------- | --------------------------- |
| Script mit `bash -x` starten | `bash -x mein_script.sh`    |
| Variablen & Pfade prüfen     | `echo $variable`            |
| Exit-Codes prüfen            | `echo $?`                   |
| `set -e`                     | Script bricht bei Fehler ab |

---

## 🚀 Einbindung & Deployment

| Aktion                     | Beschreibung                               |
| -------------------------- | ------------------------------------------ |
| Skript auf Server kopieren | `scp mein_script.sh user@server:/pfad`     |
| SSH-Verbindung             | `ssh user@server`                          |
| Ausführung testen          | `./mein_script.sh` oder mit `bash` starten |

---



