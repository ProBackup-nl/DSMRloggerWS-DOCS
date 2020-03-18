# upload Data map naar DSMR-logger v3

De `data`-map van de DSMRloggerWS firmware kan alleen via een programmer naar de ESP-01 worden overgezet \(omdat de DSMRloggerWS firmware op de ESP-01 geen OTA functionaliteit heeft\).

Je kunt [hier](https://willem.aandewiel.nl/index.php/2018/08/27/eenvoudige-programmer-voor-de-esp-01-esp8266/) een uitvoerige post vinden over hoe je zelf een eenvoudige programmer voor de ESP-01 kunt maken en hoe je die vervolgens moet gebruiken om de firmware en de _DSMRloggerWS_ `data`-map naar de ESP-01 te uploaden.

Uiteraard kun je hiervoor ook iedere andere geschikte programmer gebruiken!

![](https://mrwheel.github.io/DSMRloggerWS/img/USB2ESP01-PrgrmrHack.png)

Als je de ESP-01 op de programmer hebt aangesloten en deze staat in "Flash-Mode" ga dan in de Arduino IDE naar `Tools` **-&gt;** `ESP8266 Sketch Data Upload`  


Let op!De lay-out van de **.csv** bestanden van de DSMRloggerWS firmware is niet compatibel met die van de DSMRlogger2HTTP firmware.  
Mocht je de, met de DSMRlogger2HTTP firmware opgebouwde, history willen bewaren, dan moet je deze bestanden éérst naar je computer uploaden \(dat kan via de **/onderhoud** pagina\).

SPIFFS wordt nu leeg gemaakt en alle bestanden in de `data`-map worden naar het SPIFFS overgezet.

Hierna zal de DSMR-logger normaal opstarten, maar met de nieuw SPIFFS inhoud.

Let op!Hou er rekening mee dat eventuele data-bestanden die al op SPIFFS stonden nu weg zijn! Als je ze niet kwijt wil moet je er eerst een kopie van maken op je computer en deze, na het flashen van SPIFFS weer terug zetten \(dat kan met de **DSMRlogger2HTTP** firmware met behulp van de **/onderhoud** pagina en bij de **DSMRloggerWS** firmware met de FSexplorer ![](https://mrwheel.github.io/DSMRloggerWS/img/FSexplorer.png)\)!

\[ChartJaar\]  


![](https://mrwheel.github.io/DSMRloggerWS/img/ChartJaar.png)[Next ](https://mrwheel.github.io/DSMRloggerWS/overzichtFuncties/)[ Previous](https://mrwheel.github.io/DSMRloggerWS/uploadFirmware_V3/)  


