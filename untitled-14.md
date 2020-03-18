# Over The Air update - DSMRloggerWS

Met deze optie wordt het mogelijk om nieuwe Firmware naar de DSMR-logger te flashen door in de FSexplorer op de knop \[Update Firmware\] te klikken

en vervolgens in de Flash Utility ..

.. op \[ChooseFile\] te klikken en daarna op \[Flash Firmware\]

Let op! Alleen voor ESP-12

 Deze functionaliteit werkt alleen als je 4MB flash geheugen hebt. Standaard heeft iedere ESP-12 dat.  
Je kunt een ESP-01 eventueel upgraden naar 4MB door de aanwezige flash chip te vervangen door een W25Q32FVSIG 32Mbit flash chip.

## Enable Format SPIFFS <a id="enable-format-spiffs"></a>

Je kunt de \[Format SPIFFS\] knop enabelen door een bestand met de naam `!format` te uploaden. Let wel: Met het formatteren van het SPIFFS file systeem raak je álle bestanden die daar opstaan kwijt!

| \#define | Functie |
| :--- | :--- |
| USE\_UPDATE\_SERVER | Om gebruik te kunnen maken van zgn. "Over The Air" \(OTA\) updates van de firmware en het SPIFFS file systeem moet je deze optie activeren. Dit kan alleen met een ESP-12 of een, met **4MB chip ge-upgrade** ESP-01 bordjes! '**Normale**' \(1MB\) ESP-01 bordjes hebben hier niet genoeg flash-geheugen voor. |

