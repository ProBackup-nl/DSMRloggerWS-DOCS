# Clonen Firmware

De **DSMRloggerWS** firmware staat hier [https://github.com/mrWheel/DSMRloggerWS](https://github.com/mrWheel/DSMRloggerWS).

Er zijn twee manieren om de firmware te clonen.

1. download de repository als een `.zip` file
2. gebruik `git`

Als je niet handig bent met `git` raad ik je aan de repository als een `.zip` file te downloaden.

#### Download .zip file <a id="download-zip-file"></a>

![](https://mrwheel.github.io/DSMRloggerWS/img/GIT_Clone1.png)

Klik op de groene knop \[Clone or Download\] ..

![](https://mrwheel.github.io/DSMRloggerWS/img/GIT_Clone2.png)

.. en selecteer \[Download ZIP\]

Er volgt een scherm als dit:

![](https://mrwheel.github.io/DSMRloggerWS/img/GIT_SaveZIP.png)

1. Bewaar het `.zip` bestand op een plek op je computer waar je hem terug kunt vinden.
2. Unzip het `DSMRloggerWS-master.zip` bestand in de ArduinoIDE `Sketchbook Location`.
3. Rename de map `DSMRloggerWS-master` naar `DSMRloggerWS` \(dus zonder `-master`\)

Ga verder naar [DSMRloggerWS Sketch openen](https://mrwheel.github.io/DSMRloggerWS/clonenFirmware/#dsmrloggerws-sketch-openen)

#### git clone <a id="git-clone"></a>

Om de repository met `git` te kunnen clonen moet je er éérst voor zorgen dat je `git` op je systeem hebt staan. Hoe je dat moet doen valt buiten de scope van deze documentatie maar [hier](https://git-scm.com/book/nl/v1/Aan-de-slag-Git-installeren) kun je alles vinden over hoe je dit, voor jouw systeem, moet doen.

Voor nu ga ik ervan uit dat je `git` op je systeem hebt staan en dat je weet hoe je ermee moet werken.

Ga naar de Arduino `Sketchbook location` \(de map waar al je Sketches in staan, [kijk hier](https://mrwheel.github.io/DSMRloggerWS/installatieESP8266core/)\) en toets het volgende commando in:

```text
git clone https://github.com/mrWheel/DSMRloggerWS.git
```

That's it!

In `Sketchbook location` staat hierna een nieuwe map met de naam `DSMRloggerWS`.

#### DSMRloggerWS Sketch openen <a id="dsmrloggerws-sketch-openen"></a>

Start de ArduinoIDE _**opnieuw**_ op en klik op het `open` icoon![](https://mrwheel.github.io/DSMRloggerWS/img/IDE_Load-a.png).

Selecteer in het `drop-down` menu ..

![](https://mrwheel.github.io/DSMRloggerWS/img/IDE_Load-b.png)

.. de sketch `DSMRloggerWS`  
Er verschijnt een nieuw editor window met de firmware van de DSMRlogger!

![](https://mrwheel.github.io/DSMRloggerWS/img/IDE_Load-c.png)

