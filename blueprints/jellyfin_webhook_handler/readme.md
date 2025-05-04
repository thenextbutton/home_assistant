
Release:<br>

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fjellyfin_webhook_handler%2Fjellyfin_webhook_release.yaml)
<br><br>

Ensure you have the [Jellyfin Webook plugin installed](https://github.com/jellyfin/jellyfin-plugin-webhook)<br><br>

Setting up webhooks from Jellyfin:<br><br>

Menu/Settings > Administration > Dashboard > Plugins > My Plugins > Webhook<br><br>
Add a Generic Destination.<br>
Give the webhook a Name (i.e. Home Assistant)<br>
Enter the webhook url (treat this as a password, try not to share it)<br>
Use a tool like [GUID Generator](https://guidgenerator.com/) to create a random string for the <webhook_id>.<br>
(example)<br>
`http://<home_assistant_ip>:8123/api/webhook/<webhook_id>`<br>
`http://10.0.1.2:8123/api/webhook/4ed1c518-9131-4c59-8f4e-08ccdc8d7f7d`<br>

Check Status: Enable<br><br>

The following should then be checked:<br>
Notification:<br>
Playback Start<br>
Playback Stop<br><br>

Item Type:<br>
Movies<br>
Episodes<br>
Songs<br>

Within the Template, paste the contents of [webhook_template.handlebars](https://github.com/thenextbutton/home_assistant/blob/main/blueprints/jellyfin_webhook_handler/webhook_template.handlebars)<br><br>

Add A Request Header and place the following in:<br>
Key: Content-Type<br>
Value: application/json<br>

Click on Save.<br>

Within Home Assistant, create a new automation from the blueprint, enter the <webhook_id> in to the Webhook ID field in the automation.

You will also need to enter the device name (playback client) in the Jellyfin Device Name field, if you are not sure what that is enable the 'Jellyfin Device Name ?' and click save. Start a movie, music or tv episode and a notification within home assistant will let you know the device name.

![image](https://github.com/user-attachments/assets/eb5d6801-4b55-418d-b760-ab9fc7f9fe5f)
