---
title: Computers- Trouble activating Matlab because a start job hangs   
layout: "post"
published: true
category: computers
---

Matlab needs to be reactivated every year with a new license. Our Centos7 servers were set up improperly and face many issues. I was receiving an error:

-------------------------------------------------------------------------
Error: Activation cannot proceed. You may either:
1. Set an X11 display, and restart the activation process
2. Use the silent activation feature
3. Activate using the license center
---------------------------------------------------------------------------

I had previously had this error and knew that the best resolution was to log in using the GUI and activate using the first option. All other options are long winded and I would recommend if you do not have a functional X11 display, to contact Mathworks directly. 

This machine contains an nvidia card, and so frequently the X11 display will break after updates to the system and you will need to reinstall the nvidia drivers, which can take several hours if you do not know what you are doing. 

The centos systems I manage are 90% remotely accessed machines. I discovered when I attempted to log in physically, I was greeted with:

-------------------------
A start job is running for ... 
--------------------------

and... only that. I cannot see the rest of the error and I cannot log into the system physically. I do some research and cannot find any explanations of where this error might be logged and I only have a few hours to fix the problem. 

I start by updating the system and rebooting, since that frequently fixes these issues. No luck. So I decide not to try and fix the X11 issue since I will be reinstalling the system soon anyways. 

I decide to try using an older kernel, because sometimes the newer kernels will break the nvidia drivers. Sure enough, this works and I am able to log in and update the license.

