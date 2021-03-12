# Home Automation

This is my setup, there's a pletora of variations.

- [Measuring moisture](#measuring-moisture)

---

## Measuring moisture

### Hardware

- Raspberry pi4
- ConBee II (on a USB extension cord - important)
- Xiaomi Aqara multi sensor

### Software

Everything on the same Raspberry Pi:
- [Home-assistant + Node-red (with big timer)](ha/docker-compose.yml)
- [deCONZ](https://github.com/marthoc/docker-deconz)
- [InfluxDB & Grafana](https://github.com/Praqma/rasb-influxdb)
