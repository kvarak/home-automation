# Home Automation

This is my setup, there's a pletora of variations.

## Measuring moisture

### Hardware

- Raspberry pi4
- ConBee II (on a USB extension cord - important)
- Xiaomi Aqara multi sensor

### Software

Everything on the same Raspberry Pi:
- [Home-assistant + Node-red (with big timer)](ha/docker-compose.yml)
- [Phoscon GW](https://www.phoscon.de/en/conbee2)
- [InfluxDB & Grafana](https://github.com/Praqma/rasb-influxdb)
