---
layout: post
title:  "Rule Cache and OperatorID"
date:   2022-02-19 19:09:36 +0100
categories: administration cache
---

Unlike instances of most other Data- classes, the system saves Operator ID instances to the rule cache. 

As a result, until the next time that the rule cache is synchronized, one node might access a stale copy from its rules cache.

[Source](https://community.pega.com/knowledgebase/articles/application-development/86/operators)