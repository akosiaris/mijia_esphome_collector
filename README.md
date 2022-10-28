# Intro

A m5stack atom lite esphome configuration that gets information using Bluetooth
Low Energy from 4 different Mi Jia thermometers that run the pvvx firmware,
transforms them into a collectd compatible format and publishes them to an MQTT
broker to be consumed by an already existing collectd instance with the proper
configuration

# Details

Requirements:

* An m5stack atom lite
* 4 Mi Jia LYWSD03MMC Mi Jia thermometers/hygrometers running pvvx firmware
* An esphome installation

## How to

Create a file secrets.yaml containing something like the following:

```
ota_password: "foobar"
api_password: "foobar"
wifi_ssid: "foobar"
wifi_password: "foobar123"
fallback_ssid: "Window Fallback Hotspot"
fallback_password: "foobar321"

area_1_name: myhouse
area_1_upper_name: My house
area_1_mac_address: "AB:CD:EF:01:23:45"
...
```

Amend to your will, and make sure you define 4 areas.
