---
title: Metadata error when setting up the CRM 2011 Email Router
author: admin
layout: post
permalink: /2011/08/01/metadata-error-when-setting-up-the-crm-2011-email-router/
categories:
  - Microsoft / CRM / SharePoint / SSRS
---


Here’s a new error I ran into when setting up the email router:

> The E-mail Router Configuration Manager was unable to retrieve user and queue information from the Microsoft Dynamics CRM server is busy. Verify that URL  is correct. Additionally, this problem can occur if specified access credentials are insufficient. To try again, click Load Data. (Metadata contains a reference that cannot be resolved: ‘crmserver/XrmServices/2011/Discovery.svc?wsdl’.)

![][2]

 [2]: /images/old/Metadata-Error.png

Basically this error is saying that it can’t connect to the URL. The reason I ran into this issue was because we were having DNS issues and couldn’t connect to the server. Hope this helps as the error is slightly cryptic (saying it’s busy).