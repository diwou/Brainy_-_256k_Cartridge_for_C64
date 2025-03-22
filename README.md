# BRAINY – 256KB Cartridge für den Commodore C64

Dies ist eine Replik einer **256KB EPROM-Karte** für den Commodore C64.

![](https://codeberg.org/diwou/Brainy_-_256k_Cartridge_for_C64/raw/branch/main/Images/brainy256.jpg)

Die Zeitschrift **"64'er"** fasste das Projekt folgendermaßen zusammen:

> **"Brainy ist eine neue Generation von EPROM-Modulkarten.  
> Im Gegensatz zu den bisher vorgestellten Modulen wird hier der gesamte EPROM-Speicherplatz genutzt.  
> Brainy wird jedem Anfänger oder fortgeschrittenen Benutzer empfohlen, der es leid ist, ewig darauf zu warten,  
> dass längere Programme von Diskette geladen werden. Die beiliegende Diskette enthält einen sehr übersichtlichen  
> Modul-Generator, der automatisch alle notwendigen Einstellungen für die Karte vornimmt."**

---

## Zusammenbau

Die Karte besteht ausschließlich aus **THT-Bauteilen** (Durchsteckmontage).  
Einige Widerstände, Kondensatoren und eine Diode befinden sich unter den ICs.

Da die Platine in ihrer ursprünglichen Form reproduziert wurde, sind die Lötpads und Leiterbahnen entsprechend groß dimensioniert und leicht zu verarbeiten.

Der Zusammenbau erfolgt unkompliziert, eine Bestückungsliste liegt im Repository bei.

---

## Funktionsweise

Die Brainy-Cartridge nutzt ein **Bank-Switching**-Verfahren, um den gesamten 256KB großen EPROM-Speicherbereich effektiv zu adressieren.

Ein Adress-Decoder sorgt in Kombination mit den Steuerleitungen des C64 für das dynamische Ein-/Ausblenden der Speicherbereiche.  
Dies geschieht abhängig von der aktuell aufgerufenen Speicheradresse.

Der modulare Aufbau erlaubt das Umschalten einzelner 8KB-Blöcke, sodass verschiedene Programme oder Datenbereiche parallel geladen werden können.

Die Steuerung erfolgt teils automatisch durch das Betriebssystem des C64 bzw. manuell durch eigenen Programmcode (z. B. Assembler).

---

## Software

Zum Projekt gehörte ein **Modul-Generator**, der es erlaubt, einzelne Programme im EPROM zu organisieren.  
Damit können Startadressen, Titel und Blöcke komfortabel definiert werden.

Die zugehörige Diskette enthielt sowohl Tools zum Erstellen als auch zum Brennen der EPROM-Inhalte.  
In modernen Umgebungen kann man dies mit Tools wie z. B. CBM prg Studio oder einem HEX-Editor übernehmen.

---

## Stückliste (BOM)

| Bezeichnung | Anzahl | Beschreibung                       |
|-------------|--------|------------------------------------|
| EPROM       | 1x     | 27C020 oder 27C040 (je nach Konfig) |
| TTL-ICs     | 6x     | 74LS00, 74LS02, 74LS138, etc.      |
| Diode       | 1x     | 1N4148                             |
| Widerstände | div.   | z. B. 1kΩ, 4.7kΩ                    |
| Kondensator | 100nF  | Entkopplung                        |
| Fassung     | 28/32p | für EPROM                          |
| Platine     | 1x     | Brainy-Layout                      |

---

## Hinweise

Die Platine richtet sich primär an:

- Retro-Fans,
- Hardwarebastler,
- Sammler und
- Programmierer.

Die Platine bietet eine kompakte und stabile Lösung für eigene Anwendungen, Spiele oder Utilities.

---

## Lizenz

Der Inhalt dieses Repositories steht unter folgender Lizenz:

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)**  
Der vollständige Lizenztext befindet sich in der Datei [LICENSE.CC-NC-BY-SA-4.0](https://codeberg.org/diwou/Brainy_-_256k_Cartridge_for_C64/raw/branch/main/LICENSE.CC-NC-BY-SA)  
Und ist auch online verfügbar unter: https://creativecommons.org/licenses/by-nc-sa/4.0/

