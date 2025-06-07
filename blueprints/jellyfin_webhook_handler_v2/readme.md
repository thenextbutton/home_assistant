Release: <br>
[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fjellyfin_webhook_handler_v2%2Fjellyfin_webhook_release_v2.yaml)


<br><br>
Configuring Webhook within Jellyfin:

<br>Import Jellyfin Webhook plugin:<br>
https://github.com/jellyfin/jellyfin-plugin-webhook

<br>Dashboard > My Plugins > Webhook...

<br>Server Url: http://{server_url}:{port}

<br>Webhook Name: Home Assistant (or whatever you want to call it)
<br>Webhook Url: http://{ha_ip}:{ha_port}/api/webhook/{your_webhook_id}
<br>example: `http://10.0.1.19:8123/api/webhook/-KeGmJuhypjHC7HL-fQUNyszy`
<br>Use a tool like [GUID Generator](https://guidgenerator.com/) to create a random string for the {your_webhook_id}.<br>
<br>
Select the following within the Webhook setings:<br>

Status:
- [x] Enabled

Notification Type:
- [x] Authentication Failure
- [x] Authentication Success
- [x] Item Added
- [x] Item Deleted
- [x] Playback Progress
- [x] Playback Start
- [x] Playback Stop
- [x] User Created
- [x] User Deleted
- [x] User Locked Out
- [x] User Password Changed
- [x] User Updated

Item Type:
- [x] Movies
- [x] Episodes
- [x] Season
- [x] Series
- [x] Albums
- [x] Songs
- [x] Videos
- [x] Trim leading and trailing whitespace from message body before sending

<br>Template:
<br>[webhook_template.handlebars](https://github.com/thenextbutton/home_assistant/blob/main/blueprints/jellyfin_webhook_handler_v2/webhook_template.handlebars)

<br><br>Add Requester Header:
<br>Key: Content-Type
<br>Value: application/json

Home Assistant

Create a new toggle helper<br>
Settings > Devices & services > Helpers > + Create Helper
<br>
Call it something memorable, you will need more than one if deploying to more than one client/room.
<br>
Settings > Automations & scenes > Blueprints > select Jellyfin Webhook v2
<br>
Enter Webhook ID, Select the Toggle Helper you have just created and enter the Jellyfin Client ID/Name (if not sure then save the automation without it and toggle the 'Jellyfin Client Name/ID', as long as you have setup the webhook information correctly a notification will appear within home assistant with the details. It is probably preferred to use the Client ID but the name option is there if needed, If you enter the ID and a Name the ID will take preference over Name.
<br><br>
![image](https://github.com/user-attachments/assets/3d68feaf-bada-4856-8f9d-97774953005e)

