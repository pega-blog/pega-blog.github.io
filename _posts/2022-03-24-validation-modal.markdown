---
layout: post
title:  "Validation Messages in Modal Windows"
date:   2022-03-24 19:09:36 +0100
categories: UI
---

If you run Modal Window using Local Action on Link/Button Validation Message will be displayed on the background of the Modal Window like this:

![Wrong Modal Validation](/assets/modal-validation-bad.png)

It happens because Modal Window doesn't have own harness with section for displaying Validation Messages. Can be easily resolved by adding pyCaseErrorSection to the Modal Template or Flow Action Section:

![Right Modal Validation](/assets/modal-validation-good.png)

That problem exists since beginning for both UI-Kit and Cosmos, crazy that such simple and common use case isn't covered OOTB.