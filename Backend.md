# Backup

## Backup-Ziele und Datenträger

Für Datensicherungen können verschiedene Speichermedien und Geräte verwendet werden:

- **Externe Festplatten**: Diese bieten große Speicherkapazitäten und lassen sich einfach transportieren.
- **Netzwerkspeicher (NAS)**: Mit NAS-Geräten können Daten zentral gespeichert und über das Netzwerk abgerufen werden.
- **Cloud-Speicher**: Dienste wie Google Drive, Dropbox oder spezialisierte Backup-Dienste wie Backblaze ermöglichen eine sichere Speicherung über das Internet.
- **USB-Sticks**: Für kleinere Datenmengen sind USB-Sticks praktisch, jedoch bieten sie weniger Sicherheit und Haltbarkeit.
- **Optische Medien (DVDs, Blu-rays)**: Diese werden zunehmend seltener genutzt, da ihre Kapazität begrenzt ist und die Haltbarkeit nicht immer gewährleistet werden kann.
- **Magnetbänder**: Vor allem in großen Unternehmen und Rechenzentren sind Magnetbänder für Backups weiterhin sehr verbreitet.

## Kompressionsverfahren bei Backups

Für die Datensicherung kommen verschiedene Kompressionsmethoden zum Einsatz:

- **Lossless-Kompression (verlustfrei)**: Techniken wie ZIP oder GZIP komprimieren Daten, ohne dass dabei Informationen verloren gehen. Dies ist besonders wichtig, da Backups die vollständige Wiederherstellung der Daten erfordern.
- **Deduplizierung**: Diese Methode reduziert Redundanzen, indem identische Daten nur einmal gespeichert werden. Dadurch lässt sich der Speicherbedarf erheblich senken.
- **Inkrementelle Kompression**: Bei dieser Technik werden nur die Änderungen seit dem letzten Backup gesichert und komprimiert.

### Warum ist Kompression bei Image-Backups wichtig?

Bei einem Image-Backup wird das gesamte Dateisystem, inklusive ungenutztem Speicher, gesichert. Dies führt zu sehr großen Backup-Dateien. Durch Kompression wird die Dateigröße reduziert, was sowohl Speicherplatz spart als auch die Übertragungszeit verkürzt. Besonders bei Cloud-Backups oder langfristiger Archivierung sind geringere Größen entscheidend, um Kosten und Zeitaufwand zu minimieren.

---

## Arten der Datensicherung

### Vollsicherung, differenzielle Sicherung und inkrementelle Sicherung

- **Vollsicherung**: Es wird eine komplette Kopie aller Daten erstellt. Diese Methode erfordert den meisten Speicherplatz, da sämtliche Daten jedes Mal vollständig gesichert werden.
- **Differenzielle Sicherung**: Hier werden alle Änderungen seit der letzten Vollsicherung gesichert. Der Speicherbedarf wächst mit der Zeit, doch die Wiederherstellung geht schneller als bei inkrementellen Backups.
- **Inkrementelle Sicherung**: Nur die Änderungen seit dem letzten Backup werden gesichert (egal ob voll oder inkrementell). Diese Methode benötigt am wenigsten Speicherplatz, allerdings ist die Wiederherstellung aufwändiger, da mehrere Sicherungen kombiniert werden müssen.

### Notwendigkeit eines Vollbackups für differenzielle und inkrementelle Sicherungen

Ja, sowohl die differenzielle als auch die inkrementelle Sicherung setzen ein vollständiges initiales Vollbackup voraus. Ohne dieses gibt es keinen Referenzpunkt, von dem aus die Änderungen nachverfolgt werden können.

### Vor- und Nachteile der verschiedenen Methoden

- **Vollsicherung**
  - **Vorteile**: Einfach in der Verwaltung, schnelle Wiederherstellung.
  - **Nachteile**: Hoher Speicherbedarf, lange Sicherungsdauer.
- **Differenzielle Sicherung**
  - **Vorteile**: Schneller als Vollsicherungen, geringer Speicherbedarf.
  - **Nachteile**: Der Speicherbedarf wächst im Laufe der Zeit; jedoch schneller in der Wiederherstellung als inkrementelle Sicherungen.
- **Inkrementelle Sicherung**
  - **Vorteile**: Sehr effizient in Bezug auf Speicher und Dauer.
  - **Nachteile**: Langsamere und komplexere Wiederherstellung, da mehrere Sicherungen erforderlich sind.

---

## Block-Level vs. File-Level Backup

### Unterschiede zwischen Dateisystem-Ebene und Block-Ebene

- **File-Level Backup**: Hierbei werden einzelne Dateien und Ordner gesichert. Diese Methode ist besonders geeignet, wenn nur ausgewählte Dateien oder Verzeichnisse benötigt werden.
- **Block-Level Backup**: Dabei werden Daten auf der Ebene von Speicherblöcken gesichert. Diese Methode ist effizienter bei großen Datenmengen, da nur geänderte Speicherblöcke gesichert werden.

### Welche Methode eignet sich besser für ein Festplatten-Image und warum?

Für ein Festplatten-Image ist ein **Block-Level Backup** die bessere Wahl. Es sichert das gesamte Dateisystem, einschließlich ungenutzter Speicherblöcke, und bietet eine schnellere und effizientere Methode zur Sicherung großer Datenmengen.

### Welche Methode eignet sich besser für den Home-Ordner?

Für die Sicherung eines spezifischen Ordners, wie dem Home-Ordner, ist ein **File-Level Backup** besser geeignet. Es werden nur die relevanten Dateien und Ordner gesichert, was Speicherplatz spart und die Sicherung sowie Wiederherstellung beschleunigt.

---

## Hot Backup vs. Cold Backup

### Definition und praktische Einsatzzwecke

- **Hot Backup**: Ein Backup, das während des laufenden Betriebs erstellt wird. Es ist ideal für Systeme, die keine Ausfallzeiten tolerieren, wie z.B. Datenbanken oder Webserver.
  - **Einsatzbeispiele**: Sicherung einer laufenden Datenbank oder eines Webservers ohne Unterbrechung des Betriebs.

- **Cold Backup**: Ein Backup wird nur erstellt, wenn das System abgeschaltet ist. Diese Methode eignet sich für weniger kritische Systeme oder wenn die Konsistenz der Daten garantiert werden muss.
  - **Einsatzbeispiele**: Sicherung eines Fileservers während eines Wartungsfensters oder eines PCs am Ende des Arbeitstages.

---

## Datensicherungsstrategie

### Wie oft sollte man ein Backup durchführen?

Die Häufigkeit von Backups hängt von der Wichtigkeit der Daten ab. Wichtige Daten sollten täglich gesichert werden, während weniger kritische Daten wöchentlich oder monatlich ausreichend gesichert werden können.

### Auf wie vielen verschiedenen Datenträgern sollte man Backups aufbewahren?

Die **3-2-1-Regel** empfiehlt, dass Sie drei Kopien Ihrer Daten auf zwei verschiedenen Medien aufbewahren sollten, wobei eine Kopie an einem externen Ort (z.B. in der Cloud oder an einem anderen physischen Standort) gespeichert wird.

### Weitere Begriffe zur Recherche

- **Turm von Hanoi**: Eine Strategie für die Rotation von Backups, bei der mehrere Medien nach einem festgelegten Plan verwendet werden, um eine langfristige Aufbewahrung von verschiedenen Backup-Generationen sicherzustellen.
- **3-2-1-Regel**: Eine bewährte Methode zur Datensicherung, bei der alle Daten **3** Kopien auf **2** verschiedenen Medien haben und **1** Kopie extern gespeichert wird.
