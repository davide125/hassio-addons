# Homebridge addon for Home Assistant

This is an [Homebridge](https://homebridge.io) add-on for [Home Assistant](https://www.home-assistant.io). Homebridge provides a lightweight HomeKit API implementation with plugin support.

Note that Home Assistant supports HomeKit natively these days, both as a [controller](https://www.home-assistant.io/integrations/homekit_controller/) and as a [device](https://www.home-assistant.io/integrations/homekit/), so you probably don't need Homebridge if you just want to integrate with the HomeKit ecosystem. However, Homebrige has a lot of plugins, so it can still be useful to bridge some less-supported devices (e.g. [Nest](https://github.com/chrisjshull/homebridge-nest)) into Home Assistant.

## Installation
Add the [add-on repository](https://github.com/davide125/hassio-addons) and install Homebridge from the add-on store. This may take a while: no prebuilt image is currently being provided so Home Assistant will build one for you at installation time. 

To configure Homebridge, forward the Homebridge UI port to the host in the add-on configuration to access it. The default credentials are the same as regular Homebridge (i.e. admin/admin); please change them on the first login.

## Credits
This add-on was inspired by [adsb-multi-portal-feeder](https://github.com/MaxWinterstein/homeassistant-addons/tree/main/adsb-multi-portal-feeder) to leverage a pre-existing Docker image and integrate it into an add-on ([Docker Homebridge](https://github.com/oznu/docker-homebridge) in this case). The add-on icon is derived from [Material Design Icons](https://materialdesignicons.com/icon/home-automation). These projects (and Homebridge itself) deserve all the credit here. This add-on is unrelated to the deprecated [addon-homebridge](https://github.com/hassio-addons/addon-homebridge).
