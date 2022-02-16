---
layout: post
title:  "Extension Points and Rule Resolution for Navigation Rules"
date:   2022-02-20 19:09:36 +0100
categories: rules
---

Something strange happenes with rule resolution for Navigation rules.

We have:	
* Work Object of class OZOTM0-Platform-Work-CaseType
	
* Base navigation rule pyWorkActionsReview in class Work- with extension reference to TestDBA navigation rule
![Navigation Base](/assets/navigation-base.png)
* Placeholder TestDBA in Work-
![Navigation Placeholder](/assets/navigation-placeholder.png)

* Actual extension TestDBA in OZOTM0-Platform-Work-CaseType
![Navigation Placeholder](/assets/navigation-extension.png)

We get:

In runtime it always takes one from Work-, regardless the fact that current context is OZOTM0-Platform-Work-CaseType:

![Navigation Runtime](/assets/navigation-runtime.png)

This is quite common practice to have such extension points with Data Transforms, Activities, Sections, but it doesn't work with Navigation? If Save As pyWorkActionsReview rule to OZOTM0-Platform-Work-CaseType - then the reference works fine.

Couldn't find any info on this behaviour on Pega Docs
