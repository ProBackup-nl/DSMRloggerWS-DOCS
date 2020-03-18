# Integratie met Mindergas.nl

De data uit de DSMR-logger kan 1x per dag automatisch geupload worden naar de website Mindergas.nl. Deze website is in 2011 ontstaan uit de persoonlijke behoefte van David Hei Lei om te meten wat het effect is van woningisolatie op zijn gasverbruik [\(lees hier meer\)](https://mindergas.nl/about_us). De website maakt het eenvoudig mogelijk om je gasverbruik in te voeren en vervolgens te vergelijken op diverse manieren.

De website Mindergas.nl maakt het eenvoudig mogelijk om je jaarverbruik te vergelijken met een voorgaande periode \(jaren vergelijken\). Hierbij zorgt mindergas.nl voor de omrekening op basis van [gewogen graaddagen](https://mindergas.nl/degree_days_calculation/explanation). Door het gebruik van graaddagen krijg je een beter beeld van het daadwerkelijke verbruik, er wordt namelijk rekening gehouden met het feit of sprake is van een milde winter of een strenge winter. Hierdoor wordt het ook mogelijk om door de jaren heen je verbruik te vergelijken, er wordt immers rekening gehouden met de verschillen in temperaturen door de winters heen.

Doordat je je verbruik het hele jaar elke dag opvoert, kan op basis van voorspelling een vrij nauwkeurige jaarverbruik door het jaar heen worden voorspelt. Je kunt het verbruik vergelijken met voorgaande jaren. En daarnaast kan je je gasverbruik vergelijken met dat van anderen. Een handige functie als je bijvoorbeeld jouw verbruik wilt vergelijk met je buren, om te ontdekken of energiebezuinigende maatregelen effect hebben.

Bovendien kent Mindergas.nl een integratie met Pricewise waardoor je snel kunt vergelijken wat jouw energieverbruik bij andere energieleveranciers aan kosten met zich mee zou brengen. Handig als je wilt weten of het zinvol is om van energie leverancier te wisselen.

#### \#define USE\_MINDERGAS <a id="define-use_mindergas"></a>

| \#define | Functie |
| :--- | :--- |
| USE\_MINDERGAS | Door deze define wordt de mindergas integratie mee gecompileerd bij het maken van de firmware. Kijk ook [hier](https://mrwheel.github.io/DSMRloggerWS/Use_Mindergas/) |

#### Instellen van Mindergas.nl <a id="instellen-van-mindergasnl"></a>

Om mindergas in gebruik te nemen moet je allereerst een [account aanmaken](https://mindergas.nl/users/sign_up) bij de website van Mindergas.nl. Na het aanmaken van een nieuw account kan je [hier](https://mindergas.nl/member/api) een zogenaamde `API key` aanmaken.

Klik daar op de knop _Genereren_, dan zal er een Authenicatietoken worden aangemaakt. Er verschijnt dan een API authenicatietoken, zoiets als dit `Ahah%4JgongF7pwH92uN`. Dit token moeten je invoeren bij de Instellingen pagina van de DSRM-Logger.

Via `FSexplorer -> Edit instellingen -> Settings` kun je het authenicatietoken invullen voor gebruik van mindergas:

![img](https://mrwheel.github.io/DSMRloggerWS/img/DSMR-USE_MINDERGAS_Settings.png)

