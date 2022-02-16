---
layout: post
title:  "MashUp scrollings and <!DOCTYPE html>"
date:   2022-02-17 19:09:36 +0100
categories: integration mashup
---

I had two identical MashUp HTMLs and one had `<!DOCTYPE html>` at the beginning (1) and another one didn't (2). They had the same CSS, same application behind. But version (1) had issues with scroll bars (it was not fullscreen) and version (2) was working just okay. 

So the lesson of the day: `<!DOCTYPE html>` affects browser rendering.

Probably error comes from the fact that MashUp isn't 100% html5 comlaint with its iframes, but also I might just suck in CSS.

[Source](https://www.htmlgoodies.com/html5/the-doctype-tag-and-its-effect-on-page-rendering/)