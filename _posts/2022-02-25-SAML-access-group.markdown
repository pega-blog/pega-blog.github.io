---
layout: post
title:  "Mapping Access Groups from SAML Message"
date:   2022-02-25 19:09:36 +0100
categories: integration security
---

Need: assign OperatorID to an Access Group based on SAML message. Mapping from SAML message to Access Group isn't 1:1, so some calculation is required. 

Access Group or it's mapping could change in the future, so list of Access Groups should be refined every time OperatorID logs in. 
    
Data transform for users runs only when new user should be created (makes some sense) and it runs before mapping from "Mapping" tab (doesn't make sense at all):

![Model Operator](/assets/model-user.png)

So in the situation when during an Operator lifetime their Access Group got changed in the source system (lets say LDAP) - then we wouldn't be able to handle it on login.

Pega doesn't reccommend to change Access Groups and Defaut Access Group in the Post Auth activity and it really limits possibility of mapping to Pega Access Groups from SAML data (in my case SAML message has semicolon separated list of roles).

But Pega allows to use Functions on the Mapping tab, so we can run Data Transform from the function where we can parse SAML attribute and map Access Groups before Post Auth activity. This is important to do it before Post Auth because Post Auth activity executed in the context of default Access Group.

![OperatorID Mapping](/assets/operatorid-mapping.png)

pyNote is just some property, so Pega wouldn't complain.

![OperatorID Mapping](/assets/operatorid-mapping-dt.png)

Pega doesn't have OOTB function to run Data Transform (it has some, but they have problems with Param page), so I created my own. 

And now it works.
