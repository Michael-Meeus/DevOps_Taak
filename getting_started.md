# Volledige tutorial van Google zelf: 
https://codelabs.developers.google.com/codelabs/actions-1/#0

# Eigen Getting Started:

# Nakijken van Google permission settings

## Nodige permisies om Actions te kunnen gebruiken:

    Ga naar ‘Activity Controls' page (https://myaccount.google.com/activitycontrols).
    Login met Google account indien nodig
    Zorg dat de volgende permisies enabled zijn:

    Web & App Activity (you should also enable the option to ‘Include Chrome history')
    Device Information
    Voice & Audio Activity


# Project aanmaken op: https://console.actions.google.com/
 -> New Project

 ![New Project](https://codelabs.developers.google.com/codelabs/actions-1/img/c19fb72194296e56.png)
 
 -> Kies Conversational
 ![Conversational](https://codelabs.developers.google.com/codelabs/actions-1/img/4241cbc92f5c6b42.png)
 

    Klik op Build your Action en kies Add Action(s).
    Klik op Add your first action.
    Bij de Create Action dialog, kies voor Custom Intent en klik Build.
    In de Dialogflow Console, klik op Create:
    
 ![Create](https://codelabs.developers.google.com/codelabs/actions-1/img/12b008c60c6dcf9d.png)
    
# Importeren van project

To access the export and import settings, click the Export and Import tab.

This feature allows you to export/import an agent to/from a zip file for backing up agents or transferring them from one account to another. While you can edit the JSON files directly and re-import them, editing should be done using the Dialogflow Console or API. This ensures that changes are validated by the system and keeps troubleshooting to a minimum.

The following are not included in the export of an agent:

    Inline editor files package.json and index.json
    Integration settings for the agent.

## Verder altijd zorgen dat de Webhook onder Fulfillment enabled is!

 ![Create](https://codelabs.developers.google.com/codelabs/actions-1/img/98b20a2f25f954c6.png)

## En dat de taalsettings juist staan, op Nederlands in ons geval:

 ![Create](https://cloud.google.com/dialogflow/docs/images/add-a-language.png)
 
# Opzetten database en resources

Ga naar https://console.firebase.google.com

## Firebase Realtime Database

Import JSON (resources/it-project-test-ahukuq-export.json) in Database
 ![Database](https://github.com/Michael-Meeus/Osudio_IT_Project/blob/dev/docs/Adding_database.png)

## Storage

Upload contactsfile (resources/Contacts.vcf) naar Storage

 ![Storage](https://github.com/Michael-Meeus/Osudio_IT_Project/blob/dev/docs/Import_contacts.png)


# Deployen van project vanuit de source code folder op local machine

## Dependencies

Navigeer naar part-picker/functions folder en installeer dependencies:

```
npm install
```

### Deploying naar firebase

Het projectID van eigen project kan teruggevonden worden in de Dialogflow Console onder Settings : General

 ![ProjectId](https://github.com/Michael-Meeus/Osudio_IT_Project/blob/dev/docs/ProjectId.png)
 


```
firebase deploy --project _projectId_
```

# Project delen of developers toevoegen:

Bij settings van het project op het tabblad Share accounts toevoegen.

https://cloud.google.com/dialogflow/docs/access-control

# Role Management
## Via Cloud Identity and Access Management (Cloud IAM) 

https://cloud.google.com/iam/docs/
  
## Via Dialogflow Console

https://cloud.google.com/dialogflow/docs/console
  
  
  
  
  
