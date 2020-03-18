# preferencesIDE - DSMRloggerWS

Om het _Over The Air updaten_ van de firmware eenvoudig\(er\) te maken is het handig om altijd precies te weten waar de nieuw gecompileerde firmware door de IDE wordt neergezet.

Het standaard door de ArduinoIDE gebruikte `build-path` is min-of-meer random, maar in ieder geval is het standaard een steeds veranderende plek op je computer.

Gelukkig kún je het `build-path` ook op een door jou bepaalde vaste plek configureren.

Ga, in de ArduinoIDE, naar `Instellingen` of `Preferences`. Onder in het popUp scherm dat nu verschijnt staat het pad naar een tekst bestand waarin de ArduinoIDE allerlei gegevens bijhoudt.

Het gaat nu om de plek waar het `preferences.txt` bestand staat.  
 Sluit de ArduinoIDE af en open het `preferences.txt` bestand met een tekst-editor \(**niet met een tekst-verwerker!**\).

Ergens in het `preferences.txt` bestand staan deze instellingen die aangeven hoe je binaries worden _ge-build_ en waar ze worden neergezet.

```text
.
build.path=/Users/(YourLoginName)/Documenten/arduinoBuild
build.verbose=true
build.warn_data_percentage=75
.
.
```

Het gaat om de variabele `build.path`. Als deze niet in het `preferences.txt` bestand staat, raad ik je aan hem toe te voegen met een pad waar je makkelijk bij kunt komen zodat je Sketches altijd op dezelfde plek gecompileerd worden. Het maakt het leven een stukje eenvoudiger ;-\)

Let op!

 Pas het preferences.txt bestand **alleen** aan als de ArduinoIDE is afgesloten! De ArduinoIDE heeft deze preferences in zijn geheugen staan en overschrijft het preferences.txt bestand bij het afsluiten.

