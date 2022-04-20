---
layout: post
title:  "Check if Data Instance Exists"
date:   2022-03-22 19:09:36 +0100
categories: database
---

There are two ways to check if data instance exists:
- Function "pxDoesHandleExist". But in order to use it - you need to know pzInsKey beforehand. Not something you have before creation of the instance. It is possible to generate it manually, but let's try to avoid it
- When rule and/or function pxDoesObjectExist. Works exactly how you expect it to. Just run it in the context of the item you need to check

[Source](https://docs.pega.com/reference/87/obj-open-method)