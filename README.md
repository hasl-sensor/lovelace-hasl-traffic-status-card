[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)
[![ha_version](https://img.shields.io/badge/home%20assistant-0.92%2B-yellow.svg)](https://www.home-assistant.io)
[![version](https://img.shields.io/badge/version-2.3.0-green.svg)](#)
[![maintained](https://img.shields.io/maintenance/yes/2019.svg)](#)

# SL Traffic Status Lovelace Card
Present traffic status from HASL Combination sensors.

![card](https://user-images.githubusercontent.com/1217994/57677754-e1773980-7627-11e9-81e7-4b991a6e4dc1.png)

## Manual Installation
Copy [`hasl-traffic-status-card.js`](https://github.com/hasl-platform/lovelace-hasl-traffic-status-card/blob/master/dist/hasl-traffic-status-card.js) to `<config>/www/hasl-traffic-status-card.js`

Where `<config>` is your Home Assistant configuration directory.
Then use the following in your ui-lovelace.yaml file:

```yaml
resources:
  - url: /local/hasl-traffic-status-card.js
    type: js
```

and use the card through this example:

```yaml
cards:
  - type: custom:hasl-traffic-status-card
        name: Traffic Status
        language: en-EN
        show_time: false
        hide_events: false
        show_only_disturbances: false
        entities:
          - sensor.traffic_status
```

## Configuration variables

- **name** (*Optional*): If specified it will not render titles per entitiy in the card, but rather have this as the card name. If not speficied it will render each sensors name

- **show_cardname**: Render card name, default `true`

- **language** (*Optional*): The texts will be rendered in this language. Can be one of `sv-SE` or `en-EN`

- **show_time** (*Optional*): Render the time beside the name of the card, default `false`

- **hide_events** (*Optional*): Hide all events and renders just the headers, default `false`

- **show_only_disturbances** (*Optional*): Renders just disturbances in the traffic, default `false`
