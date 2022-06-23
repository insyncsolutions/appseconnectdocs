---
title: "Configuring Teams Bot"
toc: true
description: "Steps to configure Teams Bot in APPSeCONNECT"
keywords: "Teams App,appseconnect bot,integration through bot,configuration"
tag: developers
category: "Connectors"
menus: 
    botconnectors :
        title: "Configuring Teams Bot"
        weight: 3
        icon: fa fa-file-word-o
        identifier: teamsbotconnector
---

APPSeCONNECT Bot in Microsoft Teams allows you to build a communication channel between your line of business 
applications configured in APPSeCONNECT with Teams. The bot can notify you your daily sales report, Revenue, 
Customer information from your application in real time. You need to setup your BOT and connect to APPSeCONNECT
integration solution to communicate and get notified with actionable insights. 
Enable notifications and messaging from APPSeCONNECT regarding integrations, automations, data sync, triggered messaging, etc. 
to seamlessly manage your integration journey through Bots.

## Features

- Receive action-based notifications, either as adaptive cards or plain text on any public channel or specific user in Teams.
- Execute an integration directly from ProcessFlow to ensure the workflow defined in the integration is performed.
- Use Help to get insights about the configured commands in APPSeCONNECT.

## Pre-requisites

- **APPSeCONNECT** account with valid credentials.
- Need Microsoft Teams App with Administrative priviledges(to install APPSeCONNECT Teams App)
- Basic knowledge of APPSeCONNECT.

## Installing APPSeCONNECT

To install APPSeCONNECT, you need to be an administrator, such that either you install APPSeCONNECT on behalf of the whole organization
or you install for yourself. To install APPSeCONNECT, in your Teams App follow the steps below :

1. Open Teams and Click on the three dots on the extreme left side of the screen. 
2. Search "APPSeCONNECT", and click on the App you see on the list. 
![appseconnect_teams.png](/staticfiles/teamsapp/appseconnect_teams.png)
3. If you are unable to see APPSeCONNECT on the Search, go to Apps Section on Teams.
4. Search for APPSeCONNECT from the Search bar on top left corner. The APPSeCONNECT App will appear.
![appseconnect_app_search.png](/staticfiles/teamsapp/appseconnect_app_search.png)
5. Click on the App, you will see an Add button. Select whether you want to install it to Team, a Chat or a meeting. We recommend to add to a Team. 
6. Select a Channel Name where you want to install the BOT. Click Setup. Once this is done, you will see our Welcome message in the Channel.
![appseconnect_app_install.png](/staticfiles/teamsapp/appseconnect_app_install.png)

### Configuring APPSeCONNECT for Teams BOT

To create a communication channel between your BOT and APPSeCONNECT, there are few requirements that you need to follow. Here are the steps 
which are required to correctly work with APPSeCONNECT BOT. 

1. Open APPSeCONNECT Portal, create a ProcessFlow. 
2. Drag the Teams App and any other App of your choice. Remember, we are creating this ProcessFlow just to show you how to configure Teams in APPSeCONNECT. 
3. [Create a schema](/connectors/configuring-teams-bot/#create-a-proper-schema-based-on-the-data-you-want-to-send) to send messages from Teams. Either choose from existing Schema, or Create a new Schema. 
4. Your schema need to follow the Adaptive Card schema defined in [Microsoft Documentation](https://docs.microsoft.com/en-us/microsoftteams/platform/task-modules-and-cards/cards/cards-reference#adaptive-card)
**Note : To send an adaptive card - you can design your card in [Adaptive card designer](https://adaptivecards.io/designer/), then copy the Json payload and 
upload the Json as import schema. This step will auto-create your Schema, where you can specify the data in Adaptive card.**
5. Create the Action to send the notification. We use **conversations** action endpoint to send notification to an existing conversation to send a notification using `APPSeCONNECT Teams App`. 
![appteams8.png](/staticfiles/teamsapp/appteams8.png)
6. To receive the Message or Adaptive card, you need to mention the receiver information properly in 
Microsoft Teams APP action filter. Navigate to Microsoft Teams APP Node Configuration Window -> Configure 
Filter. Define the Receiver information in the Microsoft Teams App Action Filter properly as mentioned in the following scenerios. 
- To send information to a Specific Group Channel 
![appteams16.png](/staticfiles/teamsapp/appteams16.png)
- To send information to Multiple channels for a specific group 
![appteams17.png](/staticfiles/teamsapp/appteams17.png)
- To send information to specific user or multiple users
![appteams18.png](/staticfiles/teamsapp/appteams18.png)
- To send information to Multiple Groups and users at the same time 
![appteams19.png](/staticfiles/teamsapp/appteams19.png)  
7. Once you create the ProcessFlow, Deploy and execute the processflow in On-Premise or hosted environment. But before you do, you need to validate credentials in APPSeCONNECT.


### Credential Validation in On Premise Agent

Follow the steps below to validate credentials during deployment. 

1. In case you are in **On-Premise agent**, make sure you open validate your credentials. Open Teams credential, and use Authorize button to authorize 
your tenancy in Teams.
![appteams12.png](/staticfiles/teamsapp/appteams12.png) 
2. You just need to click on the **Authorize** button and sign up using an admin account. 
**Note - Admin consent is required to complete the configuration process.**
3. After clicking on the **Authorize** button the log in window will open and you need to provide the admin credentials and log in.
![appteams13.png](/staticfiles/teamsapp/appteams13.png) 
4. After log in it will do all the configurations automatically, and after completion it will show you a success message.
![appteams14.png](/staticfiles/teamsapp/appteams14.png) 
5. After you get a Success notification, you can continue the deployment process. Select your schedule information and Deploy the changes.
6. After a successful deployment, you will see your app is now connected with your APPSeCONNECT Account. 


When your setup is ready, you can create or install packages to add or enhance your integration between APPSeCONNECT and Teams.

### Create a Proper schema based on the data you want to send

1. If you want to send a normal text message 
   ![appteams2.png](/staticfiles/teamsapp/appteams2.png) 
   then the schema structure will be 
   ![appteams3.png](/staticfiles/teamsapp/appteams3.png) 
   The Mapping to send a normal message will be
   ![appteams4.png](/staticfiles/teamsapp/appteams4.png) 

2. If you want to Send a Proper adaptive card 
   ![appteams5.png](/staticfiles/teamsapp/appteams5.png)
   Then the schema structure will be 
   ![appteams6.png](/staticfiles/teamsapp/appteams6.png)
   The Mapping to send an adaptive card will be
   ![appteams7.png](/staticfiles/teamsapp/appteams7.png)

   >To send an adaptive card, you can design your card in Adaptive card designer, then copy the Json payload and 
   upload the Json as import schema and do the proper mapping. Based on the notification you want.        

