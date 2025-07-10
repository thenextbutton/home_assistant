# 🏠 Home Assistant Blueprints Collection

This repository houses a growing collection of Home Assistant Blueprints designed to simplify various automation tasks. Each blueprint offers a ready-to-use automation template that you can import directly into your Home Assistant instance, helping you get powerful automations running quickly without extensive YAML coding.

---

## 📖 Table of Contents

* [✨ Available Blueprints](#-available-blueprints)
    * [1. Plex Webhooks](#1-plex-webhooks)
    * [2. Jellyfin Webhooks](#2-jellyfin-webhooks)
    * [3. Frigate Camera Offline](#3-frigate-camera-offline)
* [⚙️ How to Use or Import Blueprints](#-how-to-use-or-import-blueprints)
* [🤝 Contributing](#-contributing)
* [📄 License](#-license)

---

## ✨ Available Blueprints

Below are the blueprints currently available in this collection. Click the "Import Blueprint" button for each to add it directly to your Home Assistant instance.

### 1. Plex Webhooks

Blueprint for Home Assistant to allow automation actions when webhooks are sent from [Plex](https://www.plex.tv/). Great for lowering the lights when a movie starts to play, pausing specific automations during playback, and more.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://github.com/thenextbutton/home_assistant/blob/main/blueprints/plex_webhook_handler/plex_webhook_release.yaml)

### 2. Jellyfin Webhooks

Blueprint for Home Assistant to allow automation actions when webhooks are configured for [Jellyfin](https://jellyfin.org/). Great for lowering the lights when a movie starts to play, updating a media sensor, and other automations based on playback events.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fjellyfin_webhook_handler_v2%2Fjellyfin_webhook_release_v2.yaml)

### 3. Frigate Camera Offline

Blueprint for Home Assistant to notify a device if a camera goes offline within [Frigate](https://frigate.video/).

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fcamera_offline%2Fcamera_offline_release.yaml)

---

## ⚙ How to Use or Import Blueprints

1.  **Click the "Import Blueprint" button** above for the blueprint you wish to use. This will redirect you to your Home Assistant instance.
2.  Confirm the import in Home Assistant.
3.  Navigate to **Settings > Automations & Scenes > Blueprints** within Home Assistant.
4.  Find the newly imported blueprint and click on **"Create Automation"**.
5.  Configure the required fields and options as per the blueprint's requirements.
6.  Save your new automation!

Alternatively, you can manually import a blueprint:
1.  Copy the raw URL of the blueprint YAML file (e.g., `https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME/main/blueprints/blueprint_name.yaml`).
2.  In Home Assistant, go to **Settings > Automations & Scenes > Blueprints**.
3.  Click the "Import Blueprint" button in the bottom right corner.
4.  Paste the raw URL into the URL field and click "PREVIEW BLUEPRINT" then "IMPORT".

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements, or encounter any bugs, feel free to open an issue or submit a pull request.

When contributing a new blueprint, please ensure it includes:
* A clear description.
* Necessary inputs and actions.
* Proper YAML formatting.
* Consider adding a screenshot of the automation configuration if it helps clarify usage.

---

## 📄 License

