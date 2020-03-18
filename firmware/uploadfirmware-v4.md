# Firmware Flashen DSMR-logger v4

Versie 4 van de DSMR-logger hardware maakt gebruik van een ESP-12 processor. Deze processor zit op de printplaat van de DSMR-logger gesoldeerd en moet dus, op de printplaat, geflashed worden.

Om de firmware naar de **DSMR-logger Versie 4** te kunnen flashen moet deze eerst voor de ESP-12 geschikt worden gemaakt.

Breaking News!

 Er is ondertussen een nieuwere versie van de DSMR-logger firmware beschikbaar. Het grootste deel van deze documentatie is nog steeds van toepassing maar als je de DSMRloggerAPI firmware wilt gaan gebruiken kun je de informatie hierover in de volgende documenten vinden:

* Deze [post](https://willem.aandewiel.nl/index.php/2020/02/28/restapis-zijn-hip-nieuwe-firmware-voor-de-dsmr-logger/) op mijn website.
* Op [github](https://github.com/mrWheel/DSMRloggerAPI) kun je de meest actuele bestanden vinden.
* [Hier](https://github.com/mrWheel/DSMRloggerAPI/releases) kun je pré compiled binaries vinden.
* De officiële documentatie van de DSMRloggerAPI firmware kun je [hier](https://mrwheel-docs.gitbook.io/dsmrloggerapi/) vinden.

Dit doe je door in de ArduinoIDE de `#define`'s in het eerste tab-blad aan te passen.

Heb je géén Oled-display \(let op de twee _slashes_ voor `#define`'s van HAS\_OLED\_SSD1306 en HAS\_OLED\_SH1106!\):

```text
/******************** compiler options  ********************************************/
#define IS_ESP12                  // define if it's a 'bare' ESP-12 (no reset/flash functionality on board)
#define USE_UPDATE_SERVER         // define if there is enough memory and updateServer to be used
//  #define HAS_OLED_SSD1306          // define if a 0.96" OLED display is present
//  #define HAS_OLED_SH1106           // define if a 1.3" OLED display is present
//  #define USE_PRE40_PROTOCOL        // define if Slimme Meter is pre DSMR 4.0 (2.2 .. 3.0)
//  #define USE_NTP_TIME              // define to generate Timestamp from NTP (Only Winter Time for now)
#define USE_MQTT                  // define if you want to use MQTT
#define USE_MINDERGAS             // define if you want to update mindergas (also add token down below)
//  #define SM_HAS_NO_FASE_INFO       // if your SM does not give fase info use total delevered/returned
//  #define SHOW_PASSWRDS             // well .. show the PSK key and MQTT password, what else?
//  #define HAS_NO_METER              // define if No "Slimme Meter" is attached (*TESTING*)
/******************** don't change anything below this comment **********************/

```

Heb je wel een Oled-display op de DSMR-logger aangesloten dan moeten de compiler options worden aangepast door de twee _slashes_ voor het gebruikte type OLED display weg te halen \(in het voorbeeld hieronder is er een OLED scherm van het type SH1106 aangesloten\).

```text
/******************** compiler options  ********************************************/
#define IS_ESP12                  // define if it's a 'bare' ESP-12 (no reset/flash functionality on board)
#define USE_UPDATE_SERVER         // define if updateServer to be used and there is enough memory
//  #define HAS_OLED_SSD1306          // define if an OLED display is present
#define HAS_OLED_SH1106           // define if a 1.3" OLED display is present
//  #define USE_PRE40_PROTOCOL        // define if Slimme Meter is pre DSMR 4.0 (2.2 .. 3.0)
//  #define USE_NTP_TIME              // define to generate Timestamp from NTP (Only Winter Time for now)
#define USE_MQTT                  // define if you want to use MQTT
#define USE_MINDERGAS             // define if you want to update mindergas (also add token down below)
//  #define SM_HAS_NO_FASE_INFO       // if your SM does not give fase info use total delevered/returned
//  #define SHOW_PSK_KEY              // well .. show the PSK key, what else?
//  #define HAS_NO_METER              // define if No "Slimme Meter" is attached (*TESTING*)
/******************** don't change anything below this comment **********************/

```

Vervolgens moeten de `Boards` settings als volgt worden ingevuld:

|  | Instelling | Waarde |
| :--- | :--- | :--- |
|  | Board | "Generic ESP8266 Module" |
|  | Upload Speed | "115200" |
|  | CPU Frequency | "80MHz" |
|  | Flash Frequency | "40MHz" |
|  | Flash Mode | "DIO" of "DOUT \(compatible\)" |
|  | Flash Size | "4M \(1M SPIFFS\)" |
|  | Crystal Frequency | "26MHz" |
|  | Reset Method | "None" |
|  | Debug Port | "Disabled" |
|  | Debug Level | "None" |
|  | IwIP Variant | "v2 Lower Memory" |
|  | VTables | "Flash" |
|  | Exeptions | "Disabled" |
|  | Builtin Led | "2" |
|  | Erase Flash | "Only Sketch" \(First Time: "All Flash Contents"\) |
|  | Port | Bedraad: "Serial Port" |

Pas op!

 Als je de **Flash Mode** veranderd t.o.v. wat je gebruikt hebt voor de firmware die nu in de DSMR-logger zit en je doet een OTA update van de firmware, dan zal de Flash Mode niet veranderen!

## Firmware Bedraad Flashen <a id="firmware-bedraad-flashen"></a>

Pas op!

 Koppel de DSMR-logger los van de Slimme Meter vóórdat je de DSMR-logger op de programmer aansluit!!

Sluit de [USB-&gt;ESP12 programmer](../hardware_V4_Programmer/) aan op de `Program`-header van de _DSMR-logger v4_

1. Druk de `FLASH` knop in en houd deze ingedrukt
2. Druk op de `RESET` knop
3. Laat de `RESET` knop los
4. Laat de `FLASH` knop los

De _DSMR-logger v4_ staat nu in Flash-mode en blijft in die mode tot er gegevens vanaf de programmer naar de DSMR-logger zijn overgebracht óf tot je nog een keer op de `RESET` knop drukt.

Vergeet niet in de ArduinoIDE de `Port` te selecteren waarop je de USB-&gt;ESP12 programmer hebt aangesloten en druk op het _Compile and Upload_ icoon.

## Firmware _Over The Air_ Flashen <a id="firmware-over-the-air-flashen"></a>

Bij het _Over The Air_ flashen van de firmware of `data`-map kan de DSMR-logger v4 gewoon op de Slimme Meter aangesloten blijven.

Alle instellingen voor de DSMRloggerWS firmware blijven gelijk aan de bedraade methode van flashen.

Vervolgens moet je niet op het   `Compile & Upload`-Icoon     

klikken maar in het \[`Sketch`\] drop-down menu de keuze `Export Compiled Binary` selecteren.

De firmware wordt nu gecompileerd en in de Arduino Sketch map waar de DSMRloggerWS firmware ook staat neergezet. Het bestand heeft de extentie `.bin`.

Als de firmware gecompileerd is klik je op de DSMR-logger pagina op het  icoontje.

In de FSexplorer klik je op de knop `Update Firmware`

Er verschijnt nu een scherm waarin je een firmware bestand \(de naam eindigt op `.bin` met ergens in de naam ook `.ino.`\) kunt kiezen door op de bovenste knop `Choose File` te klikken.

Selecteer uit het `popUp scherm` dat nu verschijnt het binary file dat je wilt uploaden ..

.. klik op \[Choose\] en daarna op de knop `flash Firmware`

Na enige tijd krijg je de melding dat de upload is geslaagd en dat de DSMR-logger opnieuw opstart.

Let op!

 Het komt regelmatig voor dat het scherm niet automatisch ge-refreshed wordt \(dit lijkt te maken te hebben met de omvang van de firmware\). Klik in dat geval, na ongeveer 3 minuten, op de tekst

       Als het lijkt of er niets gebeurd, wacht dan ongeveer drie minuten en klik daarna **hier**.

 Als de verbinding met de server vóór die tijd verbroken wordt klik dan op de \`back\` knop van de browser waarna de tekst alsnog \(weer\) verschijnt. Klik nu op \*\*hier\*\* om de DSMRloggerWS hoofd pagina opnieuw te laden.

\[DSMR-PCB\]  


