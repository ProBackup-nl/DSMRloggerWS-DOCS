# \#define SHOW\_PASSWRDS

Met deze \#define geef je aan of je wilt dat de **PSK Key** van je WiFi netwerk en het **wachtwoord** van de gebruikte MQTT Broker zichtbaar worden.

Via telnet het opvragen van de Board Info:

```text
 B - Board Info
         .
         .
         .

==================================================================
               Board type [ESP8266_GENERIC]
                     SSID [A@nd@W@F@]
                  PSK key [**********]
               IP Address [192.168.1.108]
                 Hostname [DSMR-WS]
       Last reset reason: [Exception]
                   upTime [32(d):02:01]
==================================================================

```

en de Settings:

```text
 S - list Settings
         .
         .
         .

==== MQTT settings ==============================================
          MQTT broker URL/IP : hassio.local
                   MQTT user : hassUser1
               MQTT password : *************
          MQTT send Interval : 120
              MQTT top Topic : DSMR-WS

```

| Define | Functie |
| :--- | :--- |
| SHOW\_PASSWRDS | In de **System Info** tab wordt, als deze \#define actief is de **PSK Key** van het WiFi netwerk getoont. Bij de **B - Board Info** uitvoer wordt met deze deze \#define de **PSK Key** zichtbaar en bij **S - list Settings** het wachtwoord van de MQTT Broker. |

\[System Info\]  
![](https://mrwheel.github.io/DSMRloggerWS/img/DSMR-logger-PSK_Key.png)

