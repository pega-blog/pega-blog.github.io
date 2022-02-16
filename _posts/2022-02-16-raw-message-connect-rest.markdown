---
layout: post
title:  "Keep Raw JSON Response from Connect-REST"
date:   2022-02-16 19:09:36 +0100
categories: integration rest
---

Sometimes you need to keep raw JSON (maybe even XML, didn't try yet) response, not just mapping to pega clipboard. Lets say errors do not fit into your Pega Data Structure. For this Param.storeRawMessage=true should be passed to Connect-REST rule.

It can be done from Data Page or Activity Rule-Connect-REST.Invoke.

I know, it isn't ideal, but there is no good extension point.

![Store Raw Message](/assets/store-raw-message.png)

Nothing about this parameter in Pega Docs unfortunatelly.