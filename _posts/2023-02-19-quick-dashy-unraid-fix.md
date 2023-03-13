---
title: Quick Dashy Fix Test
permalink: /quick-dashy-unraid-fix/
tags: Linux HomeLab UnRaid
categories: Quick_Tips
---

## Issue with installing Dashy on UnRaid
I ran into a tiny problem while setting up Dashy on my UnRaid server. I discovered that after installing the Dashy app the conf.yml file is setup as a directory not as a file. This prevents Dashy from starting correctly.  To be fair, instructions for downloading the config are provided in the app description.
When trying to run Dashy without downloading a new config file you may see a similar error about attempting to mount a directory onto a file.

![](/assets/images/unraid_dashy_error_1.png)

Here is how the conf.yml appears in UnRaid without making any changes. As you can see the conf.yml file is actually a directory not a file.

![](/assets/images/unraid_webterminal_1.png)  



## How To Fix Our Conf.yml Issue
1. Start by opening an UnRaid web terminal. 
2. Change into /mnt/user/appdata/dashy/ directory  
``` cd /mnt/user/appdata/dashy/ ```
3. The conf.yml file is actually setup (from the install) as a directory.  We need to delete this and download a sample conf.yml file directly from the git repo.  
``` rm /mnt/user/appdata/dashy/conf.yml ```  
``` curl -O https://raw.githubusercontent.com/Lissy93/dashy/master/public/conf.yml ```
4. Restart the Dashy container.

As you can see our conf.yml file is now recongnized as a file and not a directory.  
![](/assets/images/unraid_webterminal_2.png)  

Now we can proceed with configuring Dashy! 