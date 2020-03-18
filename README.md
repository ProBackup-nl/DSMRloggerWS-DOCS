# Introductie - DSMRloggerWS

Je vindt hier de documentatie voor het project DSMR-logger \(Versie 4\).

De DSMR-logger is een hardware en software systeem waarmee de Slimme Meter \(vanaf _DSMR_ versie 4.0\) kan worden uitgelezen. De uitgelezen data \(telegrammen\) worden in de DSMR-logger opgeslagen en kunnen in de vorm van tabellen en charts, via WiFi, op een computer of tablet worden weergegeven.

Begrippen

 In dit document worden de volgende begrippen gebruikt:

| Begrip | Omschrijving |
| :--- | :--- |
| DSMR |  [Dutch Smart Meter Requirements](https://nl.wikipedia.org/wiki/Slimme_meter) De [DSMR-specificatie](https://www.netbeheernederland.nl/_upload/Files/Slimme_meter_15_a727fce1f1.pdf) is een afgeleide van de NTA 8130-normering. De DSMR-logger \(V3 en V4\) is ontworpen voor de DSMR versie 4.0 of hoger. Versie 4 geeft aan dat de Slimme Meter op de P1-poort 5 volt bij 250mA moet kunnen leveren \(zie pagina 8 en 9 van de specificatie\). Deze spanning wordt door de DSMR-logger gebruikt om de elektronica te voeden. |
| DSMR-logger | de Hardware |
| DSMR-logger v2 \(of Versie 2\) | Versie 2 van de Hardware Dit is de hardware van de DSMR-logger die is uitgerust met een **ESP-01 \(Black/S\)** bordje. Voor deze versie is de firmware DSMRlogger2HTTP bedoeld maar DSMRloggerWS is, met beperkte functionaliteit, ook geschikt te maken voor deze versie van de hardware. |
| DSMR-logger v3 \(of Versie 3\) | Versie 3 van de Hardware Verder gelijk aan Versie 2. |
| DSMR-logger v4 \(of Versie 4\) | Versie 4 van de Hardware Deze hardware is de basis voor dit project |
| DSMR-logger v4.5 \(of Versie 4.5\) | Versie 4.5 van de Hardware Deze hardware is een verbetering van de v4 hardware. Standaard heeft deze hardware een 5Volt DC Jack-Plug voor gebruik van een externe voeding en een jumper om de voeding te selecteren vanuit de Slimme Meter of de Jack-Plug. Bij gebruik van de Jack-Plug wordt de 5Volt van de Slimme Meter ontkoppelt. De draadbruggen voor de selectie van de signalen naar een OLED display zijn nu standaard \[GND,3v3,SCL,SDA\] maar deze kunnen, door de verbindingen aan de achterkant van de PCB door te snijden, ook aangepast worden. |
| DSMRloggerWS | De firmware voor de DSMR-logger v4 Deze firmware maakt intensief gebruik van webSockets. Let op! De firmware heeft geen streepje \(-\) tussen "DSMR" en "logger" |
| ESP-12 | Een bordje met een ESP8266 processor en **4MB** Flash Geheugen Dit bordje wordt gebruikt in de DSMR-logger v4 |
| ESP-01 \(Black\) | Een **ESP-01** met **1MB** flash geheugen Dit bordje heeft een rode Power Led en een blauwe Led op **GPIO-01** |
| ESP-01S | Een **ESP-01** met **1MB** flash geheugen Dit bordje heeft alleen een blauwe Led op **GPIO-02** |
| ESP-01\(Black/S\) | Als een '**ESP-01 Black**' of '**ESP-01S**' wordt bedoelt maar niet een '**ESP-01**'. DSMR-logger v2 en v3 maken gebruik van dit bordje |
| ESP-01 | Een bordje met een ESP8266 processor en 512KB flash geheugen Dit bordje is **niet** geschikt voor dit project |
| PUYA | PUYA is een fabrikant van flash chips die op verschillende soorten ESP-01 bordjes wordt gebruikt. Deze chips voldoen niet aan de eisen en hebben voor veel problemen gezorgd. Er is wel een compiler-optie die het gebruik van deze chip mogelijk maakt maar dit werkt helaas niet in alle gevallen. Het wordt afgeraden deze flash chip met DSMRloggerWS te gebruiken. |

Een volledige beschrijving van dit project kun je [hier](https://willem.aandewiel.nl/index.php/2019/04/09/dsmr-logger-v4-slimme-meter-uitlezer/) vinden.

\[DSMRlogger v4\]  


