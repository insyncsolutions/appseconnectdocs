---
title: "Redeployment"
toc: true
tag: developers
category: "Processflow"
menus: 
    deployment:
        title: "Redeployment"
        weight: 3
        icon: fa fa-file-word-o
        identifier: redeployprocessflow
---

Redeploying processflow functionality allows you to re-deploy an existing processflows (deployed/deployed and executed) 
to the same environment in order to make any changes and execute the integration process. 
Users, can redeploy the changes made in the processflows and there can be various types of 
changes pertaining to redeloying a processflow.

## Causes for Redeployment of ProcessFlow 

1) Addition of a new node.  
2) Deletion of an existing node.  
3) Changes in Mapper node/Mapping.  
4) Changes in Lookup Mapping - Addition, Deletion & Updation.  
5) Updating Credential Token.    
6) Updation in Action Filter & Runtime Filter.    

### Prerequisites to re-deploy ProcessFlows

1.	Should have valid credentials for logging in to the APPSeCONNECT portal.
2.  A [deployed processflow](/processflow/deploying-and-executing-processflow/) should be available to make the changes for redeploying.  

### Steps to re-deploy ProcessFlows to an Environment

1.	Login to the portal and navigate to the **processflow** module available on the left menu.  
2.  Choose the processflow which is already deployed, make the necessary changes and click on the **deploy button** in the processflow Designing Page.   
![Deploy Processflow2](../../staticfiles/processflow/media/deploy-processflow21.png)

3.  The deploy wizard appears where you can redeploy the processflow by making any changes.
4.  You can view the **Environment** section is already selected (remains same as chosen earlier)
    and the remaining part is in disabled Mode. This means if your selected environment is 
   `On-Premise` then Hosted will be in disabled mode and vice-versa. Make sure to check the
    envirnonment is in connected state.    
    **NOTE: If the environment is in disconnected state, you will get an error message -
`Environment is not enabled` and thus you cannot proceed with further deployment steps**. 
![Redeploy Processflow](../../staticfiles/processflow/media/redeploy-processflow.png) 

5. Click NEXT button, the selected apps and its adapters in the designed processflow would get downloaded.
6. The screen navigates to the **Set-up Connection** section of the Deploy wizard. Select the credential from the drop down, 
for the respective application used in the processflow. Previously chosen credentials will be selected if exists in the processflow, 
incase of new credentials added to the application will be visible in the drop down list. Choose the credential as required.   
![Redeploy3](../../staticfiles/processflow/media/redeploy3.png)

7. Click `Refresh Connection` button. You will get the latest credentials or updates to credentials made in the OP Agent. 
Now Click on the NEXT button.
8. The screen navigates to the **Lookups** section of the Wizard, where you can view the existing lookups implemented
 while mapping the attributes. During the redeployment of processflow, latest fixes will 
 be displayed with selected Reference Table with a green tick.

    * User will have the option to re-assign preassigned `Reference Table` as well as fix new `Reference Table`.
    * If a `Reference Table` has already been selected during a processflow deployment 
 and then the Lookup Mapping or the Reference Table is deleted (from the Lookup Repositories), 
 then during Redeployment process, the deleted lookup mapping will show as an unresolved 
 warning which the user may fix if desired.
![Redeploy5](../../staticfiles/processflow/media/redeploy5.png)  

9. Click Next, the screen navigates to the **Sync and Retry** section of the deploy wizard. You can choose or change the configuration from 
Manual/Auto for re-deploying the processflow.  To know more about Sync & Retry [Click Here](/processflow/deploying-and-executing-processflow/#Sync and Retry : On Premise)

10. After configuring the sync and retry section, click Finish button. 
The processflow would be successfully re-deployed.   

You can view these messages processflow Publish Started, processflow Publish Completed, 
Downloading processflow Data, Downloading XSLT Files, Deployed etc. while re-deploying. 
click the Finish button. Following the above steps, you can successfully Re-deploy and Execute 
a processflow.

**NOTE: (a) You can redeploy a processflow by clicking `Deploy` button in the designer. 
(b) Before redeployment starts, the agent will take a backup of the previously deployed 
XSLT of the specific processflow, processflow database, along with dependent data. 
(c) If redeployment of the processflow fails, the agent will automatically restore backed up configuration 
after pending time outs. 
(d) After successful deployment, the deploy button will get enabled** 








 








