---
layout: post
title:  "Use pzExternalName Property Qualifier"
date:   2022-02-25 19:09:36 +0100
categories: integration
---
    
Not everybody is aware of "pzExternalName" property qualifier. You can use it when you need to map property to/from JSON, but Pega property doesn't match JSON name. E.g it has a dash inside or starts with a number. You can use it from 7.1.8.

Fast Mapping has to be disabled in the Connect-REST rule.

![pzExternalName Property Qualifier](/assets/pzExternalName.png)


[Source](https://docs.pega.com/data-management-and-integration/87/json-mapping-special-characters)