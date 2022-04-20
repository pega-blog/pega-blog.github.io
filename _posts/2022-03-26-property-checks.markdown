---
layout: post
title:  "(Property Exists) vs (Property Exists and has Value) vs (.Property !=\"\")"
date:   2022-03-26 19:09:36 +0100
categories: property
---

Every time Pega reference property though dot notation like .Property (as ClipboardProperty, without quotes) - it will be automatically created in the Clipboard. If you pass property reference to the function as ".Property" (as string, in quotes) it will not be created.
There are really few cases where you need to use @PropertyExists(".PropertyName") function, better to avoid it.
Its up to you if you want to use:

* @(Pega-RULES:Utilities).PropertyHasValue(tools, ".PropertyName") = bad readability, doesn't create a property if doesn't exist

* @(Pega-RULES:Utilities).PropertyHasValue(tools, .PropertyName) = bad readability, creates a property if doesn't exists
	
* .PropertyName != "" = good readability, creates a property if doesn't exists


You should just accept the fact that Pega creates empty properties all the time. Relying on @PropertyExists(".PropertyName") somewhere in your code will make things fail other day when somebody will deciede to reference the property. There are some cases when we don't want to have empty properties, like a data export or service response, but most of the time this is ok.

