
### 🧩 **Lernziel: Sie wissen was eine CLI (Command Line Interface) ist und kennen auch Synonyme davon.**

**Erklärung:**
Eine CLI ist eine textbasierte Schnittstelle, über die man direkt Befehle an das Betriebssystem eingibt.
Synonyme: **Shell**, **Terminal**, **Kommandozeile**, **Konsole**.
Man verwendet CLI typischerweise für systemnahe Arbeiten, Automatisierung oder Verwaltung.

**Beispiel:**
Im Terminal kann man mit `ls` den Inhalt eines Ordners anzeigen lassen.

---

### 🖼️ **Lernziel: Sie wissen was eine GUI ist und kennen den Unterschied zu einer CLI.**

**Erklärung:**
Eine GUI (**Graphical User Interface**) ist eine grafische Oberfläche mit Fenstern, Icons und Schaltflächen.
Der Unterschied zur CLI: Die GUI ist visuell und einfacher zu bedienen, CLI ist schneller und für Profis geeignet.

**Beispiel:**
Dateien per **Datei-Explorer** öffnen (GUI) vs. `cd` und `ls` im Terminal (CLI).

---

### 🧮 **Lernziel: Sie kennen die Vor- und Nachteile von GUI und CLI betreffend Ressourcen.**

**Erklärung:**

* **CLI Vorteile:** Schnell, benötigt wenig Speicher, lässt sich automatisieren.
* **CLI Nachteile:** Höhere Einstiegshürde, erfordert Befehlskenntnis.
* **GUI Vorteile:** Benutzerfreundlich, visuelles Feedback.
* **GUI Nachteile:** Mehr Ressourcenverbrauch (RAM, CPU), weniger Automatisierung.

---

### 📂 **Lernziel: Sie kennen einfache Befehle wie `ls`, `mkdir`, `diff`, `less`, `tail`, `cat`, `ip`, `pwd`, `date` und deren Einsatz.**

| Befehl  | Zweck                                 |
| ------- | ------------------------------------- |
| `ls`    | Dateien im Ordner anzeigen            |
| `mkdir` | Neues Verzeichnis erstellen           |
| `diff`  | Unterschiede zwischen Dateien zeigen  |
| `less`  | Datei seitenweise anzeigen            |
| `tail`  | letzte Zeilen anzeigen                |
| `cat`   | Datei komplett anzeigen               |
| `ip a`  | Netzwerkinfo anzeigen (IP, Interface) |
| `pwd`   | aktueller Pfad anzeigen               |
| `date`  | Datum und Uhrzeit anzeigen            |

---

### 🤖 **Lernziel: Sie kennen Einsatzgebiete/Jobs der Automatisierung und auch welche Tasks nicht gut automatisiert werden können.**

**Geeignet für Automatisierung:**

* Backup-Skripte
* Software-Updates
* Logdateien auswerten
* Benutzer anlegen

**Nicht gut automatisierbar:**

* Kreative Tätigkeiten (Design)
* Entscheidungen mit viel Kontext
* Unklare, sich ständig ändernde Aufgaben

---

### 🔡 **Lernziel: Sie wissen was case sensitiv ist.**

**Erklärung:**
„Case sensitive“ bedeutet, dass **Groß- und Kleinschreibung unterschieden wird**.
`Datei.txt` ≠ `datei.txt` → zwei verschiedene Dateien.

---

### 💬 **Lernziel: Sie können Kommentare in einem Skript erstellen.**

**Erklärung:**
Kommentare beginnen mit `#` und werden nicht ausgeführt.
Sie dienen zur Erklärung des Codes.

```bash
# Das ist ein Kommentar
echo "Hallo"
```

---

### ⏰ **Lernziel: Sie kennen die Zeitsteuerung mit Crond/Cronjobs.**

**Erklärung:**
Mit `cron` kann man Befehle zeitgesteuert ausführen lassen.

```bash
crontab -e
# Beispiel: täglich um 3 Uhr ein Skript starten
0 3 * * * /home/user/backup.sh
```

---

### 🔐 **Lernziel: Sie kennen die Datei-Rechte RWX und können diese für User und Gruppe setzen.**

**Erklärung:**

* **r** = read (lesen), **w** = write (schreiben), **x** = execute (ausführen)
* Rechte setzen mit `chmod`:

```bash
chmod u+x script.sh   # User darf ausführen
chmod g+w datei.txt   # Gruppe darf schreiben
```

---

### 🔒 **Lernziel: Sie kennen Sicherheitsregeln betreffend Ausführrechten von Skripten.**

**Erklärung:**

* Nur Skripte aus vertrauenswürdigen Quellen ausführbar machen.
* Keine unnötigen `777`-Rechte vergeben.
* Skripte in sicheren Pfaden speichern.

