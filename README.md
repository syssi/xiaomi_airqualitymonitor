# Xiaomi Mi Air Quality Monitor (PM2.5)

This is a custom component for home assistant to integrate the Xiaomi Mi Air Quality Monitor (PM2.5).

Please follow the instructions on [Retrieving the Access Token](https://home-assistant.io/components/xiaomi/#retrieving-the-access-token) to get the API token to use in the configuration.yaml file.

Credits: Thanks to [Rytilahti](https://github.com/rytilahti/python-miio) for all the work.

## Features

### Air Quality Monitor

* On, Off
* Air Quality Index
* Attributes
  - power
  - charging
  - battery
  - time_state

## Setup

```yaml
# confugration.yaml

sensor:
  - platform: xiaomi_miio
    name: Xiaomi Air Quality Monitor
    host: 192.168.130.73
    token: 56197337f51f287d69a8a16cf0677379
```

Configuration variables:
- **host** (*Required*): The IP of your light.
- **token** (*Required*): The API token of your light.
- **name** (*Optional*): The name of your light.


## Platform services

#### Service sensor.turn_on

Turn the air quality monitor on.

| Service data attribute    | Optional | Description                                                   |
|---------------------------|----------|---------------------------------------------------------------|
| `entity_id`               |      yes | Only act on a specific xiaomi miio entity. Else targets all.  |

#### Service sensor.turn_off

Turn the air quality monitor off.

| Service data attribute    | Optional | Description                                                   |
|---------------------------|----------|---------------------------------------------------------------|
| `entity_id`               |      yes | Only act on a specific xiaomi miio entity. Else targets all.  |
