---
title: "APPSeCONNECT APP and its configuration with Microsoft Teams APP"
description: "APPSeCONNECT APP and its configuration with Microsoft Teams APP"
keywords: "APPSeCONNECT APP in Teams,Teams APP integration with organization"
toc: true
tag: developers
category: "Connectors"
menus: 
    Connectors :
        title: "APPSeCONNECT APP in Microsoft Teams APP"
        weight: 7
        icon: fa fa-file-word-o
        identifier: configuringappseconnectteamsapp
---

APPSeCONNECT APP in Microsoft Teams app store will send you notifications based on the ProcessFlows you create in 
the APPSeCONNECT Web Portal. These notifications can be your Sales Report, Revenue, Customer information 
based on your CRM, Real time new customer add, Real Time new Order place etc. 
Enable notifications and messaging from APPSeCONNECT regarding integrations, automations, data sync, triggered messaging, etc. 
Seamlessly manage your integration journey and receive all updates on the go.

**Points to Note** :

- Receive action-based notifications, either as adaptive cards or plain text.

- Receive notifications on any public channel on Microsoft Teams groups or any specific active user.

- Receive updates from APPSeCONNECT ProcessFlow for real-time or scheduled integrations, as configured by the you (new customers, new orders, revenue details, etc.)

## Pre-requisites

- **APPSeCONNECT** account with valid and proper credentials.
- Need to have Microsoft Teams in your organization and allow 3rd Party APP Installation.
- Basic knowledge of APPSeCONNECT.

### Configuring APPSeCONNECT APP with any other APP

You need to follow the below mentioned steps to configure APPSeCONNECT APP with other APPs.

1. Create a ProcessFlow with source application and Microsoft Teams as your destination application.  
2. Drag your source application from the Left side APP list from the ProcessFlow designer window and do the 
node configurations properly based on your needs. 
3. Drag the Mapper node and Microsoft Teams APP from the Left side APP list and do the node configurations properly.
![appteams1.png](/staticfiles/teamsapp/appteams1.png)

4. Create a proper schema or select a schema based on the data you want to send from the Manage Schema window.  
a) If you want to send a normal text message,
![appteams2.png](/staticfiles/teamsapp/appteams2.png)

then the schema structure will be as mentioned below,
![appteams3.png](/staticfiles/teamsapp/appteams3.png)

and the mapping to send a normal message will be as mentioned below.
![appteams4.png](/staticfiles/teamsapp/appteams4.png)

b)  If you want to send a Proper adaptive card,
![appteams5.png](/staticfiles/teamsapp/appteams5.png)

then the schema structure will be,
![appteams6.png](/staticfiles/teamsapp/appteams6.png)

and the mapping to send an adaptive card will be as follows.
![appteams7.png](/staticfiles/teamsapp/appteams7.png)

**Note : To send an adaptive card – you can design your card in Adaptive card designer, then copy the Json payload and 
upload the Json as import schema and do the proper mapping, based on the notification you want.**

5. Create the Action to send the notification or the specific task you want to achieve by providing an api endpoint. 
To send a notification using APPSeCONNECT Teams App the action endpoint should be 
**conversations**, you can also choose different actions based on the Api endpoint you want to hit.   
![appteams8.png](/staticfiles/teamsapp/appteams8.png)

6. Now to receive the message or **Adaptive card**, you need to mention the receiver information properly in 
Microsoft Teams APP action filter. For this go to **Microsoft Teams APP** Node configuration window -> Configure 
Filter and define the receiver information.

- To send to a Specific Group Channel, provide the action filter as 
  group -> <group_name> --> channel -> <channel_name>
![appteams9.png](/staticfiles/teamsapp/appteams9.png)


  - To send to Multiple channels for a specific group, provide the action filter as 
  group -> <group_name> --> channels -> <channel_name_1> + <channel_name_2>
![appteams10.png](/staticfiles/teamsapp/appteams10.png)

**Note : For Multiple channels please provide (+) separator.**


- To send to specific user or multiple users, follow the below mentioned steps.  
![appteams11.png](/staticfiles/teamsapp/appteams11.png) 

- To send Multiple Groups and users at the same time, provide the action filter as 
group -> <group_name> --> channels -> <channel_name_1> + <channel_name_2> && group -> <group_name> --> channel -> <channel_name> 


7. Link **source node**, **mapper node** and **destination node** after proper node configuration and mappings.Here, we have created 
a ProcessFlow with **Magento** as our **source Application** and **Microsoft Teams** as our 
**destination application**.

8. Deploy and execute the processflow in On-Premise or hosted environment as and when required to the get full flaovour of our smart, smooth and free-flowing intregratyions.

### Credential Validation of your choosen Applications

- In your **On-Premise** agent, both your source and destination application is available. Get to know the way to validate credentials for
[magento](/connectors/magento2/) and for Microsoft Teams App click on the (+) icon to provide a new credentials.
![appteams12.png](/staticfiles/teamsapp/appteams12.png) 

- You just need to click on the **Authorize** button and sign up 
using an admin account. Provide the admin consent for some Read only scopes. 

**Note - Admin consent is required to complete the configuration process.**

- After clicking on the **Authorize** button the log in window will open and you need to provide the admin credentials and log in.
![appteams13.png](/staticfiles/teamsapp/appteams13.png) 

- After log in it will do all the configurations automatically, and after completion it will show you a 
success message.
![appteams14.png](/staticfiles/teamsapp/appteams14.png) 

- After a success message you can continue with the deployment process by proving the newly added 
Microsoft Teams credentials. Provide the Auto or Manual execution as per your choice.

-  After a successful deployment, you can manually execute the ProcessFlow, if you choose the 
execution mode as manual. Else, you choose auto execution. Then you will get notified to the Proper Group –
Channel or user in your organization teams which you have configured in the Action filter.
![appteams15.png](/staticfiles/teamsapp/appteams15.png)

**Note :**

- Here on this above ProcessFlow, we have configured as, it will notify to a Specific Channel every week about the 
newly joined customers. So, we have set it on automatic execution mode.

- Based on your need you can set Automatic or Manual execution, for this you need to mention the 
Receiver information on Specific Group - Channel properly in the Microsoft Teams APP Action Filter.  







