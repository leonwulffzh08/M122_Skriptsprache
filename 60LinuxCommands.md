# Linux Befehle - Übersicht

## 1. Dateien & Verzeichnisse löschen

### `rm` – Löscht eine Datei
```bash
rm text.txt          # Löscht die Datei "text.txt"
rm -r ordner/        # Löscht den Ordner "ordner" (mit -r für rekursiv)
```
⚠️ **Achtung:** `rm` löscht endgültig! Kein Papierkorb!

### `rmdir` – Löscht einen leeren Ordner
```bash
rmdir leerer_ordner  # Funktiert nur, wenn der Ordner leer ist
```

## 2. Systembefehle & Benutzerverwaltung

### `clear` – Macht das Terminal sauber
```bash
clear  # Terminal ist wieder leer
```

### `whoami` – Zeigt aktuellen Benutzernamen
```bash
whoami  # Gibt z. B. "root" oder "deinname" aus
```

### `useradd` – Erstellt einen neuen Benutzer
```bash
sudo useradd max    # Legt Benutzer "max" an
```

### `adduser` – Wie useradd, aber einfacher
```bash
sudo adduser lisa   # Fragt nach Passwort etc.
```

### `sudo` – Führt einen Befehl als Admin aus
```bash
sudo apt update     # Führt "apt update" als Admin aus
```

### `su` – Wechselt zu einem anderen Benutzer
```bash
su root            # Wechselt zu root (Passwort nötig)
```

### `passwd` – Ändert Passwort
```bash
passwd            # Ändert Passwort des aktuellen Benutzers
sudo passwd lisa  # Ändert Passwort von Benutzer "lisa"
```

### `exit` – Beendet die Terminal-Session
```bash
exit  # Terminal-Fenster schließt sich
```

## 3. Paketverwaltung & Tools

### `apt` – Installiert oder aktualisiert Software
```bash
sudo apt update          # Aktualisiert die Paketliste
sudo apt install firefox # Installiert Firefox
```

### `finger` – Zeigt Benutzerinfos
```bash
finger max  # Zeigt Login-Zeiten, Shell etc. von "max"
```

### `man` – Zeigt das Handbuch für einen Befehl
```bash
man ls      # Zeigt alle Optionen für "ls"
```

### `whatis` – Kurzbeschreibung eines Befehls
```bash
whatis ls   # Zeigt: "ls - list directory contents"
```

### `curl` – Lädt Daten aus dem Internet
```bash
curl https://google.com  # Zeigt HTML-Code von Google
```

## 4. Dateien anzeigen & bearbeiten

### `less` – Zeigt eine Datei seitenweise an
```bash
less große_datei.txt  # Mit Leertaste blättern, 'q' zum Verlassen
```

### `head` – Zeigt die ersten Zeilen einer Datei
```bash
head log.txt          # Erste 10 Zeilen
head -n 5 log.txt     # Nur erste 5 Zeilen
```

### `tail` – Zeigt die letzten Zeilen einer Datei
```bash
tail log.txt          # Letzte 10 Zeilen
tail -f log.txt       # Verfolgt Live-Änderungen (gut für Logs)
```

### `cat` – Zeigt den Inhalt einer Datei an
```bash
cat datei.txt  # Gibt gesamten Inhalt aus
```

### `nano/vim` – Texteditoren im Terminal
```bash
nano datei.txt  # Einfacher Editor
vim datei.txt   # Leistungsstarker Editor (schwieriger für Anfänger)
```

## 5. Dateien vergleichen

### `cmp` – Vergleicht zwei Dateien Byte für Byte
```bash
cmp datei1.txt datei2.txt  # Zeigt erste Unterschiede
```

### `diff` – Zeigt Unterschiede zwischen zwei Dateien
```bash
diff datei1.txt datei2.txt  # Zeigt alle Unterschiede
```

## 6. Dateien sortieren & suchen

### `sort` – Sortiert Zeilen einer Datei
```bash
sort namen.txt      # Sortiert alphabetisch
sort -n zahlen.txt  # Sortiert numerisch
```

### `find` – Sucht nach Dateien
```bash
find /home -name "*.txt"  # Findet alle .txt-Dateien in /home
```

### `grep` – Sucht nach Text in Dateien
```bash
grep "error" log.txt  # Findet alle Zeilen mit "error"
```

## 7. Dateiberechtigungen & Verwaltung

### `chmod` – Ändert Dateiberechtigungen
```bash
chmod +x script.sh  # Macht "script.sh" ausführbar
chmod 755 datei     # Setzt Rechte auf rwxr-xr-x
```

