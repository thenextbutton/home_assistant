# 🎉 Jellyfin Webhook Handler Blueprint for Home Assistant

Automate your Home Assistant with events from Jellyfin! This blueprint allows you to trigger custom automations in Home Assistant based on various Jellyfin playback events (e.g., play, pause, stop, progress) and other server activities (e.g., item added/deleted, user actions).

---

## 🚀 Release

Click the badge below to easily import the blueprint directly into your Home Assistant instance:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fjellyfin_webhook_handler_v2%2Fjellyfin_webhook_release_v2.yaml)

---

## 📖 Table of Contents

* [Project Overview](#-project-overview)
* [Features](#-features)
* [Prerequisites](#-prerequisites)
* [How It Works](#-how-it-works)
* [Setup](#-setup)
    * [1. Install the Jellyfin Webhook Plugin](#1-install-the-jellyfin-webhook-plugin)
    * [2. Generate a Unique Webhook ID](#2-generate-a-unique-webhook-id)
    * [3. Configure the Webhook within Jellyfin](#3-configure-the-webhook-within-jellyfin)
    * [4. Create a Home Assistant Toggle Helper](#4-create-a-home-assistant-toggle-helper)
    * [5. Import the Blueprint into Home Assistant](#5-import-the-blueprint-into-home-assistant)
    * [6. Create Your Automation](#6-create-your-automation)
        * [Determine Jellyfin Client ID/Name](#determine-jellyfin-client-idname)
    * [7. Configure Automation Actions](#7-configure-automation-actions)
* [Accessing Blueprint Data / Payload Structure](#-accessing-blueprint-data--payload-structure)
* [Example Automation Output / Actions](#-example-automation-output--actions)
* [Troubleshooting & Tips](#-troubleshooting--tips)
* [Contributing](#-contributing)
* [License](#-license)

---

## 💡 Project Overview

This blueprint integrates your Jellyfin server with Home Assistant using webhooks. When significant events occur in Jellyfin (e.g., media playback, library changes, user actions), Jellyfin sends a data packet (a webhook) to your Home Assistant instance. This blueprint then captures that webhook, extracts relevant information, and triggers a Home Assistant event. Your custom automations can then respond to these events, allowing for powerful home automation based on your Jellyfin activity.

---

## ✨ Features

* Trigger automations based on various Jellyfin playback events (play, pause, stop, progress).
* Monitor server activities like item added/deleted and user actions.
* Supports multiple Jellyfin clients/rooms.
* Provides detailed webhook data for advanced automation logic.

---

## 🛒 Prerequisites

To use this blueprint, you'll need:

* **Jellyfin Server:** A running Jellyfin Media Server instance.
* **Jellyfin Webhook Plugin:** Installed on your Jellyfin server.
* **Home Assistant:** A working Home Assistant instance, accessible from your Jellyfin server.

---

## ⚙ How It Works

This blueprint integrates your Jellyfin server with Home Assistant using webhooks. When significant events occur in Jellyfin (e.g., media playback, library changes, user actions), Jellyfin sends a data packet (a webhook) to your Home Assistant instance. This blueprint then captures that webhook, extracts relevant information, and triggers a Home Assistant event. Your custom automations can then respond to these events, allowing for powerful home automation based on your Jellyfin activity.

---

## 🛠 Setup

Follow these steps to configure the Jellyfin Webhook and Home Assistant Blueprint:

### 1. Install the Jellyfin Webhook Plugin

If you haven't already, install the Webhook plugin on your Jellyfin server:

1.  **Import Jellyfin Webhook plugin:** Use the official plugin repository for Jellyfin:
    `https://github.com/jellyfin/jellyfin-plugin-webhook`
2.  Follow the instructions to install the plugin via your Jellyfin Dashboard.

### 2. Generate a Unique Webhook ID

Generate a **unique and random string** to use as your **Webhook ID**. This ID acts as a secret key for your webhook. A [GUID generator](https://guidgenerator.com/) is a reliable tool for this purpose.

### 3. Configure the Webhook within Jellyfin

Now, configure the Webhook plugin in your Jellyfin Dashboard to send events to Home Assistant:

1.  In your Jellyfin Dashboard, navigate to **My Plugins** > **Webhook**.
2.  Click the **+** button to add a new webhook.
3.  Configure the following settings:
    * **Server Url:** `http://{server_url}:{port}` (This refers to your Jellyfin server's base URL and port, typically for local access, though the plugin handles the actual webhook URL separately)
    * **Webhook Name:** `Home Assistant` (or any descriptive name you prefer)
    * **Webhook Url:** `http://{ha_ip}:{ha_port}/api/webhook/{your_webhook_id}`
        * Replace `{ha_ip}` with your Home Assistant's IP address (or hostname).
        * Replace `{ha_port}` with your Home Assistant's port (default is `8123`).
        * Replace `{your_webhook_id}` with the unique ID you generated in step 2.
        * **Example:** `http://10.0.1.19:8123/api/webhook/-KeGmJuhypjHC7HL-fQUNyszy`
4.  Under **Notification Type**, select the events you wish to receive. It is recommended to select all the following:
    * `[x] Authentication Failure`
    * `[x] Authentication Success`
    * `[x] Item Added`
    * `[x] Item Deleted`
    * `[x] Playback Progress`
    * `[x] Playback Start`
    * `[x] Playback Stop`
    * `[x] User Created`
    * `[x] User Deleted`
    * `[x] User Locked Out`
    * `[x] User Password Changed`
    * `[x] User Updated`
5.  Under **Item Type**, select the media types you wish to monitor:
    * `[x] Movies`
    * `[x] Episodes`
    * `[x] Season`
    * `[x] Series`
    * `[x] Albums`
    * `[x] Songs`
    * `[x] Videos`
    * `[x] Trim leading and trailing whitespace from message body before sending` (Recommended)
6.  For the **Template**, you **must** use the provided Handlebars template for this blueprint to function correctly.
    * Copy the contents from: `https://github.com/thenextbutton/home_assistant/blob/main/blueprints/jellyfin_webhook_handler_v2/webhook_template.handlebars`
    * Paste the entire content into the "Template" field within the Jellyfin Webhook plugin settings.
7.  Under **Add Requester Header**, configure the following:
    * **Key:** `Content-Type`
    * **Value:** `application/json`
8.  Ensure **`[x] Enabled`** is checked under **Status**.
9.  Save your Webhook configuration in Jellyfin.

### 4. Create a Home Assistant Toggle Helper

This blueprint requires a boolean (toggle) helper to manage the state of the media playback for each client. You will need a separate helper for each Jellyfin client/room you wish to monitor.

1.  In Home Assistant, go to **Settings** > **Devices & services** > **Helpers**.
2.  Click **+ Create Helper**.
3.  Select **Toggle**.
4.  Give it a memorable name, such as `jellyfin_living_room_toggle` or `jellyfin_bedroom_player`.

### 5. Import the Blueprint into Home Assistant

If you haven't already, import the **Jellyfin Webhook Handler v2** blueprint into your Home Assistant instance using the "Release" badge at the top of this README, or by manually importing the blueprint's YAML file.

### 6. Create Your Automation

1.  In Home Assistant, go to **Settings** > **Automations & Scenes**.
2.  Click the **+ Create Automation** button and choose **Start with an empty automation**.
3.  Select the **Jellyfin Webhook Handler v2** blueprint from the blueprint dropdown.
4.  You will be prompted to enter:
    * Your generated **Webhook ID**.
    * Select the **Toggle Helper** you created in step 4.
    * Enter the **Jellyfin Client ID/Name** for the device you want to monitor.

    ---

    #### Determine Jellyfin Client ID/Name

    If you're unsure of the exact **Jellyfin Client ID** or **Client Name** for your device:

    1.  Leave the "Jellyfin Client ID/Name" field empty for now.
    2.  Enable the **'Jellyfin Client Name/ID?'** option within the blueprint's configuration.
    3.  Save the automation.
    4.  As long as you've set up the webhook correctly in Jellyfin, now **play any media on Jellyfin** using the client you wish to identify.
    5.  Within Home Assistant, you will receive a persistent notification (like the example below) displaying the client's exact name and ID.

    ![image](https://github.com/user-attachments/assets/d8ba6c65-e508-4109-b101-26628f7cd775)

    6.  Copy either the **Client ID** or the **Client Name** and enter it into the blueprint’s **Jellyfin Client ID / Name** field.

    **Note:** The **Client ID is preferred** over the client name, as it provides a unique identifier for your device, preventing potential conflicts if you have multiple devices with the same or similar names on your network. If you enter both an ID and a Name, the ID will take preference.

    ---

### 7. Configure Automation Actions

Finally, define the **actions** you want your Home Assistant automation to perform when the blueprint triggers. The blueprint will expose various Jellyfin events (e.g., `media_play`, `media_pause`, `media_stop`, `media_progress`, `item_added`, `user_login`) that you can use to design your automation logic.

---

## 📊 Accessing Blueprint Data / Payload Structure

Within your Home Assistant automations, you can access detailed information from the Jellyfin webhook payload using Jinja2 templating. The primary data is available under `payload`.

The Handlebars template ensures a consistent `payload` structure that maps to common event types. You can inspect the notification from the "Determine Jellyfin Client ID/Name" step to see the full `payload` structure for a playback event.

**Common `payload` attributes:**

* `payload.EventType`: The type of event (e.g., `PlaybackStart`, `PlaybackStop`, `ItemAdded`).
* `payload.Item.Name`: Name of the media item (e.g., movie title, song title).
* `payload.Item.MediaType`: Type of media (e.g., `Video`, `Audio`).
* `payload.Item.Type`: More specific item type (e.g., `Movie`, `Episode`, `Song`).
* `payload.Item.OfficialRating`: Official rating (e.g., `PG-13`).
* `payload.Item.Overview`: Synopsis/overview of the item.
* `payload.Item.RunTimeTicks`: Total runtime of the item in ticks.
* `payload.PlaybackPositionTicks`: Current playback position in ticks (for `PlaybackProgress` events).
* `payload.Server.Name`: Name of the Jellyfin server.
* `payload.User.Name`: Name of the user performing the action.
* `payload.Client.Name`: Name of the client device (e.g., `Web`, `Android`).
* `payload.Client.Id`: Unique ID of the client device.

**Example(s):**

* **Accessing the media item name:**
    ```yaml
    {{ payload.Item.Name }}
    ```

* **Getting the client name and event type:**
    ```yaml
    Jellyfin {{ payload.Client.Name }} triggered {{ payload.EventType }}
    ```

* **Full URL for Item Image (backdrop or thumbnail):**
    ```yaml
    {% set server_url = "http://YOUR_JELLYFIN_IP:8096" %}
    {% if payload.Item.PrimaryImageTag and payload.Item.Id %}
      {{ server_url }}/Items/{{ payload.Item.Id }}/Images/Primary?tag={{ payload.Item.PrimaryImageTag }}
    {% elif payload.Item.BackdropImageTag and payload.Item.Id %}
      {{ server_url }}/Items/{{ payload.Item.Id }}/Images/Backdrop?tag={{ payload.Item.BackdropImageTag }}
    {% endif %}
    ```
    *Remember to replace `YOUR_JELLYFIN_IP:8096` with your actual Jellyfin server's IP and port.*

---

## 🚧 Troubleshooting & Tips

* **Webhook Not Triggering:**
    * **Check Plugin Installation:** Ensure the Webhook plugin is correctly installed and enabled in Jellyfin.
    * **Verify Webhook URL:** Double-check your Jellyfin webhook URL for any typos, especially the IP address, port (`8123`), and the unique Webhook ID.
    * **Network Access:** Ensure your Home Assistant instance is accessible from your Jellyfin server (e.g., no firewall blocking port `8123` or routing issues).
    * **Jellyfin Logs:** Check your Jellyfin server logs for any errors related to webhooks.
    * **Selected Notification/Item Types:** Ensure the specific "Notification Type" and "Item Type" checkboxes are selected in the Jellyfin webhook configuration for the events you expect to receive.
    * **Handlebars Template:** Verify that the correct `webhook_template.handlebars` content has been pasted entirely and correctly into the Jellyfin webhook template field.
* **Home Assistant Logs:** If you're not seeing the expected behavior, review your Home Assistant logs (Settings > System > Logs) for any errors related to `webhook` or this blueprint.
* **Multiple Clients:** The blueprint supports handling events from multiple Jellyfin clients. You will need to create a separate Home Assistant automation (and a separate toggle helper) for each distinct client/room you wish to monitor.

---

## 🤝 Contributing

Feel free to open an issue or submit a pull request if you have suggestions for improvements or encounter any bugs. Your contributions are welcome!

---

## 📄 License

This project is licensed under the MIT License.
