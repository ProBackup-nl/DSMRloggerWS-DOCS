# Benodigd Bibliotheken - DSMRloggerWS

Voor de **DSMRloggerWS** firmware zijn de volgende bibliotheken nodig:

## dsmr <a id="dsmr"></a>

Deze library is ontwikkeld door _Matthijs Kooijman_ en vormt het hart van de DSMR-logger. Je kunt de bibliotheek hier [https://github.com/matthijskooijman/arduino-dsmr](https://github.com/matthijskooijman/arduino-dsmr) downloaden.  
 De firmware is getest met `Version 0.1 - Commit f79c906 on 18 Sep 2018` maar nieuwere versies zullen waarschijnlijk ook werken.

## TimeLib <a id="timelib"></a>

Deze is door _Paul Stoffregen_ ontwikkeld. Je kunt hem hier [https://github.com/PaulStoffregen/Time](https://github.com/PaulStoffregen/Time) downloaden.

## WiFiManager <a id="wifimanager"></a>

Je kunt de, door _Tzapu_ ontwikkelde, bibliotheek hier [https://github.com/tzapu/WiFiManager](https://github.com/tzapu/WiFiManager) downloaden.  
 De DSMR-logger firmware is getest met `version 0.14.0` van deze bibliotheek maar nieuwere versies zullen waarschijnlijk ook werken.

## TelnetStream <a id="telnetstream"></a>

Deze bibliotheek is door _Juraj Andrassy_ ontwikkeld. Je kunt deze bibliotheek hier [https://github.com/jandrassy/TelnetStream](https://github.com/jandrassy/TelnetStream) downloaden.  
 De firmware is getest met `version 0.0.1` maar nieuwere versies zullen waarschijnlijk ook werken.

**Let op:** De installatie van deze bibliotheek gaat net als de andere bibliotheken. Een update kan echter pas geïnstalleerd worden als éérst de map `TelnetStream-master` uit de map `Libraries` wordt verwijderd!

## WebSocketsServer <a id="websocketsserver"></a>

Deze bibliotheek is ontwikkeld door _Markus Sattler_ en je kunt hem hier [https://github.com/Links2004/arduinoWebSockets](https://github.com/Links2004/arduinoWebSockets/) downloaden.  
 De DSMR-logger firmware is getest met **Version 20.05.2015 -** [**commit 72731be**](https://github.com/Links2004/arduinoWebSockets/tree/72731beb10c18c6247c6b511f2f46a452ef293c3) **on 16 Jan 2019** maar nieuwere versies zullen waarschijnlijk ook werken.

## SSD1306Ascii <a id="ssd1306ascii"></a>

_William Greiman_ heeft deze bibliotheek ontwikkeld met in het achterhoofd minimaal gebruik van resources \(dus: een bibliotheek die weinig geheugen gebruikt\). Je kunt de bibliotheek hier [https://github.com/greiman/SSD1306Ascii](https://github.com/greiman/SSD1306Ascii) downloaden.  
 De DSMR-logger Firmware is getest met `Version 1.2.x - Commit 97a05cd on 24 Mar 2019` maar nieuwere versies zullen waarcshijnlijk ook werken.

## PubSubClient <a id="pubsubclient"></a>

_Nick O'Leary \(knolleary\)_ heeft deze bibliotheek ontwikkeld. Je kunt de bibliotheek hier [https://github.com/knolleary/pubsubclient](https://github.com/knolleary/pubsubclient) downloaden.

## ArduinoJson <a id="arduinojson"></a>

Copyright _Benoit Blanchon_ 2014-2019  
De DSMR-logger Firmware is getest met `Version 6.13.0` van ArduinoJson.  
Je kunt de bibliotheek hier [https://github.com/bblanchon/ArduinoJson.git](https://github.com/bblanchon/ArduinoJson/releases) downloaden.

## ModUpdateServer <a id="modupdateserver"></a>

Deze bibliotheek maakt het mogelijk om firmware en SPIFFS Over The Air te flashen naar de DSMR-logger.  
Deze bibliotheek is nodig vanaf versie 2.6.3 van de Arduino/ESP8266 core. Je kunt de bibliotheek hier [https://github.com/mrWheel/ModUpdateServer](https://github.com/mrWheel/ModUpdateServer) downloaden.

## dsmr30 <a id="dsmr30"></a>

Let op! Deze functionaliteit is slechts beperkt getest!

 Heb je een pré DSMR 4.0 Slimme Meter dan kun je deze toch aansluiten op de DSMR-logger maar moet je een aantal `define`'s in het eerste tab-blad aanpassen én je moet [deze](https://github.com/mrWheel/arduino-dsmr30) library installeren. Kijk ook [hier](../Use_Pre40_Protocol/).

## Overige libraries <a id="overige-libraries"></a>

Onderstaande libraries zijn onderdeel van de `ESP8266 Core` **en moeten dus niet handmatig geïnstalleerd worden**!

```text
* ESP8266WiFi    
* ESP8266WebServer
* WiFiUdp        
* ESP8266mDNS   
* FS           
* ArduinoOTA
```

\[DSMR-Chart Dag\]

