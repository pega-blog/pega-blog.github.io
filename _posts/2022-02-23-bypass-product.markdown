---
layout: post
title:  "Import Only New Instances of Specific Classes"
date:   2022-02-23 19:09:36 +0100
categories: rules
---

When work with DSS usually those settings are different for each environment, should be configured only once and never be overwritten with future deployments. Previously devs had to remove DSS association with Rule Set and move such products manually or be really carefull during the deployment.

But now Pega provides new configuration on the Product rule:
![OperatorID Product Warning](/assets/bypass-dss.png)


[Source](https://wiki.pega.com/index.php/Manage_data_instances_during_update)