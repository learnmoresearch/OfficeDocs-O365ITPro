---
title: "Yammer file storage overview"
ms.author: v-irpast
author: IrenePasternack
manager: pamgreen
ms.date: 5/28/2019
audience: Admin
ms.topic: article
ms.service: yammer
localization_priority: Normal
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
description: "Where files are stored in Yammer depends on whether or not the network is using Office 365 connected groups."
---

# Yammer file storage overview

As of May 2019, Yammer is rolling out changes to file storage for files uploaded to Yammer in Office 365 connected Yammer groups. Formerly, all files uploaded to Yammer were stored in Yammer cloud storage. Once your organization gets these changes, all new files uploaded through Yammer in Office 365 connected Yammer groups will be stored in the group's SharePoint document libraries. These files can still accessed from within Yammer. 

For information about using Yammer files stored in SharePoint, see the following topics: 

- [Where are my Yammer files stored?](https://support.office.com/article/how-do-i-tell-where-my-yammer-files-are-being-stored-fadfdefa-e00d-40b6-94cb-a9ddb171a443)

- [Attach a file to a Yammer message](https://support.office.com/article/attach-a-file-or-image-to-a-yammer-message-f576d4d1-ad66-4ce4-9c43-46cf75978dbf)

- [Edit documents from Yammer](https://support.office.com/article/edit-documents-from-yammer-913dbeab-7efd-4789-8f4d-a666fe315d85)

- [Edit a previously uploaded file when your Yammer connected group now stores files in SharePoint](https://support.office.com/article/edit-a-previously-uploaded-file-when-your-yammer-connected-group-now-stores-files-in-sharepoint-4b2cfde2-871e-4f0d-9936-db5a57ef5f87)

## Benefits

For network and tenant administrators:

- SharePoint has a rich set of security and compliance features that will now apply to files uploaded in Yammer for Office 365 connected Yammer groups, including eDiscovery, data loss protection, and in-geo residence for files at rest.  

For end users: 
  
- A familiar user interface for file navigation and management in SharePoint. 
  
- Better file organization using folders to organize content.
 
- Greater discoverability and easier access via Microsoft search. 

    Users with appropriate permissions can find and access the files through Yammer, and can also access the files through SharePoint and other Office 365 resources by using browse or search in SharePoint and Delve.  
     
- Offline access to files by syncing a SharePoint folders to a folder on their computer.  

## What determines where a file is stored    
 
Files are stored in SharePoint when they are uploaded to an Office 365 connected Yammer group. This includes:  
  
- Files that are attached to a message in an Office 365 connected Yammer group.  

- Files that are uploaded to a group from the **Files** page of an Office 365 connected Yammer group. 
 
- Files that are attached to an email that is sent to an Office 365 connected Yammer group.   
  
Files will continue to be stored in Yammer cloud storage in the following instances:   
 
- If the Yammer network does not use Office 365 connected groups. This includes:
 
  - Office 365 tenants that have more than one Yammer network  
  
  - Yammer  networks that don't enforce Office 365 identity  

  - Yammer Basic networks  
 
- When the location the file is being uploaded to is not an Office 365 connected Yammer group: 

    - Groups that are not Office 365 connected groups, including All Company, external groups, and secret groups.   
  
    - Yammer private messages.  
  
    - Existing files stored in Yammer legacy storage will not be moved to SharePoint.  

 > [!NOTE]
 > Moving a conversation to an Office 365 connected Yammer group will not change where the file is stored. 
  
## Where files are stored in SharePoint
 
Files that users upload in Office 365 connected groups are saved in the **Apps > Yammer** subfolder of the SharePoint document library for the Office 365 connected group. The SharePoint document library can be accessed from Yammer under **Office 365 Resources** on the right side of an Office 365 connected Yammer group, as well as through SharePoint itself.   
  
## Guest and external user access to files
  
The following table shows how each type of guest and external user can access files uploaded in Yammer and stored in SharePoint.

|||
|----------|----------|
|**Type of user**|**Access to group files**|
|**Conversation-level guest that is in your network**|**Private group**: can view files that have been shared in the conversation, but can't upload files.<br>**Public group**: Can view, edit, and upload files.|
|**Network-level guest that is also an Azure B2B guest, and also a member of the group in Office 365**|Can view, edit and upload files.|
|**Azure B2B guest, but not a member of a the group<br/>Network-level guest<br/>Conversation-level guest that is not in your network**|No file access by default. These users can request access to specific files.<br/>Can't upload files.|
|**Network-level guest, but not Azure B2B guest**| No file access. These users must become an Azure B2B guest and a member of the group in Office 365. Alternatively, other group members can grant access to specfic files or the entire document library via one of many SharePoint external sharing methods.|
|||

> [!NOTE]
> Membership in the group for guests in Azure Active Directory (AAD) and Yammer are completely separate. Deleting a network-level guest from an Office 365 connected Yammer group or from the tenant in AAD does not remove the user in Yammer, and deleting a user from Yammer does not delete the user from an Office 365 group or AAD. 

For more information about Azure B2B guests, see [Guest user access in an Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).