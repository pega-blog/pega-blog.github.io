---
layout: post
title:  "Understand When Pega Page is Truly Loaded"
date:   2022-02-01 19:09:36 +0100
categories: ui javascript
---
Sometimes JS ready event executes when Pega is still working hard to display the page.

To not rely on it you can check for document-statetracker element in DOM, but also there is a JS property pega.ui.statetracking where you can see what exactly is loading right now. 

![Log Categories List](/assets/statetracking.png)

There is no public docs on it from Pega side on it.