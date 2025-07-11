# Frigate Camera Offline Detector Blueprint for Home Assistant

Receive instant notifications when your Frigate NVR cameras go offline. This blueprint detects disconnected cameras and, after a user-defined delay, alerts your specified Home Assistant devices, ensuring you're always aware of your security system's status.

---

## Release

Click the badge below to easily import the blueprint directly into your Home Assistant instance:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fcamera_offline%2Fcamera_offline_release.yaml)

---

## Prerequisites

To use this blueprint, you'll need:

* **Frigate NVR:** A running Frigate NVR instance with configured cameras.
* **Frigate Integration:** The official Frigate integration installed and configured in Home Assistant.
* **Home Assistant:** A working Home Assistant instance.

---

## How It Works

This blueprint monitors the state of your Frigate cameras via their `camera` entities in Home Assistant. When a camera's state changes from `on` to `off`, a timer is started. If the camera remains `off` for the user-defined duration, the blueprint triggers an automation to send a notification to your chosen devices, alerting you to the offline camera.

---

## Setup

Follow these steps to configure the blueprint:

### 1. Import the Blueprint

If you haven't already, import the **Frigate Camera Offline Detector** blueprint into your Home Assistant instance using the "Release" badge above, or by manually importing the blueprint's YAML file.

### 2. Create Your Automation

1.  In Home Assistant, go to **Settings** > **Automations & Scenes**.
2.  Click the **+ Create Automation** button and choose **Start with an empty automation**.
3.  Select the **Frigate Camera Offline Detector** blueprint from the blueprint dropdown.
4.  You will be prompted to configure the following options:
    * **Camera(s) to Monitor:** Select one or more camera entities you want to monitor for offline status (e.g., `camera.front_door`, `camera.backdoor`). These should be entities that report `unavailable` when offline.

    * **Notification Settings:**
        * **Device(s) to Notify:** Select the mobile device(s) (running the Home Assistant app) to receive offline notifications.
        * **Offline Duration:** Set the duration a camera must be offline (unavailable) before a notification is sent. This helps prevent false alerts from brief network glitches.
        * **Cooldown Duration:** Set a cooldown period. Once a camera offline notification is sent, **no further notifications (for any camera)** will be sent until this period expires. Set to `0` to disable this cooldown.
        * **Notification Title:** Enter the desired title for the push notification (default: "🚨 Camera Offline Alert 🚨").
        * **Notification Message:** Customize the message that will appear in the push notification. The default message includes the camera's friendly name, entity ID, and how long it has been offline.
        * **Critical Notification:** Enable this option to send a critical alert that bypasses silent mode settings on the device (if supported by your device and the Home Assistant Companion app).

![example notification](https://github.com/user-attachments/assets/d7dfd6de-249c-4c70-aecd-d6b78f8f476a)

---

## Example Automation Output

Upon a camera going offline for the specified duration, a notification similar to this will be sent to your chosen device(s):

![image](https://github.com/user-attachments/assets/c3a06098-d09f-4afa-ba4f-cf8afb943e2b)

---

## Troubleshooting & Tips

* **Camera State Not Updating:** Ensure your Frigate NVR is running and the Frigate integration in Home Assistant is connected and functioning correctly. Check the `camera` entity's state in Home Assistant Developer Tools.
* **No Notifications:**
    * Verify that the "Notification Device" is correctly selected in the blueprint configuration.
    * Check your Home Assistant Companion app settings on your notification device to ensure notifications are enabled.
    * Temporarily set the "Offline Duration" to a very low value (e.g., 1 minute) for testing purposes.
    * Check if the "Cooldown Duration" is preventing notifications.
* **False Alarms:** Adjust the "Offline Duration" to a higher value if you are receiving notifications for brief camera disconnections or network hiccups.
* **Home Assistant Logs:** If issues persist, check your Home Assistant logs (Settings > System > Logs) for any errors related to the camera entity or the blueprint automation.
