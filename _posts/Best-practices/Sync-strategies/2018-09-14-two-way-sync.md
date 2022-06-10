---
title: "Two-Way Sync Strategy"
toc: true
description: "Get to know about our two-way data synchronization to successfully perform your business integration."
keywords: "two way sync, two-way sync, Conflict Management Technique, Circular Update Management, Distinctly identify updates from User vs Integration platform, Automatically merge data with Conflict management"
tag: developers
category: "best-practices"
menus: 
    bp:
        title: "Two-Way Sync Strategy"
        weight: 2
        icon: fa fa-wpexplorer
        identifier: bptwoway
---

`Two-Way` or `Bidirectional` synchronization enables you to define an integration where both applications are getting parallelly updated. 
Practically two-way sync is defined as a two one-way sync between two applications where both the application can update the applications back and forth. 
This sync strategy is most often required in situations like customers, contacts, vendors etc 
rather than invoices, quotes, orders, etc. Bidirectional synchronization updates are sometimes critical and require manual 
conflict management which in most cases not recommended. 

# Challenges

As `two-way` sync requires the same recordset to be updated multiple times, there are some 
challenges that need to be kept in mind before doing the actual integration.

## Conflict Management Technique 

As two applications involved in sync operation can both update the same record, there could be conflicts between them. 
In scenarios where the same record or same data has been updated in both the places before you start the sync 
operation, it would be an anomaly to decide which one we should take and which one to reject. In such cases, 
we mark one application as `Master` and another as a `Slave`, the integration tries to merge unique values together 
while it automatically rejects the slave updates (if any) if there is any conflict between the two apps. 
When two-way sync is performed, the data which is in the conflict in a slave is rejected and updated with the 
one in master. 

## Circular Update Management 

Sometimes when an application always finds a new update for the same record in place, there might be a situation 
of circular update. Let us suppose that an update to a record generates new modified time for a record. 
The integration looks for new changes and finds the record again to update. It then updates the application to 
the other application and changes the modified date again. This process continues. 

To solve these challenges, we can device two methods :

- Distinctly identify updates from User Vs Integration  
- Automatically merge data with manual conflict management  

## Steps to solve the challenges

### Distinctly identify updates from User vs Integration platform

This method enhances the flag based approach and stores some additional data that is triggered only when the data is 
modified or added through the integration platform. In such a case the platform knows the context and does additional 
stuff that ensures the flag is unset only when the data operation is performed from user interfaces. 

**Pros and Cons**

- The approach is best suited for Two-way sync and addresses all the challenges. It enhances the Flag based approach to ensure it identifies the user context. 
- The approach makes the integration little complex as both side customizations needed. 
- It does not require additional cost but not all applications support this. 

### Automatically merge data with Conflict management

Sometimes it is important for the integration platform to decide which data to update and which not. In merging the cells, 
the integration platform allows to choose the right value based on the record update or based on the `Master-Slave` relationship 
mentioned beforehand. It is important to note, this kind of approach also produces conflict and the conflict is being put into 
the data bucket for a manual fix. 

**Pros and Cons**

- This approach requires manual intervention in some cases, which might delay the record update of certain conflicting recordsets.
- As conflicts are managed automatically by merging data together, there might be some cases where the data is wrongful.

