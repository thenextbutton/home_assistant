# 🎉 Plex Webhook Handler Blueprint for Home Assistant

Automate your Home Assistant with events from Plex! This blueprint allows you to trigger custom automations in Home Assistant based on various Plex playback events (e.g., play, pause, resume, stop) from specific Plex clients.

---

## 🚀 Release

Click the badge below to easily import the blueprint directly into your Home Assistant instance:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://github.com/thenextbutton/home_assistant/blob/main/blueprints/plex_webhook_handler/plex_webhook_release.yaml)

---

## 📖 Table of Contents

* [Project Overview](#-project-overview)
* [Features](#-features)
* [Prerequisites](#-prerequisites)
* [How It Works](#-how-it-works)
* [Setup](#-setup)
    * [1. Generate a Unique Webhook ID](#1-generate-a-unique-webhook-id)
    * [2. Configure Plex Webhook](#2-configure-plex-webhook)
    * [3. Import the Blueprint](#3-import-the-blueprint)
    * [4. Create Your Automation](#4-create-your-automation)
        * [Determine Plex Client Name/UUID](#determine-plex-client-nameuuid)
    * [5. Configure Automation Actions](#5-configure-automation-actions)
* [Accessing Blueprint Data / Payload Structure](#-accessing-blueprint-data--payload-structure)
* [Example Automation Output / Actions](#-example-automation-output--actions)
* [Advanced: Real-Time Session & Metadata Integration](#-advanced-real-time-session--metadata-integration)
* [Troubleshooting & Tips](#-troubleshooting--tips)
* [Contributing](#-contributing)
* [License](#-license)

---

## 💡 Project Overview

This blueprint leverages Plex's webhook functionality. When an event occurs in Plex (like playing, pausing, or stopping media), Plex sends a webhook to your Home Assistant instance. This blueprint then captures that webhook, extracts relevant information (like the client name or UUID), and triggers a Home Assistant automation that you create.

---

## ✨ Features

* **Event Triggering:** Play, pause, resume, and stop events.
* **Client Filtering:** Target specific Plex clients via Name or UUID.
* **Smart Scheduling (New v0.5.2):** * **GUI Schedule Support:** Use Home Assistant Schedule Helpers for visual timing.
    * **Sun Elevation:** Only run when the sun is down.
    * **Manual Fallback:** Precise start/end times with cross-midnight support.
* **Deep Metadata:** Access rating keys, thumbnails, and technical data.

---

## 🛒 Prerequisites

To use this blueprint, you'll need:

* **Plex Pass:** A Plex Pass is required to enable webhook functionality within Plex Media Server.
* **Home Assistant:** A working Home Assistant instance, accessible from your Plex Media Server.
* **Sun Integration:** Must be enabled to use sunset/sunrise filters.

---

## ⚙ How It Works

This blueprint leverages Plex's webhook functionality. When an event occurs in Plex (like playing, pausing, or stopping media), Plex sends a webhook to your Home Assistant instance. This blueprint then captures that webhook, extracts relevant information (like the client name or UUID), and triggers a Home Assistant automation that you create.

### Time Logic Priority 
To prevent conflicting settings, the blueprint follows a strict hierarchy. Once a higher-priority condition is met, the others are ignored:

1. **Sunset Mode (Highest Priority):** If "Use Sunset/Sunrise" is ON, actions only run when the sun is below the horizon. Manual times and Schedules are ignored.
2. **Schedule Helper (Secondary):** If a Schedule Helper is selected, the automation follows that grid. This overrides Manual Times.
3. **Manual Fallback:** If neither Sunset nor a Schedule is used, the automation reverts to the Manual Start and End time boxes.

---

## 🛠 Setup

Follow these steps to get your Plex Webhook Handler blueprint up and running:

### 1. Generate a Unique Webhook ID

First, generate a **unique and random string** to use as your **Webhook ID**. This ID acts as a secret key to ensure your webhook is secure. A [GUID generator](https://guidgenerator.com/) is a reliable tool for this purpose.

### 2. Configure Plex Webhook

Next, you need to tell Plex where to send its webhook events.

1.  Open your **Plex Media Server settings**.
2.  Navigate to **Settings** > **Webhooks**.
3.  Click **Add Webhook**.
4.  Enter your Home Assistant webhook URL in the following format, replacing `home_assistant_ip` with your Home Assistant's IP address (or hostname) and `{webhook_id}` with the unique ID you generated:

    `http://home_assistant_ip:8123/api/webhook/{webhook_id}`

    **Example:** `http://10.0.1.2:8123/api/webhook/e9ee051d-31cd-464a-b3c4-034992a96be0`

### 3. Import the Blueprint

If you haven't already, import the **Plex Webhook Handler** blueprint into your Home Assistant instance using the "Release" badge above, or by manually importing the blueprint's YAML file.

### 4. Create Your Automation

1.  In Home Assistant, go to **Settings** > **Automations & Scenes**.
2.  Click the **+ Create Automation** button and choose **Start with an empty automation**.
3.  Select the **Plex Webhook Handler** blueprint from the list.
4.  You will be prompted to enter:
    * Your generated **Webhook ID**.
    * The **Plex Client Name** (or UUID) for the device you want to monitor.

    ---

    #### Determine Plex Client Name/UUID

    If you're unsure of the exact **Plex Client Name** or **UUID** for your device:

    1.  Enable the **'Plex Client Name/UUID ?'** option within the blueprint's configuration.
    2.  Save the automation.
    3.  As long as you've set up the webhook correctly in Plex, now **play any media on Plex** using the client you wish to identify.
    4.  Within Home Assistant, you will receive a persistent notification (like the example below) displaying the client's exact name and UUID.

    ![image](https://github.com/user-attachments/assets/540c68c0-4be0-499b-b5e6-b6120d744fd9)

    5.  Copy either the **UUID** or the **Client Name** and enter it into the blueprint’s **Plex UUID / Client Name** field.

    **Note:** The **UUID is preferred** over the client name, as it provides a unique identifier for your device, preventing potential conflicts if you have multiple devices with the same or similar names on your network. Multiple players are supported, it is advised to create an automation from the blueprint for each room.

    ---

### 5. Configure Automation Actions

Finally, define the **actions** you want your Home Assistant automation to perform when the blueprint triggers. The blueprint will expose various Plex playback events (e.g., `media_play`, `media_pause`, `media_stop`, `media_resume`) that you can use to design your automation logic.

---

## 📊 Accessing Blueprint Data / Payload Structure

Within your Home Assistant automations, you can access detailed information from the Plex webhook payload using Jinja2 templating. The primary data is available under `payload.Metadata`.

**Example(s):**

* **Thumbnail (cover art):**
    ```yaml
    {{ payload.Metadata.thumb }}
    ```

* **Full URL to retrieve thumbnail:**
    ```yaml
    {% set base_url = "http://plex_ip:32400" %}
    {% if payload.Metadata.thumb %}
    {{ base_url + payload.Metadata.thumb }}
    {% endif %}
    ```

* **Artist and Song Title:**
    ```yaml
    {{ payload.Metadata.originalTitle }} - {{ payload.Metadata.title }}
    ```

For a comprehensive list of available `payload.Metadata` attributes, refer to the [Plex Webhooks Support Article](https://support.plex.tv/articles/115002267687-webhooks/) linked in the Prerequisites section.

---

## 🖼 Example Automation Output / Actions

Plex's `resume` webhook event is triggered both when you resume previously paused media and when you start media from a "continue watching" point. This blueprint provides an option to treat the `resume` event identically to a `play` event, if desired, simplifying your automation logic.

Here's an example of how you might define an action within your Home Assistant automation to create a persistent notification upon a Plex event (e.g., after a Plex database backup completes, if your blueprint is configured to trigger on that):

```yaml
action: persistent_notification.create
metadata: {}
data:
  message: Plex Database Backup completed.
  notification_id: plex_db_backup
  title: Plex Alert
```

---

## ⚡ Advanced: Real-Time Session & Metadata Integration

While standard webhooks tell you a movie has started, they don't tell you if it's being **transcoded** or what the **real-time aspect ratio** is. By querying the Plex `/status/sessions` endpoint, we can extract live data specific to the player that triggered the webhook.

### 1. Configure the REST Command
Add this to your `configuration.yaml`. This command fetches all active sessions on your server. Replace `<plex_server_ip>` and `<plex_token_id>` with your specific details.

```yaml
rest_command:
  plex_get_session_details:
    url: "http://<plex_server_ip>:32400/status/sessions?X-Plex-Token=<plex_token_id>"
    method: GET
    headers:
      Accept: "application/json"
```

### 2. Implementation in Automation Actions
Because this data is live, we call the API and then use a series of variables to "chain" the data processing. This ensures we find the session matching the specific client (UUID) that triggered the webhook.

**The Action & Variables:**
```yaml
sequence:
  - action: rest_command.plex_get_session_details
    metadata: {}
    data: {}
    response_variable: plex_api_response
  - variables:
      all_sessions: "{{ plex_api_response.content.MediaContainer.Metadata | default([]) }}"
      active_session: >
        {{ all_sessions | selectattr('Player.machineIdentifier', 'eq',
        payload.Player.uuid) | first | default({}) }}
      media_block: "{{ active_session.get('Media', [{}])[0] }}"
      transcode_block: "{{ active_session.get('TranscodeSession', {}) }}"
      realtime_aspect_ratio: "{{ media_block.get('aspectRatio', 'unknown') }}"
      audio_decision: "{{ media_block.get('Part', [{}])[0].get('decision', 'unknown') }}"
      realtime_audio_channels: >
        {% if transcode_block %}{{ transcode_block.get('audioChannels', 2) }}{%
        else %}{{ media_block.get('audioChannels', 2) }}{% endif %}
      realtime_audio_codec: >
        {% if transcode_block %}{{ transcode_block.get('audioCodec', 'aac') }}{%
        else %}{{ media_block.get('audioCodec', 'unknown') }}{% endif %}
      primary_genre: "{{ active_session.get('Genre', [{}])[0].get('tag', 'None') }}"
      collections: "{{ active_session.get('Collection', []) | map(attribute='tag') | list }}"
      content_rating: "{{ active_session.get('contentRating', 'NR') }}"
```

### 3. Use Case: Real-Time AV Sync
With these variables, you can automate your home theater hardware based on the stream properties.

**Example: Automated Screen Masking & Audio Mode**
```yaml
choose:
  # If the movie is in CinemaScope (2.35/2.39), adjust the screen masks
  - conditions:
      - condition: template
        value_template: "{{ realtime_aspect_ratio in ['2.35', '2.39'] }}"
    sequence:
      - action: cover.set_cover_position
        target:
          entity_id: cover.screen_masks
        data:
          position: 0

  # If Plex is transcoding to Stereo, set the receiver to 'All Channel Stereo'
  - conditions:
      - condition: template
        value_template: "{{ realtime_audio_channels == 2 }}"
    sequence:
      - action: media_player.select_source
        target:
          entity_id: media_player.receiver
        data:
          source: "All Channel Stereo"

  # If it's a Horror movie, set the lights to a dim Deep Red
  - conditions:
      - condition: template
        value_template: "{{ primary_genre == 'Horror' }}"
    sequence:
      - action: light.turn_on
        target:
          entity_id: light.theater_leds
        data:
          color_name: "darkred"
          brightness_pct: 5
```

---

## 🚧 Troubleshooting & Tips

* **Webhook Not Triggering:**
    * **Check Plex Pass:** Ensure you have an active Plex Pass, as it's required for webhooks.

    * **Verify Webhook URL:** Double-check your Plex webhook URL for any typos, especially the IP address, port (8123), and the unique Webhook ID.

    * **Network Access:** Ensure your Home Assistant instance is accessible from your Plex Media Server (e.g., no firewall blocking port 8123 or routing issues).

    * **Plex Logs:** Check your Plex Media Server logs for any errors related to webhooks.
	
* **Home Assistant Logs:** If you're not seeing the expected behavior, review your Home Assistant logs (Settings > System > Logs) for any errors related to webhook or this blueprint.

* **Multiple Clients:** While multiple players are supported, it is advised to create an automation from the blueprint for each room.

* **Client Name/UUID Mismatch:** Ensure the client name/UUID in your blueprint automation exactly matches what Plex reports (use the 'Determine Plex Client Name/UUID?' option if unsure).

* **"Unknown entity selected":** If you aren't using a Schedule Helper, the UI shows a warning. This is expected behavior; the automation will simply fall back to your Manual Times.
  
* **REST Command Failures:** Check your Home Assistant Logs. Ensure your Plex Token is correct and that HA can reach the Plex IP on port 32400.
  
* **Trace Insights:** To see what other data is available, run a media file, open the **Automation Trace**, and look at the `plex_api_response` variable.

---

## 🤝 Contributing

Feel free to open an issue or submit a pull request if you have suggestions for improvements or encounter any bugs. Your contributions are welcome!

---

## 📄 License

This project is licensed under the MIT License.
