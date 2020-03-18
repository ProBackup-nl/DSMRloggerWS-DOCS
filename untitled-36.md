# DSMR-logger V4 met ESP-12 - DSMRloggerWS

Met deze optie zal de DSMR-logger de Data Request pin van de Slimme Meter 'hoog' maken als hij een Telegram kan ontvangen. Na het ontvangen van een volledig Telegram zal de Data Request pin weer 'laag' worden gemaakt waardoor de Slimme Meter stopt met het sturen van Telegrammen.

Let op! Alleen voor DSMR-logger V4

 Deze functionaliteit werkt alleen in combinatie met een Versie 4 van de DSMR-logger. Met een DSMR-logger V2 of V3 bordje moet je deze optie niet activeren.

| \#define | Functie |
| :--- | :--- |
| IS\_ESP12 | Om gebruik te kunnen maken van de Data Request pin van de Slimme Meter. |

