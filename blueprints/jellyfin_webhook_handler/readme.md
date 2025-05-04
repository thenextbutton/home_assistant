<p align="center">
<img src="https://github.com/user-attachments/assets/2f3a76d5-cda6-49b0-982c-97f4af36d2f4"  height="250" width="250" >
</p>

Ensure you have the [Jellyfin Webook plugin install](https://github.com/jellyfin/jellyfin-plugin-webhook)<br><br>


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
