# Firmware Flashen DSMR-logger v3 - DSMRloggerWS

Let op!

 De DSMR-logger Versie 3 maakt gebruik van een ESP-01 bordje met 1MB flash geheugen. Vanwege de omvang van de DSMRloggerWS firmware is deze alleen met beperkte functionaliteit geschikt om naar een ESP-01 te worden ge-upload. Met een ESP-01\(Black/S\) is het niet mogelijk om **Over The Air** updates van de firmware of SPIFFS te doen.  
 Ook de **RTS** hardware en de **I2C** interface \(oled-scherm\) zijn voor de ESP-01 niet beschikbaar.

Om de firmware naar de ESP-01 \(Black/S\) te kunnen flashen moet deze eerst voor de ESP-01 geschikt worden gemaakt.

Dit doe je door vóór de `#define`'s twee _slashes_ \(**//**\) te zetten. In de ArduinoIDE zien de regels na `/*** compiler options ***/` er dan zó uit:

```text
/******************** compiler options  ********************************************/
//  #define IS_ESP12                  // define if it's an ESP-12
//  #define USE_UPDATE_SERVER         // define if updateServer to be used and there is enough memory
//  #define HAS_OLED_SSD1306          // define if an OLED display is present
//  #define SM_GIVES_NO_TIMESTAMP     // define to generate Timestamp from NTP (Only Winter Time)
//  #define SHOW_PSK_KEY              // well .. show the PSK key, what else?
//  #define HAS_NO_METER              // define if No "Slimme Meter" is attached (*TESTING*)
/******************** don't change anything below this comment **********************/

```

Let op!

 Mocht je een ESP-01 bordje met een **PUYA** flash chip hebben, dan moet je nog wat doen om SPIFFS met deze PUYA chip te laten werken. Kijk [hier](../PUYA_patch/) wat je moet doen.

Vervolgens moeten de \[`Boards`\] settings als volgt worden ingevuld:

|  | Instelling | Waarde |
| :--- | :--- | :--- |
|  | Board | "Generic ESP8266 Module" |
|  | Upload Speed | "115200" |
|  | CPU Frequency | "80MHz" |
|  | Flash Frequency | "40MHz" |
|  | Flash Mode | "DOUT \(compatible\)" |
|  | Flash Size | "1M \(256K SPIFFS\)" |
|  | Crystal Frequency | "26MHz" |
|  | Reset Method | "None" \(afhankelijk van de gebruikte programmer\) |
|  | Debug Port | "Disabled" |
|  | Debug Level | "None" |
|  | IwIP Variant | "v2 Lower Memory" |
|  | VTables | "Flash" |
|  | Exeptions | "Disabled" |
|  | Builtin Led | ESP-01 \(Black\): "1" ESP-01S:         "2" |
|  | Erase Flash | "Only Sketch" \(First Time "All Flash Contents"\) |
|  | Port | Bedraad: "Serial Port" |

Stop de ESP-01 in de programmer \( [hier](https://willem.aandewiel.nl/index.php/2018/08/27/eenvoudige-programmer-voor-de-esp-01-esp8266/) vind je een post over hoe je van een USB to ESP-01 Adapter zelf eenvoudig een programmer kunt maken\) en sluit deze aan op je computer. Vergeet niet de juiste `Port` te selecteren en druk op het _Compile and Upload icoon_.

\[DSMR-Editor\]  


