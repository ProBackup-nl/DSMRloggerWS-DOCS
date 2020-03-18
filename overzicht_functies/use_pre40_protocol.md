# \#define USE\_PRE40\_PROTOCOL

Vanaf versie 0.4.5 kan de DSMRloggerWS firmware ook overweg met Slimme Meters die nog niet aan de DSMR 4.0 standaard voldoen.

{% hint style="info" %}
Let op!   
Deze functionaliteit is slechts beperkt getest!  
Met dank aan Jordy voor het testen met een DSMR 2.2 meter!  
Mocht je meer informatie kunnen geven over eventuele problemen neem dan contact met mij op \(plaats een comment op mijn website\)
{% endhint %}

Om de DSMRloggerWS firmware geschikt te maken voor een pré DSMR 4.0 Slimme Meter zijn er een aantal opties mogelijk \(zie de \#define tabel hieronder\) die mogelijk van toepassing zijn op pré DSMR 4.0 Slimme Meters.

Om deze functionaliteit te kunnen gebruiken moet je ook de speciaal gehackte [arduino-dsmr30](https://github.com/mrWheel/arduino-dsmr30) bibliotheek installeren!

| \#define | Functie |
| :--- | :--- |
| USE\_PRE40\_PROTOCOL | Deze define zorgt ervoor dat de instellingen voor de seriële poort goed worden gezet \(9600, SERIAL\_7E1\). tevens wordt een speciaal gehackte 'arduino-dsmr' bibliotheek gebruikt omdat het pré DSMR 4.0 protocol geen checksum heeft. |
| USE\_NTP\_TIME | Het pré DSMR 4.0 protocol geeft niet altijd een timestamp \(0-0:1.0.0\). Doet jouw Slimme Meter dat ook niet, dan wordt met deze define de tijd via het NTP protocol gebruikt. Vooralsnog alleen Winter Tijd! |
| SM\_HAS\_NO\_FASE\_INFO | Heb je een Slimme Meter die geen verbruik per fase \(1-0:x1.7.0 enz.\) door geeft, dan kun je met deze optie er toch voor zorgen dat de Actuele chart informatie geeft over je verbruik |

