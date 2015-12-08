---
layout: post
title: "Deploy Flask project on Apache2 with mod_wsgi"
description: ""
category: 
tags: [python, web]
---
{% include JB/setup %}

> this is from my old blog on wordpress. For convenience, I migrated it without much modification.

I want to put a real-world project on production and people can use it and give feedback. That’s why I want to deploy my flask project. The address for the new site is: http://115.159.82.193/(it is not available right now).

At first I thought, there isn’t much difference between the testing environment and production mode. So just need one more line:

`app.run(port=80)`

But, it appeared that it doesn’t work that way. The error message said the socket port is already taken. And I don’t know which process is using it. Thus, I seek for another solution:Apache2.

I have used Apache2 in my wordpress project. everything works fine: No tricky set up, just one more config file, few modifications on the “permission” config file, load the new config, restart the application and DONE.

Except this time we have to add one “mod_wsgi” stuff, and it drives me really mad.

Here are five more links which helps a lot during the process:

* [flask official guide on deploy with mod_wsgi](http://dormousehole.readthedocs.org/en/latest/deploying/mod_wsgi.html)
* [blog on the kind of deploy but on Windows](http://blog.csdn.net/firefox1/article/details/46438769)
* [Apache2 configuration to solve PERMISSION problem](http://www.cnblogs.com/vamei/archive/2012/12/04/2799381.html)
* [Server Internal Error Solution — check out the log](http://coolerfeng.blog.51cto.com/133059/47635/)
* [module imported error Solution — python path](http://blog.csdn.net/you_lan_hai/article/details/8592697)

And FML that Apache2 doesn’t synchronize with updates on python file!!!!