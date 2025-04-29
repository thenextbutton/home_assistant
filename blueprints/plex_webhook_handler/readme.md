Plex Webhook Handler, carries out actions based on the event taking place within PLEX.


Release:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fthenextbutton%2Fhome_assistant%2Fblob%2Fmain%2Fblueprints%2Fplex_webhook_handler%2Fplex_webhook_release.yaml)



<img width="718" alt="plex_webhook_blueprint" src="https://github.com/user-attachments/assets/5ae5e4e8-9484-41f1-b6ac-7af7596211be" />



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

Example URL: http://<home_assistant_ip>:<port>/api/webhook/{webhook_id}

Example: http://10.0.1.2:8123/api/webhook/e9ee051d-31cd-464a-b3c4-034992a96be0

Import the Blueprint.

Create Automation:

Create a new automation using the imported blueprint.

Enter your generated webhook ID and the Plex client name.

Determine Plex Client Name:

If unsure of the client name:
Enable the 'Plex Client Name?' option within the blueprint.
Save the automation.
As long as you have setup the webhook on Plex to send to Home Assistant, then...
Play media on Plex.
Look at Home Assistant and you will have a notification within the web page with the client name.
Enter this value into the blueprint’s Plex client field (case-insensitive).


Configure Automation Actions:

Define actions to trigger based on Plex playback events.


Resume Handling (Optional):

The webhook reports a resume event when pausing then playing again, or when you start media that is part way through (continue watching).
The blueprint allows you to treat “resume” as “play” if desired.


Access Webhook Data:

Use payload.Metadata in templates to access data like cover art:

Example(s): 

Thumbnail (cover art)

{{ payload.Metadata.thumb }}


Here you can create the entire url to retreive the thumbnail:

{% set base_url = "http://<plex_server_ip>:32400" %} {% if payload.Metadata.thumb %} {{ base_url + payload.Metadata.thumb }} {% endif %}


For Artitst and Song Title:

{{ payload.Metadata.originalTitle  }} - {{ payload.Metadata.title }}

