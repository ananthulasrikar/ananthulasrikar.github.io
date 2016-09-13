---
id: 464
title: Eucalyptus euca2ools.3.0.1 configuration problem solved
date: 2015-06-10T08:53:39+00:00
author: ananthulasrikar
layout: post
guid: http://ananthulasrikar.wordpress.com/?p=464
permalink: /eucalyptus-euca2ools-3-0-1-configuration-problem-solved/
publicize_facebook_url:
  - https://facebook.com/10203893649484546
  - https://facebook.com/10203893649484546
publicize_google_plus_url:
  - https://plus.google.com/118439463786613963347/posts/CUCBcGJWvEG
  - https://plus.google.com/118439463786613963347/posts/CUCBcGJWvEG
publicize_twitter_user:
  - imasrikar
  - imasrikar
publicize_twitter_url:
  - http://t.co/zruQzefiNE
  - http://t.co/zruQzefiNE
publicize_linkedin_url:
  - 'http://www.linkedin.com/updates?discuss=&scope=53729844&stype=M&topic=5870734735306665984&type=U&a=8PDs'
  - 'http://www.linkedin.com/updates?discuss=&scope=53729844&stype=M&topic=5870734735306665984&type=U&a=8PDs'
publicize_tumblr_url:
  - http://ananthulasrikar.tumblr.com.tumblr.com/post/85279592243
  - http://ananthulasrikar.tumblr.com.tumblr.com/post/85279592243
publicize_path_id:
  - 536d9bcae0ec1b04e1de1d77
  - 536d9bcae0ec1b04e1de1d77
categories:
  - Uncategorized
tags:
  - euca2ools
  - Eucalyptus
  - learning
  - problems
  - python
---
Hi all,

I would like to share a problem which I came across configuring euca2ools.3.0.1 on server.

<img class="alignright" src="http://upload.wikimedia.org/wikipedia/commons/c/c3/Eucalyptus-Logo.jpg" alt="" width="300" height="32" />

**Problem:** I was not able to connect to my eucalyptus cloud from server running RHEL 5.7 even after installation euca2ools.3.0.1 from source

[xxxxxx@xxxxx]$euca-describe-instances
  
Traceback (most recent call last):
  
File &#8220;/euca2ools\_3\_0_2/bin/euca-register&#8221;, line 5, in <module>
  
pkg\_resources.run\_script(&#8216;euca2ools==3.0.1&#8217;, &#8216;euca-register&#8217;)
  
File &#8220;build/bdist.linux-x86\_64/egg/pkg\_resources.py&#8221;, line 528, in run_script
  
File &#8220;build/bdist.linux-x86\_64/egg/pkg\_resources.py&#8221;, line 1394, in run_script
  
File &#8220;/euca2ools\_3\_0_2/lib/python2.7/site-packages/euca2ools-3.0.1-py2.7.egg/EGG-INFO/scripts/euca-register&#8221;, line 3, in <module>
  
import euca2ools.commands.euca.registerimage
  
File &#8220;/euca2ools\_3\_0\_2/lib/python2.7/site-packages/euca2ools-3.0.1-py2.7.egg/euca2ools/commands/euca/\\_\_init\_\_.py&#8221;, line 31, in <module>
  
from requestbuilder import Arg, MutuallyExclusiveArgList, AUTH, SERVICE
  
ImportError: cannot import name AUTH

**Analyzing:** I have installed following packages from tar ball/source code in a custom location using &#8211;prefix option from source

  1. python 2.7.5
  2. lxml (http://lxml.de/)
  3. requestbuilder (https://github.com/boto/requestbuilder)
  4. requests (http://www.python-requests.org/)
  5. setuptools (https://pypi.python.org/pypi/setuptools)
  6. six (http://pythonhosted.org/six/)

I have installed all the latest versions. If we can see the error its sure that we have some dependency missing. I googled it but could not find any where.

**Solution:** I contacted IRC and mailing list and found that “requests” version which I installed was 0.2.0 and it should be uninstalled and oldest version 0.1.0 was installed using pip command which is very useful in uninstalling and installing of python packages.

I need to reconfigure the installation again from source and build the ecua2ools from source. I was able to then run the euca2ools perfectly.

Thanks for irc #[eucalyptus](https://github.com/eucalyptus) and users mailing list of eucalyptus !!