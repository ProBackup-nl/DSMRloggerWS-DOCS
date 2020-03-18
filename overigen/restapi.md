# restAPI

Via de `restAPI` is het mogelijk om vanaf een extern systeem data uit de DSMRlogger op te halen.  
 Deze data wordt in `json` formaat afgeleverd.

De syntax is:

```text
    http://dsmr-ws.local/restAPI?get={ Actueel | Actual | DevInfo }
```

In plaats van `dsmr-ws.local` kun je ook het `IPadres` van de DSMR-logger gebruiken.

Let op!

**restAPI** is case-sensitive en moet precies zó geschreven worden of helemaal in lower-case \(**restapi**\).  
 De overige argumenten zijn niet case-sensitive \(**Get** of **gEt** en **Actual** of **aCtUaL** zijn gelijk\).

### Voorbeeld 1 <a id="voorbeeld-1"></a>

Om de actuele data uit de Slimme Meter op te halen gebruik je:

```text
    http://dsmr-ws.local/restAPI?get=Actueel
```

 Waarna je de volgende `json` string terug krijgt:

```text
{
   "Timestamp":"160717102501S"
  ,"Energy_Delivered":"96966.094"
  ,"Energy_Returned":"69198.641"
  ,"Gas_Delivered":"4756.104"
  ,"Energy_Delivered_Tariff1":"54210.770"
  ,"Energy_Delivered_Tariff2":"42755.324"
  ,"Energy_Returned_Tariff1":"27365.799"
  ,"Energy_Returned_Tariff2":"41832.840"
  ,"Energy_Tariff":"0002"
  ,"Power_Delivered":"4680"
  ,"Power_Returned":"1740"
  ,"Voltage_l1":"241.0"
  ,"Current_l1":"0"
  ,"Voltage_l2":"237.0"
  ,"Current_l2":"2"
  ,"Voltage_l3":"236.0"
  ,"Current_l3":"0"
  ,"Power_Delivered_l1":"2964"
  ,"Power_Returned_l1":"136"
  ,"Power_Delivered_l2":"1180"
  ,"Power_Returned_l2":"1696"
  ,"Power_Delivered_l3":"1536"
  ,"Power_Returned_l3":"70"
}
```

In plaats van `Actueel` kun je ook `Actual` gebruiken.

### Voorbeeld 2 <a id="voorbeeld-2"></a>

Om de Device Informatie van de Slimme Meter en de DSMR-logger op te halen gebruik je het volgende commando:

```text
    http://192.168.12.63/restapi?GET=DEVInfo
```

 Waarna je de volgende `json` string terug krijgt:

```text
{
   "Identification":"XMX5LGBBLB1234567890"
  ,"P1_Version":"50"
  ,"Equipment_Id":"453030xxxxxxxxxxxxxxxxxxxxxxxx3136"
  ,"Electricity_Tariff":"0002"
  ,"Gas_Device_Type":"3"
  ,"Gas_Equipment_Id":"47303xxxxxxxxxxxxxxxxxxxxxxxx23136"
  ,"Author":"Willem Aandewiel (www.aandewiel.nl)"
  ,"FwVersion":"v0.4.2 (May  5 2019)"
  ,"Compiled":"May  5 2019  19:31:28"
  ,"FreeHeap":12528
  ,"maxFreeBlock":5632
  ,"ChipID":"41e189"
  ,"CoreVersion":"2_5_0"
  ,"SdkVersion":"3.0.0-dev(c0f7b44)"
  ,"CpuFreqMHz":80
  ,"SketchSize":511.203
  ,"FreeSketchSpace":236.000
  ,"FlashChipID":"0014405E"
  ,"FlashChipSize_MB":1.000
  ,"FlashChipRealSize_MB":1.000
  ,"FlashChipSpeed_MHz":40.00
  ,"FlashChipMode":"DOUT"
  ,"BoardType":"ESP8266_GENERIC"
  ,"SSID":"thisWiFi"
  ,"IpAddress":"192.168.12.63"
  ,"WiFiRSSI":-51
  ,"Hostname":"DSMR-WS"
  ,"upTime":"9(d):20:57"
  ,"TelegramCount":162180
  ,"TelegramErrors":7
  ,"lastReset":"Software/System restart"
}
```

