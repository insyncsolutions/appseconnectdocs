---
title: "SAP B1 DISERVER Restart"
toc: true
tag: developers
category: "Rule"
menus: 
    preconfigurerule:
        title: "SAP B1 DISERVER Restart"
        weight: 20
        icon: fa fa-wpexplorer
        identifier: sapb1diserverrestartrule
---

## Introduction

`Integration` is a continuous process which gives the flexibility to the users to run an integration procedure again and again
based on the schedule defined by the user. As the process executes in background without any human intervension, it gives 
the user a piece of mind such that the data syncs seamlessly. But occassionally there might be a situation where the integration 
stops all of a sudden and the user who is not regularly monitoring them, does not get any clue about it. This rule will identify any 
issue in the platform and generate notification based on various parameters, such that any decrepancy could be identified easily.     

While using any `Processflow` with `SAP B1` as the source or destination application to perform any business integrations, 
the `DI-SERVER` should be runnig in your local system. Further, you can schedule your processflow in `manual` or `auto` mode 
as per your requirement in `OP` or `Cloud` agent. These procesflows will retrieve and update specific data 
from respective `source` and `destination` application. However, it might happen that, while you are performing data sync between 
any business application and `SAP B1`, the sync may not occur properly. To overcome, such situations `SAP B1 DI-SERVER` comes into the scenerio.  

## How to use the Rule

As `SAP B1 DI-SERVER Restart Rule` is a `Pre-packaged` & `Pre-configured` rule, you can use this with `single click` from the 
enivronment section of any organization. Follow the below mentioned steps to `Deploy/Undeploy` this rule in your respective 
organization. 

- Login to `portal` with any valid login credentials. 
- From the `Home` page, naviagte to `Deploy` -> `Environments`. 
- Expand the node `On-Premise`. Select any environment where your processflow are deployed and executed. Click on the `Rules`.
![detailedsyncreportprocessflow2](/staticfiles/rules/media/detailedsyncreportprocessflow2.png)
- On clicking the ellipses button(...), you will get to deploy the rule in your organization. If you, do not 
deploy the rule in your own organization, it will not try to restart the `DI-SERVER` during the integration process.   
![sapb1diserverrestartrule](/staticfiles/rules/media/sapb1diserverrestartrule.png)    

## Rule Notification

The rule will detect if `DI-SERVER` is non-functional based on logs, if so, 
then tries to restart the `DI-SERVER` via function defined in SAP B1 application. 
You can see the logs in your local system from the location where agent is installed. 
Open the `OP` agent, copy the `Service Output Path` and navigate to this location. Click on `Log` and open the folder 
on the day, which you want to see the `DI-SERVER` status. Open the `SchedulerRules` file and you will get to see all the details 
regarding `SAP B1 DI-SERVER`.

