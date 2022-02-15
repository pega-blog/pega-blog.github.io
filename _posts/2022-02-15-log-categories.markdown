---
layout: post
title:  "Persistent Log Level in Admin Studio"
date:   2022-02-16 19:09:36 +0100
categories: pega log administration
---
Now you can change log level per category (set of loggers) in Admin Studio. No more setting multiple loggers on multiple nodes to debug your REST connector, yay!
That setting will be persisted across restarts. It isn't affected by old school reset all loggers to default button:
![Log Categories List](/_posts/assets%20/log-categories-list.png)
You can see details of what exact loggers are included in the Dev Studio. Also you can create your own:
![Log Categories List](/_posts/assets%20/log-categories-dev-studio.png)

Available since 8.4:

https://docs.pega.com/system-administration/87/managing-log-categories