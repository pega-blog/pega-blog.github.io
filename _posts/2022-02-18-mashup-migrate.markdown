---
layout: post
title:  "Move MashUp Between Environments"
date:   2022-02-18 19:09:36 +0100
categories: integration mashup
---

Now Pega MashUp is a channel. So you cannot just use generated MashUp code on all environments, you need to move the channel as well. Otherwise you will have a security error exception.

For this you need to associate instance of DATA-CHANNEL-MASHUP with your app RuleSet.

[Source](https://docs.pega.com/keeping-current-pega/85/migrating-existing-mashups)