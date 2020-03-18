# Overzicht - DSMRloggerWS

Tijdens het compileren van de firmware kun je bepaalde functionaliteit in- en uit-schakelen door de \#defines wél of níet door twee slashes \("//"\) vooraf te laten gaan.

In onderstaande tabel kun je zien of een bepaalde functionaliteit beschikbaar is voor de verschillende versies van de DSMR-logger.

| \#define | Functie | Versie 4 | Versie 3 |
| :--- | :--- | :--- | :--- |
| [IS\_ESP12](../Is_ESP12/) | Geeft aan of je de firmware voor een ESP12 of andere \(ESP-01\) processor compileren |  JA \(moet\) |  NEE |
| [USE\_UPDATE\_SERVER](../Use_Update_Server/) | Met de Update Server kun je vanuit de FSexplorer updates van de firmware installeren |  JA |  NEE |
| [HAS\_OLED\_SSD1306](../Has_OLED_SSD1306/) | Functionaliteit om \(status\) meldingen naar een OLED scherm \(0.96" type SSD1306\) te sturen |  JA |  NEE |
| [HAS\_OLED\_SH1106](../Has_OLED_SH1106/) | Functionaliteit om \(status\) meldingen naar een OLED scherm \(1.3" type SH1106\) te sturen |  JA |  NEE |
| [USE\_PRE40\_PROTOCOL](../Use_Pre40_Protocol/) | Voor "oude" Slimme Meters |  JA |  JA |
| [USE\_NTP\_TIME](../Use_NTP_Time/) | Gebruik de tijd van een NTP server i.p.v. die van de Slimme Meter |  JA |  JA |
| [SM\_HAS\_NO\_FASE\_INFO](../SM_Has_No_Fase_Info/) | Sommige één fase Slimme Meter's geven geen info per fase af |  JA |  JA |
| [USE\_MQTT](../Use_MQTT/) | Deze optie zorgt ervoor dat de functionaliteit voor het versturen van gegevens naar een MQTT broker wordt ingebouwd |  JA |  JA |
| [USE\_MINDERGAS](../Use_Mindergas/) | Deze optie zorgt ervoor dat de functionaliteit voor het versturen van gegevens naar [mindergas.nl](https://mindergas.nl/) waar je huidige gasverbruik kunt vergelijken met vorig jaar. |  JA |  NEE |
| [SHOW\_PASSWORDS](../Show_Passwrds/) | Of je de gebruikte passwords in het Systeem Info scherm en via telnet wilt tonen |  JA |  JA |
| [HAS\_NO\_METER](../Has_No_Meter/) | Als je geen Slimme Meter op de DSMR-logger hebt aangesloten |  JA |  JA |

```text

/******************** compiler options  ********************************************/
#define IS_ESP12                  // define if it's a 'bare' ESP-12 (no reset/flash functionality on board)
#define USE_UPDATE_SERVER         // define if there is enough memory and updateServer to be used
#define HAS_OLED_SSD1306          // define if an OLED display is present
//  #define HAS_OLED_SH1106           // define if an OLED display is present
//  #define USE_PRE40_PROTOCOL        // define if Slimme Meter is pre DSMR 4.0 (2.2 .. 3.0)
//  #define USE_NTP_TIME              // define to generate Timestamp from NTP (Only Winter Time for now)
//  #define SM_HAS_NO_FASE_INFO       // if your SM does not give fase info use total delevered/returned
#define USE_MQTT                  // define if you want to use MQTT
//  #define USE_MINDERGAS             // define if you want to update mindergas (also add token down below)
//  #define SHOW_PASSWRDS             // well .. show the PSK key and MQTT password, what else?
//  #define HAS_NO_METER              // define if No "Slimme Meter" is attached (*TESTING*)
/******************** don't change anything below this comment **********************/

```

