---
layout: post
title:  "Automatically Convert ISO date to Pega Date in Connect-REST Response"
date:   2022-02-01 19:09:36 +0100
categories: integration rest
---
1. Int- class property should have correct type (DateTime):
![DateTime Property](/assets/date-convert-property.png)


2. Fast Processing on Connect-REST rule should be off:
![Fast Processing](/assets/date-convert-fast-processing.png)

Then Pega will automatically convert ISO to GMT format:
![Date Convert Result](/assets/date-convert-result.png)
