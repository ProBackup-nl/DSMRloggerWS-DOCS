# Gebruik mindergas.nl - DSMRloggerWS

Met deze optie wordt de functionaliteit om gasverbruik naar [mindergas.nl](https://mindergas.nl/) te sturen geactiveerd.

Via `FSexplorer -> Edit instellingen -> Settings` kun je het jouw toegekende authorisatie token invoeren.

| Rubriek | Functie |
| :--- | :--- |
| Mindergas Authenticatie Token | Bij aanmelding bij mindergas.nl kun je een zgn. **Authenticatie Token** opvragen. Dit token heb je nodig om data naar mindergas.nl te kunnen uploaden. Voer dit token hier in. |

**Lees ook** [**dit**](../integratieMindergas/).

Let op!     \(DSMR-logger V3\)

 Deze functie is niet beschikbaar op een DSMR-logger versie 2 of 3 bordje!

| \#define | Functie |
| :--- | :--- |
| USE\_MINDERGAS | Deze define zorgt ervoor dat de Firmware één maal per dag het gasverbruik uit de Slimme Meter naar **mindergas.nl** zal sturen. |

