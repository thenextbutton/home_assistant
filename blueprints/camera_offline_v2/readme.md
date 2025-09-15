# 🎉 Camera Offline (v2) Blueprint for Home Assistant

Receive instant mobile notifications when your cameras go offline or come back online. This blueprint prevents notification spam from brief, repeated outages by using a notification flag that only resets after a full camera recovery.

---

## 🚀 Release

Click the badge below to easily import the blueprint directly into your Home Assistant instance:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fcamera_offline_v2%2Fcamera_offline_v2_release.yaml)

---

## 📖 Table of Contents

* [Project Overview](#-project-overview)
* [Features](#-features)
* [Prerequisites](#-prerequisites)
* [How It Works](#-how-it-works)
* [Setup](#-setup)<br>
    * [1. Import the Blueprint](#1-import-the-blueprint)<br>
    * [2. Configure the Var Integration](#2-configure-the-var-integration)<br>
    * [3. Create Your Automation](#3-create-your-automation)<br>
* [Example Automation Output / Actions](#-example-automation-output--actions)
* [Troubleshooting & Tips](#-troubleshooting--tips)
* [Contributing](#-contributing)
* [License](#-license)

---

## 💡 Project Overview

This blueprint monitors the state of your cameras and sends a notification when they go offline. It intelligently tracks the state of each camera to avoid sending multiple alerts for a single, prolonged outage. Notifications are also sent when the camera comes back online after a full recovery.

---

## ✨ Features

* **Universal Camera Support**: Works with any camera entity that reports its status (e.g., `unavailable`, `recording`, etc.).
* **Anti-Spam Logic**: Prevents multiple notifications for the same ongoing outage.
* **Recovery Notifications**: Get a notification when a camera comes back online, including its total offline duration.
* **Customizable Timers**: User-defined stability durations for both offline and recovery states to filter out brief disconnections.
* **Critical Notifications**: Optional high-priority notifications that bypass "Do Not Disturb" settings.
* **Flexible Notification Options**: Send alerts to mobile devices, persistent notifications for debugging, or both.

---

## 🛒 Prerequisites

To use this blueprint, you'll need:

* **Home Assistant:** A working Home Assistant instance.
* **Mobile App Integration:** The **Home Assistant Companion App** installed on your mobile device(s) and configured to receive notifications.
* **Var Integration:** The **[Home Assistant Variables](https://github.com/snarky-snark/home-assistant-variables)** integration installed via **[HACS](https://www.hacs.xyz/)**. This is crucial as the blueprint uses a `var` entity to track camera states and notification flags.

A huge thank you to **snarky-snark** for developing the Home Assistant Variables integration, which makes this blueprint's advanced features possible!

---

## ⚙ How It Works

The blueprint uses the `var` integration to create a persistent **Camera Status Tracker** entity. This entity stores the state and notification flag for each monitored camera.

1.  When a camera's state changes to `unavailable` for the specified `offline_stability_duration`, the blueprint checks the tracker. If the camera hasn't been notified as offline yet, an alert is sent, and a flag is set.
2.  If the camera state repeatedly flips between `unavailable` and `recording`, no new offline notification will be sent because the flag is already set.
3.  The offline flag is **only reset** when the camera's state becomes `recording` for the specified `recovery_stability_duration`, at which point a recovery notification is sent.

This intelligent state tracking ensures you only receive one notification per full outage cycle (offline to fully recovered).

---

## 🛠 Setup

Follow these steps to configure the blueprint:

### **1. Import the Blueprint**

If you haven't already, import the **Camera Offline v2** blueprint into your Home Assistant instance using the "Release" badge above, or by manually importing the blueprint's YAML file.

### **2. Configure the Var Integration**

First, you need to configure the `var` integration in your Home Assistant's **`configuration.yaml`** file. This will create a `var` entity that the blueprint uses to store camera status information and prevent notification spam.

You can customise the **`camera_status_tracker`** (the variable entity ID) and the **`friendly_name`** to anything you like. However, it is essential to leave the other settings as they are.

```yaml
var:
  camera_status_tracker:
    friendly_name: "Camera Status Tracker"
    initial_value: "tracking"
    attributes:
      camera_states: "{}"
    restore: true
```

### **3. Create Your Automation**

1.  In Home Assistant, go to **Settings** > **Automations & Scenes**.
2.  Click the **+ Create Automation** button and choose **Start with an empty automation**.
3.  Select the **Camera Offline (v2)** blueprint from the blueprint dropdown.
4.  You will be prompted to configure the following options:
    * **Camera(s) to Monitor:** Select the camera entities you wish to monitor.
    * **Notify Target:** Choose the mobile devices that will receive the notifications.
    * **Camera Status Tracker (var entity):** Select the `var` entity you created to store the camera status.
    * **Offline Notification Details:** Customise the alert for when a camera goes offline.
        * **Enable Offline Notifications?**: Toggle this on or off.
        * **Offline Stability Duration**: Set how long a camera must be unavailable before an alert is sent.
        * **Critical Offline Notification?**: Make the alert high-priority.
        * **Offline Message Title**: Customise the message title (use `{friendly_name}`).
        * **Offline Message Template**: Customise the message (use `{friendly_name}`).
    * **Online Notification Details:** Customise the alert for when a camera recovers.
        * **Enable Recovery Notifications?**: Toggle this on or off.
        * **Recovery Stability Duration**: Set how long a camera must be `recording` before a recovery alert is sent and the notification flag is reset.
        * **Critical Recovery Notification?**: Make the alert high-priority.
        * **Recovery Message Title**: Customise the message title (use `{friendly_name}` and `{offline_duration}`).
        * **Recovery Message Template**: Customise the message (use `{friendly_name}` and `{offline_duration}`).
    * **Notification Mode**: Choose to send alerts to devices, persistent notifications (for debugging), or both.

---

### **🖼 Example Automation Output / Actions**

Upon a camera going offline for the specified duration, a notification similar to this will be sent to your chosen device(s):<br>
<img width="300" alt="image" src="https://github.com/user-attachments/assets/ccb4b7ee-c9a0-4a2c-b389-279045e90424" />



When a camera comes back online after a prolonged outage, a notification similar to this will be sent:<br>
<img width="300" alt="image" src="https://github.com/user-attachments/assets/c497c89a-fa89-4db1-87ca-7ec4890cd2ce" />


---

### **🚧 Troubleshooting & Tips**

* **No Notifications:**
    * Ensure the **`var` integration** is installed and that you have a `var` entity selected in the blueprint configuration.
    * Verify your mobile device is correctly configured with the Home Assistant Companion App and is receiving notifications.
    * Check your Home Assistant logs (Settings > System > Logs) for any errors.
* **False Alarms:** Adjust the `Offline Stability Duration` to a higher value if you are receiving notifications for brief camera disconnections or network hiccups.
* **No Recovery Notifications:** This blueprint specifically looks for the `recording` state to signal recovery. If your camera integration uses a different state, the recovery trigger may not fire. Check your camera entity's state in **Developer Tools** to confirm.
* **The Blueprint seems to not send notifications a second time:** This is an intentional anti-spam feature. The blueprint will not send another offline notification for the same camera until it has gone through a full recovery cycle and the recovery stability duration has been met.

---

### **🤝 Contributing**

Feel free to open an issue or submit a pull request if you have suggestions for improvements or encounter any bugs. Your contributions are welcome!

---

### **📄 License**

This project is licensed under the MIT License.