---

### 🧭 **Lernziel: Sie kennen Designtechniken wie Programmabläufe grafisch abgebildet werden können.**

**Erklärung:**

* **Ablaufdiagramm**: Pfeile + Symbole zeigen Schritte.
* **Pseudocode**: strukturierte Beschreibung in Klartext.
* **Strukturdiagramm**: hierarchische Darstellung.

---

### 📘 **Lernziel: Sie wissen aus welchen Gründen Skripte dokumentiert werden sollen.**

**Erklärung:**

* Nachvollziehbarkeit für andere Entwickler
* Fehler schneller finden
* Wartung und Erweiterung erleichtern

---

### 🧪 **Lernziel: Sie können Tests vorbereiten und fachgerecht durchführen.**

**Erklärung:**

* Eingaben und erwartete Ausgaben definieren
* Tests für normale und Fehlerfälle schreiben
* Automatisierte Tests möglich (z. B. Log-Prüfung)

---

### 🧾 **Lernziel: Sie wissen wie Dateinamen von Skripten aussehen sollen und welche Zeichen verwendet werden sollen.**

**Erklärung:**

* **Erlaubt:** Buchstaben, Zahlen, `-`, `_`
* **Nicht erlaubt:** Leerzeichen, Umlaute, Sonderzeichen
* Beispiel: `backup_daily.sh`

---

### 🏷️ **Lernziel: Sie können die wichtigsten Informationen in einem Scriptheader setzen.**

**Beispiel für Header:**

```bash
#!/bin/bash
# Autor: Max Muster
# Version: 1.0
# Zweck: Tägliches Backup
# Datum: 01.06.2025
```

---

### 🔀 **Lernziel: Sie wissen wie man eine Shebang für Bash schreibt.**

```bash
#!/bin/bash
```

→ Steht **ganz oben** in der Datei, sagt dem System, wie es das Skript ausführen soll.

---

### 🔎 **Lernziel: Sie können eine Datei auf dem System suchen und finden.**

```bash
find / -name "mein_skript.sh"
```

→ durchsucht das System nach dem Dateinamen

---

### 🔇 **Lernziel: Sie kennen die Infokanäle und können Fehlermeldungen/Ausgaben mit einem Zusatzbefehl unterdrücken.**

* stdout (Ausgabe) = 1
* stderr (Fehler) = 2

**Beispiel:**

```bash
befehl 2> /dev/null  # Fehler unterdrücken
```

---

### 🔍 **Lernziel: Sie kennen den Befehl um in Textdateien einen Suchstring zu finden und können diesen auch anwenden.**

```bash
grep "Suche" datei.txt
```

→ Zeigt alle Zeilen mit dem Suchwort an

---

### 🌟 **Lernziel: Sie kennen Wildcardzeichen und können diese einsetzen.**

| Zeichen | Bedeutung                    |
| ------- | ---------------------------- |
| `*`     | beliebige Zeichenfolge       |
| `?`     | genau ein beliebiges Zeichen |

**Beispiel:** `ls *.txt` → zeigt alle `.txt`-Dateien

---

### 🧾 **Lernziel: Sie können innerhalb eines Skriptes auf Parameter zugreifen.**

```bash
#!/bin/bash
echo "Erster Parameter: $1"
echo "Zweiter Parameter: $2"
```

---

### ➡️ **Lernziel: Sie können Ausgaben umleiten.**

* `>` überschreibt Datei
* `>>` hängt an
* `<` Eingabe aus Datei
* `2>` Fehler umleiten

---

### 🔐 **Lernziel: Sie kennen Methoden wie Sie per ssh/scp Dateien von einem System auf das andere bringen.**

```bash
ssh user@server
scp datei.txt user@server:/ziel
```

---

### 📦 **Lernziel: Sie können ein einfaches Array abfüllen.**

```bash
farben=("rot" "grün" "blau")
echo ${farben[1]}  # Ausgabe: grün
```

---

### 🔁 **Lernziel: Sie können eine Schleife erstellen.**

```bash
for i in {1..5}; do
  echo $i
done
```

---

### 🧾 **Lernziel: Sie können sich im System bewegen, Dateien anzeigen und bearbeiten.**

* Anzeigen: `cat`, `less`
* Bearbeiten: `nano`, `vi`
* Erstellen: `touch`
* Löschen: `rm`

---

### ⚙️ **Lernziel: Sie können ein BASH-Skript erstellen und ausführen.**

1. Skript erstellen: `nano mein_script.sh`
2. Inhalt schreiben:

```bash
#!/bin/bash
echo "Hallo"
```

3. Rechte setzen: `chmod +x mein_script.sh`
4. Ausführen: `./mein_script.sh`

---
