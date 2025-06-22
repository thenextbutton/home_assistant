Plex Webhook Handler, carries out actions based on the event taking place within PLEX.


Release:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://github.com/thenextbutton/home_assistant/blob/main/blueprints/plex_webhook_handler/plex_webhook_release.yaml)



<img width="718" alt="plex_webhook_blueprint" src="https://github.com/user-attachments/assets/c44efbb4-f314-4546-a774-2407f8f1689a" />



Prerequisites:

Plex Pass: Enables Plex webhooks.

Understanding of Webhooks (Optional):

Home Assistant: [Webhook Trigger Documentation](https://www.home-assistant.io/docs/automation/trigger/#webhook-trigger)

Plex: [Webhooks Support Article](https://support.plex.tv/articles/115002267687-webhooks/)

Setup:

Generate a Unique Webhook ID:

Use a tool like [GUID Generator](https://guidgenerator.com/) to create a random string.
Configure Plex Webhook:

In Plex, create a webhook pointing to your Home Assistant server:

`http://home_assistant_ip:8123/api/webhook/{webhook_id}`

Example: `http://10.0.1.2:8123/api/webhook/e9ee051d-31cd-464a-b3c4-034992a96be0`

Import the Blueprint.

Create Automation:

Create a new automation using the imported blueprint.

Enter your generated webhook ID and the Plex client name.

Determine Plex Client Name:

If unsure of the client name:
Enable the 'Plex Client Name.UUID ?' option within the blueprint.
Save the automation.
As long as you have setup the webhook on Plex to send to Home Assistant, then...
Play media on Plex.
Look at Home Assistant and you will have a notification within the web page with the client name and the client uuid.

![image](https://github.com/user-attachments/assets/540c68c0-4be0-499b-b5e6-b6120d744fd9)


Enter either the uuid or the client name into the blueprint’s Plex UUID / Client Name field.

UUID is preffered as you could have 2 devices with the same name on the network.
(multiple player are allowed, incase there are more than 2 devices within the one room).

Configure Automation Actions:

Define actions to trigger based on Plex playback events.


Resume Handling (Optional):

The webhook reports a resume event when pausing then playing again, or when you start media that is part way through (continue watching).
The blueprint allows you to treat “resume” as “play” if desired.


Access Webhook Data:

Use payload.Metadata in templates to access data like cover art:

Example(s): 

Thumbnail (cover art)
```yaml
{{ payload.Metadata.thumb }}
```

Here you can create the entire url to retreive the thumbnail:
```yaml
{% set base_url = "http://plex_ip:32400" %}
{% if payload.Metadata.thumb %}
{{ base_url + payload.Metadata.thumb }}
{% endif %}
```

For Artitst and Song Title:
```yaml
{{ payload.Metadata.originalTitle  }} - {{ payload.Metadata.title }}
```

