# Home Automation

This is my setup, there's a pletora of variations.

- [Measuring moisture](#measuring-moisture)

---

## Measuring moisture

<img align="right" src="img/grafana01.png" alt="grafana01" width="350"/>

### Hardware

- Raspberry pi4
- ConBee II (on a USB extension cord - important)
- Xiaomi Aqara multi sensor

### Software

Everything on the same Raspberry Pi:
- [Home-assistant + Node-red (with big timer)](ha/README.md)
- [deCONZ](https://github.com/marthoc/docker-deconz)
- [InfluxDB & Grafana](https://github.com/Praqma/rasb-influxdb)
