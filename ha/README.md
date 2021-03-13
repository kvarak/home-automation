# Home Assistant

`docker-compose.yml`
```yml
version: '3.7'
services:
  home-assistant:
    container_name: home-assistant
    image: homeassistant/home-assistant:0.115.0
    #image: homeassistant/home-assistant:stable
    network_mode: "host"
    restart: always
    volumes:
      - /home/pi/repos/home-assistant/config/:/config
      - /etc/localtime:/etc/localtime:ro
      - /etc/letsencrypt:/etc/letsencrypt:ro
    environment:
      TZ: Sweden/Stockholm
    labels:
      - 'home-assistant'
    ports:
      - '8123:8123'

  nodered:
    image: kvarak/node-red:0.2
    #image: nodered/node-red:1.0.1-10-minimal-arm32v6
    restart: unless-stopped
    ports:
      - 1880:1880
      - 9229:9229
    volumes:
      - /etc/localtime:/etc/localtime:ro
      - /home/pi/repos/home-assistant/nodered:/data
    labels:
      - "traefik.enable=true"
      - "traefik.backend=nodered"
      - "traefik.frontend.rule=Host:nodered.home.comreset.io"
      - "traefik.port=1880"
```

---

## Resources

- [Installing HA](https://www.home-assistant.io/docs/installation/docker/)
- [HA on docker hub](https://hub.docker.com/r/homeassistant/raspberrypi4-homeassistant/tags)
- [Boot from usb drive](https://www.tomshardware.com/news/boot-raspberry-pi-from-usb,39782.html)
- [Fix locale failed warning on raspbian](https://daker.me/2014/10/how-to-fix-perl-warning-setting-locale-failed-in-raspbian.html)
- [Install docker on raspbian](https://linuxhint.com/install_docker_on_raspbian_os/)
- [docker-compose](https://manre-universe.net/how-to-run-docker-and-docker-compose-on-raspbian/)
- [docker-compose crash](https://stackoverflow.com/questions/59115685/docker-compose-crash-on-a-fresh-raspbian-installation)
- [pip-ffi-h-gcc-error](https://www.poftut.com/pip-ffi-h-gcc-error/)
