---
title: Changing CRM 2011 Web Services Port via Deployment Manager
author: admin
layout: post
permalink: /2011/02/25/changing-crm-2011-web-services-port-via-deployment-manager/
categories:
  - Microsoft / CRM / SharePoint / SSRS
---


Web services don’t work when we access them from Settings -> Developer Resources! It’s because we changed our port to 85 and we haven’t updated the web services location to 85 (when I changed the bindings)! This means that it’s actually pointing at the Share Point web services (and it bombs out). Open up deployment manager.

![][2]

 [2]: /images/old/CRM2011_Web_Services_Menu_1.png

Click properties on the right hand side.

![][3]

 [3]: /images/old/CRM2011_Web_Services_Dep_2.png

Click Web Address up top. Change the port from 80 to 85.

![][4]

 [4]: /images/old/CRM2011_Web_Services_80_85_3.png

If you still have errors, you might need to delete your bindings off of your website (which is ironic, since I asked you to change localhost to win-b80icqrvluf to fix that problem. I ended up deleting my bindings and everything still worked (so I’m not sure why it ended up fixing the file upload by changing localhost to win-b80icqrvluf, maybe someone out there knows?). 

![][5]

 [5]: /images/old/CRM2011_Web_Services_Delete_Bindings_4.png

Everything be ready to go now! Install Visual Studio 2010 on your VM (I’ll leave that up to you (for now)!). 

Expect more articles regarding development, tips (and probably a rant or two)!