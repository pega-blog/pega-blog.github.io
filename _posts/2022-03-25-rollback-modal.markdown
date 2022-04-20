---
layout: post
title:  "Rollback for changes made in a Modal Window"
date:   2022-03-25 19:09:36 +0100
categories: UI
---

Usually Modal Window in Pega executes in the same context as the main work object. And if you made some changes in the Modal Window and then clicked cancel - they aren't gonna be rolled back as well. Because once you submitted your changes to the Clipboard (e.g refreshed section inside of the Modal Window) - they are here to stay.
In order to actually roll back changes - two approaches are available:


	
1. Execute modal window in the temporary top level page and in case of confirming them - copy top level page back to work object
	
2. Use OOTB extension pyModalPageCancelAction. Inside of that extension you can copy back all needed values from the original object stashed before:

![Rollback Modal Step](/assets/rollback-modal-1.png)

![Rollback Modal Precondition](/assets/rollback-modal-2.png)
