# Fullduplex 8-Bit Nachrichtenübertragung

## Aufgabenstellung

Ziel dieses Projekts ist die Implementierung einer voll-duplexfähigen 8-Bit-Nachrichtenübertragung über Kabel zwischen zwei Systemen. Die Kommunikation erfolgt paketbasiert, wobei jedes Zeichen in zwei 4-Bit-Pakete aufgeteilt und mit Start-/End-Bits sowie Escaping übertragen wird. Zur Fehlererkennung wird eine CRC8-Prüfsumme verwendet. Das Projekt enstand im Rahmen des Modul 'Hardwarepraktikum' als Gruppenarbeit zweier Bachelorstudenten.

## Funktionsweise

- **Initialisierung:** Beide Systeme synchronisieren sich über ein Startsignal.
- **Übertragung:** Zeichen werden aus einer Textdatei eingelesen, in Pakete zerlegt, ggf. escaped und nacheinander gesendet.
- **Empfang:** Pakete werden empfangen, zusammengesetzt und ausgegeben.
- **Fehlererkennung:** Nach der Übertragung wird eine CRC8-Prüfsumme gesendet und geprüft.
- **Ende:** Die Übertragung wird mit einem definierten Endsignal abgeschlossen.

## Dateien

- [`main.cpp`](main.cpp): Hauptprogramm mit Implementierung der Übertragungslogik.
- [`Protokoll.pdf`](Protokoll.pdf): Protokoll.

## Protokoll-inhalte
- Vorüberlegungen (Theorie)
- Programmablaufs-Plan
- Code

## Hinweise

- Die Hardware besteht aus zwei B15f-Boards, siehe [B15f](https://github.com/devfix/b15f?tab=readme-ov-file)
- Die Hardware-Anbindung erfolgt über die `b15f`-Bibliothek.
- Die Übertragung kontrolliert Übertragungsfehler durch das verwendete CRC8.
- Das Protokoll unterstützt Escaping für Steuerzeichen und spezielle Bitmuster.

## Autoren
- Max
- L. P.