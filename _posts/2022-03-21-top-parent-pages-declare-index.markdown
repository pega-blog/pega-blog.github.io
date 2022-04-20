---
layout: post
title:  "Top, Parent and other Pages on Declare Index"
date:   2022-03-21 19:09:36 +0100
categories: database
---

Lets say we have OperatorID.pyWorkGroupList(x).pyWorkGroupManagers(x). If we just run Obj-Save on pyWorkGroupManagers - then Declare Index defined on it will fail because it is using Top keyword. And Top in this context would mean OperatorID, not pyWorkGroupList.

![Declare Index Pages](/assets/pages-declare.png)

Way to go in this situation will be to copy pyWorkGroupList(x) to a temp page, run Obj-Save on it and then remove such page.

And better do not use Top/Parent/whatever context dependent pages in the Declare Index.

[Source](https://community.pega.com/knowledgebase/articles/system-administration/86/declare-index-form-completing-indexes-tab)