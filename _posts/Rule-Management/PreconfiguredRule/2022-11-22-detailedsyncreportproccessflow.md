---
title: "Detailed Sync Report Processflow"
toc: true
tag: developers
category: "Rule"
menus: 
    preconfigurerule:
        title: "Detailed Sync Report Processflow"
        weight: 19
        icon: fa fa-wpexplorer
        identifier: detailsyncreportprocessflow
---

## Introduction

`Integration` is a continuous process which gives the flexibility to the users to run an integration procedure again and again
based on the schedule defined by the user. As the process executes in background without any human intervension, it gives 
the user a piece of mind such that the data syncs seamlessly. But occassionally there might be a situation where the integration 
stops all of a sudden and the user who is not regularly monitoring them, does not get any clue about it. This rule will identify any 
issue in the platform and generate notification based on various parameters, such that any decrepancy could be identified easily.     

While using `Processflows` to perform such integrations, you can schedule your processflow in `manual` or `auto` mode 
as per your requirement in `OP` or `Cloud` agent. These procesflows will retrieve and update specific data 
from respective `source` and `destination` application. However, it might happen that few informations may not be processed to the 
destination application as expected. In such scenerio, `DetailedSyncReportProcessflow` will be useful to any users/implementors. 

## How to use the Rule

As `DetailedSyncReportProcessflow` is a `Pre-packaged` & `Pre-configured` rule, you can use this with `single click` from the 
enivronment section of every organization. Follow the below mentioned steps to `Deploy/Undeploy` this rule in your respective 
organization. 

- Login to `portal` with any valid login credentials. 
- From the `Home` page, naviagte to `Deploy` -> `Environments`. 
- Expand the node `On-Premise`. Select any environment where your processflow are deployed and executed. Click on the `Rules`.
![detailedsyncreportprocessflow2](/staticfiles/rules/media/detailedsyncreportprocessflow2.png)
- On clicking the ellipses button(...), you will get to deploy the rule in your organization. If you, do not 
deploy the rule in your own organization, email will not be triggered such that you can get to know the processflow that 
have errors while in execution.
![detailedsyncreportprocessflow3](/staticfiles/rules/media/detailedsyncreportprocessflow3.png)

## Rule Notification

Users would receive the `hourly report` in the `email id` provided for the Organisation. The email would consist 
of the sync report(for failed transaction during the execution process) for the previous hour. The mail will 
consists of the `time frame` for which the report has been generated, `ProcessFlow` folder name, `name of the processflow` and 
the number of errors encountered during the execution the process. On clicking the, `ProcessFlow` folder name, the `Sync Info` 
will open up showing you the `success` and `erroneous` data. 
![detailedsyncreportprocessflow1](/staticfiles/rules/media/detailedsyncreportprocessflow1.PNG)

**Note**  
- In-case all the data has been transacted successfully, then the user/implementor will not receive any mail.           
- You will not recieve the `Detailed Sync Report` if the subscription of your organisation has expired.
- In case of Hosted Environment, you can deploy/undeploy the rule similarly and shall receive the mail.