### `chown` – Ändert den Besitzer einer Datei
```bash
sudo chown benutzer datei.txt  # Ändert Besitzer zu "benutzer"
```

### `ln` – Erstellt Verknüpfungen
```bash
ln -s /pfad/ziel linkname  # Symbolischer Link (wie Shortcut)
```

## 8. Dateien & Verzeichnisse erstellen/kopieren

### `touch` – Erstellt leere Datei oder aktualisiert Zeitstempel
```bash
touch datei.txt  # Erstellt "datei.txt" (falls nicht vorhanden)
```

### `mkdir` – Erstellt ein Verzeichnis
```bash
mkdir neuer_ordner # Legt "neuer_ordner" an
```

### `cp` – Kopiert Dateien/Ordner
```bash
cp quelle.txt ziel.txt  # Kopiert die Datei
cp -r ordner/ backup/  # Kopiert den Ordner rekursiv
```

### `echo` – Gibt Text aus oder schreibt in Dateien
```bash
echo "Hallo"  # Druckt "Hallo" im Terminal
echo "Text" > datei.txt  # Schreibt "Text" in datei.txt
```

### `shred` – Löscht Dateien sicher
```bash
shred -u datei.txt  # Überschreibt & löscht die Datei
```

## 9. Navigation

### `ls` – Listet Dateien auf
```bash
ls     # Einfache Liste
ls -l  # Liste mit Details (Rechte, Größe etc.)
```

### `pwd` – Zeigt aktuelles Verzeichnis
```bash
pwd  # Ausgabe: z. B. /home/deinname
```

### `cd` – Wechselt das Verzeichnis
```bash
cd /ordner  # Wechselt zu /ordner
cd ~        # Wechselt ins Home-Verzeichnis
```

## 10. Netzwerkbefehle

### `ifconfig/ip address` – Zeigt Netzwerk-Interfaces
```bash
ifconfig           # Älter (manchmal nicht installiert)
ip address         # Moderner (funktioniert immer)
```

### `ping` – Prüft Erreichbarkeit eines Servers
```bash
ping google.com    # Sendet Test-Pakete an Google
```

### `netstat/ss` – Zeigt Netzwerkverbindungen
```bash
netstat -tuln      # Zeigt offene Ports
ss -tuln           # Modernere Version
```

### `iptables/ufw` – Firewall-Verwaltung
```bash
sudo ufw enable    # Aktiviert die Firewall
```

### `ssh` – Verbindet zu einem anderen Rechner
```bash
ssh benutzer@server.de  # Login auf einem Remote-Server
```

## 11. System-Infos & Prozesse

### `uname` – Zeigt Systeminfos
```bash
uname -a           # Alle Infos
```

### `neofetch` – Coole Systemübersicht
```bash
neofetch           # Zeigt OS, RAM, CPU etc. schön an
```

### `free` – Zeigt RAM-Nutzung
```bash
free -h            # RAM in lesbarer Form (GB/MB)
```

### `df` – Zeigt Festplattenbelegung
```bash
df -h              # Speicherplatz aller Partitionen
```

### `ps/top/htop` – Zeigt laufende Prozesse
```bash
ps aux             # Alle Prozesse
top                # Live-Ansicht (wie Task-Manager)
htop               # Schönere Version von top
```

### `kill/pkill` – Beendet Prozesse
```bash
kill 1234          # Beendet Prozess mit PID 1234
pkill firefox      # Beendet alle Firefox-Prozesse
```

### `systemctl` – Verwaltet Systemd-Dienste
```bash
sudo systemctl start apache2   # Startet Apache
```

### `history` – Zeigt letzte Befehle
```bash
history            # Liste aller früheren Befehle
!37                # Führt Befehl Nr. 37 aus
```

### `reboot/shutdown` – Neustart oder Herunterfahren
```bash
sudo reboot        # Startet neu
sudo shutdown -h now  # Fährt sofort herunter
```

## 12. Textverarbeitung

### `awk` – Mächtiges Tool zur Textverarbeitung
```bash
awk '{print $1}' datei.txt  # Druckt die erste Spalte
```

## 13. Sonstiges

### `cal` – Zeigt einen Kalender
```bash
cal               # Kalender des aktuellen Monats
cal 2024          # Ganzes Jahr
```

### `resolvectl` – DNS-Abfragen
```bash
resolvectl status # Zeigt DNS-Konfiguration
```