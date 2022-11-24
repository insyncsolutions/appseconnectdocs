---
title: "Detailed Sync Report"
toc: true
tag: developers
category: "Rule"
menus: 
    preconfigurerule:
        title: "Detailed Sync Report"
        weight: 18
        icon: fa fa-wpexplorer
        identifier: preconfigurerulelog
---

## Introduction

`Integration` is a continuous process which gives the flexibility to the users to run an integration procedure again and again
based on the schedule defined by the user. As the process executes in background without any human intervension, it gives 
the user a piece of mind such that the data syncs seamlessly. But occassionally there might be a situation where the integration 
stops all of a sudden and the user who is not regularly monitoring them, does not get any clue about it. This rule will identify any 
issue in the platform and generate notification based on various parameters, such that any decrepancy could be identified easily.
  
`Workflows` provides you a flexibility to sync your data between 2 or more business applications in a smooth and free-flowing 
manner. You can execute these `workflows` manually as well as can schedule them for a latter time. While executing 
these `workflows` in `OP` or `Cloud` agent, it might happen that the information might not be synced successfully. 
In such scenerios, the `UNPROCESSED` ,`ERROR` and `SKIPPED` datas will be `mailed` to you in the mail id provided at the 
time of creating your account in `portal`. 

## How to use the Rule

As `DetailedSyncReport` is a `Pre-packaged` & `Pre-configured` rule, you can use this with a `single click` from the 
enivronment section of every organization. Follow the below mentioned steps to `Deploy/Undeploy` this rule in your respective 
organization. 

- Login to `portal` with any valid login credentials. 
- From the `Home` page, naviagte to `Deploy` -> `Environments`. 
- Expand the node `On-Premise`. Select any environment where your workflow are deployed and executed. Click on the `Rules`.
![detailedsyncreportprocessflow2](/staticfiles/rules/media/detailedsyncreportprocessflow2.png)
- On clicking the ellipses button(...), you will get to deploy the rule in your organization. If you, do not 
deploy the rule in your own organization, email will not be triggered such that you can get to know the touchpoints that 
have errors while in execution.
![detailedsyncreport1](/staticfiles/rules/media/detailedsyncreport1.png)

## Hourly Report Rule

|Event used|Token used |
|---|---|
|Hourly Based Sync Report|~{ReSyncBucketWithinScheduledTime("Error","Skipped")}~|

# Rule Notification

Users would receive the `hourly report` in the `email id` provided for the Organisation. The email would consist 
of the sync report(for failed transaction during the execution process) for the previous hour. The mail will 
consists of the `Conection Name`, `TouchPoint Name`, `SourceId`, `TransactionTS` and `Status`. 
![detailedsyncreport](/staticfiles/rules/media/detailedsyncreport.png)

**Note**  
- In-case all the data has been transacted successfully, then the user/implementor will not receive any mail.           
- You will not recieve the `Detailed Sync Report` if the subscription of your organisation has expired.
- In case of Hosted Environment, you can deploy/undeploy the rule similarly and shall receive the mail.
- Also, by default, the token for sending mails is set as ${orgEmails}$ which represents, that all users of the same organization will receive the notifications.       
- Users can provide the specific recipient email address directly to mail field for sending the notification to selective users.


