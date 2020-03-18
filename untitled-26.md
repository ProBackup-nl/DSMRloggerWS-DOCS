# ESP8266 Core - DSMRloggerWS

In de Arduino IDE moet bij “Instellingen” de volgende URL worden ingevoerd achter “_Additional Boards Manager URL’s:_” \(zie rood omlijnde kader\)

`https://arduino.esp8266.com/stable/package_esp8266com_index.json`

Lees vooral de uitleg in het [`README.md`](https://github.com/esp8266/Arduino/blob/master/README.md) bestand en de uitgebreide [`documentatie`](https://arduino-esp8266.readthedocs.io/en/latest/) op hun website!

Er kunnen meer additional board manager URL’s worden ingevuld. Je moet ze dan achter elkaar zetten en scheiden door een komma \(**,**\).

Eventueel kun je ook het pad waar je projecten staan \(de `Sketchbook Location`\) aanpassen. Standaard verwijst deze naar je `Documenten` map:

`C:\Users\<YourLoginName>\Documents\arduino\`

.. en dat is een prima plek!

De andere instellingen kun je naar behoefte aanpassen. Hierboven staan de instellingen die ik prettig vind.

Na het maken van aanpassingen klik je op \[OK\].

Ga nu via de ArduinoIDE menu-balk naar \[`Tools`\] -&gt; \[`Board`\] -&gt; \[`Boards Manager`\].

Voer bij filter “esp8266” in.

Selecteer de versie die je wilt gaan gebruiken en klik op \[`Install`\].

Let op!

 De DSMRloggerWS firmware v1.0.3 en v1.0.4 zijn getest met **versie 2.5.0** en met **versie 2.5.2** van de Arduino/ESP8266 core.

 Ondertussen is versie \(1.0.5\) geschikt gemaakt voor **versie 2.6.3** van de ESP8266 core. De oudere versies van de core zijn niet compatible met de DSMRloggerWS v1.0.5 firmware!

\[DSMR-Uur\]

