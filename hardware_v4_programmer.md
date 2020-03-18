# Programmer DSMR-logger v4

Er zijn verschillende manieren om de DSMR-logger van \(nieuwe\) firmware te voorzien. Dit gaat het eenvoudigst _Over The Air_ \(OTA\) maar de eerste keer zal dit altijd bedraad moeten.

* [FTDI-adapter](https://mrwheel.github.io/DSMRloggerWS/hardware_V4_Programmer/#ftdi-adapter)
* [USB to Serial adaptor bordje](https://mrwheel.github.io/DSMRloggerWS/hardware_V4_Programmer/#usb-to-serial-adaptor-bordje)
* [USB to TTL adaptor kabel](https://mrwheel.github.io/DSMRloggerWS/hardware_V4_Programmer/#usb-to-ttl-serial-adaptor-kabel)
* [Flashen \(programmeren\)](https://mrwheel.github.io/DSMRloggerWS/hardware_V4_Programmer/#flashen-programmeren)

#### FTDI-adapter <a id="ftdi-adapter"></a>

Verreweg de betrouwbaarste oplossing is om gebruik te maken van een FTDI adaptor zoals de [FTDI-basic](https://opencircuit.nl/Product/15140/SparkFun-FTDI-Basic-Breakout-5V) van Adafruit.  
Hou er rekening mee dat de USB-connector op de FTDI-basic geen _micro_-USB is maar de iets grotere _mini_-USB variant!

![](https://mrwheel.github.io/DSMRloggerWS/img/Sparkfun_FTDI-basic_5v.png)

Standaard wordt deze als 5Volt adaptor geleverd, maar aan de achterkant kun je, door het spoor tussen de middelste pad en de 5V pad te onderbreken en een soldeer brug aan te brengen tussen de middelste pad en de 3.3V pad, de adaptor geschikt maken voor 3v3.

![](https://mrwheel.github.io/DSMRloggerWS/img/Sparkfun_FTDI_Back.png)

Je moet de volgende verbindingen maken:

| FTDI-basic | DSMR-logger | Opmerking |
| :--- | :--- | :--- |
| 5V | 3v3 | LET OP! **3v3** |
| GND | GND |  |
| TXO | RxD |  |
| RXI | TxD |  |

![](https://mrwheel.github.io/DSMRloggerWS/img/DSMR-logger_V4-FTDI.png)

#### USB to Serial adaptor bordje <a id="usb-to-serial-adaptor-bordje"></a>

Ook een [USB-to-Serial adapter](https://opencircuit.nl/Product/11544/ESP-01-USB-Adapter) is eenvoudig als programmer te gebruiken door met vier draadjes verbinding tussen de USB-to-Serial Adapter en de _DSMR-logger v4_ te maken volgens onderstaand schema:

![](https://mrwheel.github.io/DSMRloggerWS/img/USB2Serial_DSMRlogger_v4.png)

~~Let op! Het heeft er alle schijn van dat dit bordje niet meer '_gezien_' wordt onder **MacOS 10.14**!~~

#### USB to TTL Serial adaptor kabel <a id="usb-to-ttl-serial-adaptor-kabel"></a>

Ook [deze](https://opencircuit.nl/Product/12809/USB-to-TTL-Serial-Cable-Debug-Console-Cable-for-Raspberry-Pi) USB-to-Serial kabel is eenvoudig als programmer te gebruiken alleen moet je er rekening mee houden dat de geleverde spanning **5 volt** is en je deze dus niet op de programming poort van de DSMR-logger V4 mag aansluiten.  
Sluit de USB-to-Serial kabel op deze manier aan om zonder problemen de DSMR-logger V4 te kunnen programmeren.

![](https://mrwheel.github.io/DSMRloggerWS/img/USB2TTL_5Volt_DSMR-logger.png)

#### Flashen \(programmeren\) <a id="flashen-programmeren"></a>

Omdat de DSMR-logger V4 geen aansluitingen voor specifieke controle signalen heeft moet je in de ArduinoIDE aangeven dat je bij het uploaden van firmware of de `data`-map geen speciaal protocol gebruikt. In het `Tools`-menu geef je bij `Reset Method` _**None**_ op.

![](https://mrwheel.github.io/DSMRloggerWS/img/ToolsResetMode.png)

Om nu de firmware of de `data`-map naar de _DSMR-logger v4_ te flashen moet je de _DSMR-logger v4_ _**eerst**_ in `Flash-mode` zetten.

Let op!Koppel, vóórdat je de programmer op de DSMR-logger v4 aansluit, éérst de Slimme Meter los!

Dit doe je door achtereenvolgens deze handelingen uit te voeren:

1. Druk op de `FLASH` knop en houdt deze ingedrukt
2. Druk vervolgens op de `RESET` knop
3. Laat de `RESET` knop los
4. Laat als laatste de `FLASH` knop los

De DSMR-logger staat nu in `Flash-mode` en blijft in die mode tot er firmware of de inhoud van de `data`-map wordt ge-upload \(of tot je nog een keer op de `RESET` knop drukt\).

Hierna hoort de DSMR-logger normaal op te starten. Mocht dit niet het geval zijn druk dan 1x op de `RESET` knop..

Zie ook [`Vraag en Antwoord`](https://mrwheel.github.io/DSMRloggerWS/QenA/#5-volt-programmer)

\[ChartActueel\]![](https://mrwheel.github.io/DSMRloggerWS/img/ChartActueel.png)

