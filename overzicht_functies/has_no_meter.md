# \#define HAS\_NO\_METER

Om te testen of de verwerking van de gegevens, die normaal gesproken uit de Slimme Meter komen, goed gaat kun je met deze \#define de firmware zó maken dat hij zélf voor \(test\) data zorgt. Om de tijd te versnellen zal de testdata eerst de maanden versneld laten voorbij gaan, daarna de dagen en tenslotte de uren.

{% hint style="info" %}
Let op!   
Alleen om te testen!
{% endhint %}

{% hint style="info" %}
Let op!   
Deze functie schakelt het versturen van berichten naar de MQTT broker uit
{% endhint %}

| \#define | Functie |
| :--- | :--- |
| HAS\_NO\_METER |  De DSMRloggerWS firmware zorgt zelf voor test-data. Als deze functionaliteit actief is moet de DSMR-logger **niet** op een Slimme Meter worden aangesloten! Omdat er geen daadwerkelijke telegrammen worden aangemaakt zullen er ook geen berichten naar de MQTT broker worden verstuurd! |

