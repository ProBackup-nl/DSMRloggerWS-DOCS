# SM geeft geen info per Fase

Sommige \(vaak pré DSMR 4.0\) meters die geschikt zijn voor één fase, geven geen Fase Informatie via recordtype "1-0:x1.7.0" en "1-0:x2.7.0" door, waardoor de DSMRloggerWS firmware geen data voor de "Actueel" chart ontvangt. Met deze optie wordt de informatie uit de "1-0:1.7.0" en "1-0:2.7.0" records in de fase records gestopt.

| \#define | Functie |
| :--- | :--- |
| SM\_HAS\_NO\_FASE\_INFO |  De velden **PowerDelivered\_l1** en **PowereReceived\_l1** worden, respectievelijk, gevuld met de waarden van de **PowerDelivered** en **PowerReceived** velden. |

