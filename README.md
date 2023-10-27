# tkn Solar Dashboard

The Grafana dashboard I use for my PV tracking, layout copied from markusdd.

- this is not fancy or parameterized, so you will have to adjust the queries to match the params in your database
  - I write the units to InfluxDB as main selector (A, V, W, kWh, Wh, etc.)
  - then I use the entity_id to select which parameter out of the unit pool I want
- in my setup the Sun data is written to the InfluxDB by HomeAssistant, you can also use Grafanas Sun&Moon plugin to achieve the same
- the solar data is gathered via OpenDTU from Hoymiles Inverter and sent to HomeAssistant via MQTT, from there I write select data to InfluxDB
- the electricity meter data is gathered through a powerfox poweropti, pulled via web-API in HomeAssistant, from there I forward some data to InfluxDB
- Powerfox integration from simon42 
