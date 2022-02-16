---
layout: post
title:  "OperatorIDs in Product Rule"
date:   2022-02-22 19:09:36 +0100
categories: rules
---

Something new, that I haven't seen before:
![OperatorID Product Warning](/assets/operatorid-product.png)

Be aware if you want to have propagate some OperatorIDs (like Model Operator in my case) to test/stage/prod. By default Pega will not update OperatorID included into package at all. You can to enable "Advanced" import and do it manually.

Guess they did it for security reasons and it will work for most situations, but in case of Model Operator I really don't expect it.


[Source](https://community.pega.com/knowledgebase/articles/system-administration/84/importing-rules-and-data-using-direct-connection-database)