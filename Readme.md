# Disco Light

A light using five WS2812B LED strips with 76 lights and an ESP8266 based
NodeMCU V2 and built with [ESPHome](https://esphome.io/).

| Light Strip | Pin | GPIO |
| ----------- | --- | ---- |
| 0           | D3  | 00   |
| 1           | D2  | 04   |
| 2           | D1  | 05   |
| 3           | D0  | 16   |
| 4           | D5  | 14   |

## Install ESPHome

See [Getting Started with ESPHome](https://esphome.io/guides/getting_started_command_line.html)

```sh
pip3 install esphome
```

## Compiling and Installing

First, you must create a file `secrets.yaml` with your WiFi network and password
plus a password for your fallback hotspot password. This file should not be
checked into source control.

```yaml
wifi_ssid: "WiFi SSID"
wifi_pw: "WiFi password"
hotspot_pw: "Fallback hotspot password"
```

You can then compile and install from the command line. If you have already
programmed the device, it can be installed over the air (OTA). First time install
must be over USB.

Run the command

```sh
esphome run discolight.yaml
```
