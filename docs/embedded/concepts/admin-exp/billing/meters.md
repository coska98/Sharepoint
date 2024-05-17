---
title: SharePoint Embedded Meters
description: This article describes the the meters in SharePoint Embedded.
ms.date: 05/21/2024
ms.localizationpriority: high
---

# SharePoint Embedded Meters
SharePoint Embedded employs a pay-as-you-go (PAYG) billing model through an Azure subscription. Billing is determined by how much data in GB you store in SharePoint Embedded, transactions used to access and modify, and data that is egressed from SharePoint Embedded platform. Each of these factors contributes to the overall cost, ensuring that you only pay for the resources and services you use. You can view this usage in the [Azure Cost Management](https://ms.portal.azure.com/) portal as meter events through the Azure subscription it chooses. 

SharePoint Embedded has three billing meters:

| &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  SharePoint Embedded Service Meters &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  Meter Unit &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| :--------------------------------:   | :----------:   |
|              Storage                 |   $/GB     |
|   Graph API Transactions             | $/Transactions    |
|           Egress                     |  $/GB      |


## Storage
Storage consumption meters in SharePoint Embedded apply to the storage used by files, documents, metadata, versions of files and documents. Storage consumption also includes all content in the recycle bin within SharePoint Embedded containers.


## API Transactions 
Graph API calls made explicitly by the SharePoint Embedded application towards containers or container content are counted as transactions, and customers are billed based on the number of these transactions. See the [examples](https://learn.microsoft.com/en-us/graph/api/resources/filestoragecontainer?view=graph-rest-beta) of  Graph API that can act on the containers and the container contents.

However, calls made by internal services to the containers, which the application has no control over, are **not** chargeable. Some examples of such non-chargeable transactions include:

1. Queries performed by the eDiscovery service to search through container content for compliance or legal purposes.
2. Admin actions taken by the Sharepoint Embedded admin or Global Admin on containers through SharePoint Admin Center or SPO PowerShell.

## Egress
Egress refers to the data dowmloaded from the SharePoint Embedded platform to the customer's client device. Eligible scenarios for egress charges include downloading files and videos from the SharePoint Embedded application to a customer's client device, such as a desktop or mobile device.

However, certain types of data transfers are exempt from egress charges. These exemptions ensure that customers are not billed for data transfers occurring within integrated Microsoft services, promoting seamless usage without additional costs for these specific internal operations. Some examples of these exemptions include:

1.	File downloads from the SharePoint Embedded application server to the customer's Office Desktop client are not charged.
2.	File downloads from the SharePoint Embedded application server to the Web Application Companion (WAC) are not charged.


