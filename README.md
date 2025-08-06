# 🏠 Home Assistant Blueprints Collection

[![Community Blueprints](https://img.shields.io/badge/Community-Blueprints-blue?logo=home-assistant&logoColor=white)](https://community.home-assistant.io/)
[![Home Assistant 2024.6.0+](https://img.shields.io/badge/Home%20Assistant-2024.6.0+-orange?logo=home-assistant&logoColor=white)](https://www.home-assistant.io/)
[![Language: YAML](https://img.shields.io/badge/Language-YAML-cb171e?logo=yaml&logoColor=white)](https://yaml.org/)
![Plex Webhooks](https://img.shields.io/static/v1?label=%20&message=Webhooks&labelColor=E5A001&color=blue&logo=plex&logoColor=white)
[![Jellyfin Webhooks](https://img.shields.io/badge/Jellyfin-Webhooks-blue?logo=jellyfin&logoColor=white)](https://jellyfin.org/)
[![Frigate Monitor](https://img.shields.io/badge/Frigate-Monitor-blue?logo=frigate&logoColor=white)](https://frigate.video/)
[![GitHub last commit](https://img.shields.io/github/last-commit/thenextbutton/home_assistant)](https://github.com/thenextbutton/home_assistant/commits/main)
[![GitHub Issues](https://img.shields.io/github/issues/thenextbutton/home_assistant)](https://github.com/thenextbutton/home_assistant/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/thenextbutton/home_assistant)](https://github.com/thenextbutton/home_assistant/pulls)
[![GitHub Stars](https://img.shields.io/github/stars/thenextbutton/home_assistant?style=social)](https://github.com/thenextbutton/home_assistant/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/thenextbutton/home_assistant/blob/main/LICENSE)

---

This repository houses a growing collection of Home Assistant Blueprints designed to simplify various automation tasks. 

---

# 🏠 Home Assistant Blueprints Collection

This repository houses a growing collection of Home Assistant Blueprints designed to simplify various automation tasks. Each blueprint offers a ready-to-use automation template that you can import directly into your Home Assistant instance, helping you get powerful automations running quickly without extensive YAML coding.

---

* [Plex Webhooks](#plex-webhooks)
* [Jellyfin Webhooks](#jellyfin-webhooks)
* [Frigate Camera Offline](#frigate-camera-offline)

---

### [Plex Webhooks](https://github.com/thenextbutton/home_assistant/tree/main/blueprints/plex_webhook_handler)

Blueprint for Home Assistant to allow automation actions when webhooks are sent from [Plex](https://www.plex.tv/). Great for lowering the lights when a movie starts to play, pausing specific automations during playback, and more.


### [Jellyfin Webhooks](https://github.com/thenextbutton/home_assistant/tree/main/blueprints/jellyfin_webhook_handler_v2)

Blueprint for Home Assistant to allow automation actions when webhooks are configured for [Jellyfin](https://jellyfin.org/). Great for lowering the lights when a movie starts to play, updating a media sensor, and other automations based on playback events.


**Important Note:** Don't forget that the webhook template is also needed to be set up within Jellyfin using this template handlebar code: [webhook_template.handlebars](https://raw.githubusercontent.com/thenextbutton/home_assistant/main/blueprints/jellyfin_webhook_handler_v2/webhook_template.handlebars)


### [Frigate Camera Offline](https://github.com/thenextbutton/home_assistant/tree/main/blueprints/camera_offline)

Blueprint for Home Assistant to notify a device if a camera goes offline within [Frigate](https://frigate.video/).
