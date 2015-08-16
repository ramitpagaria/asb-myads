# Virtual Installations / Instances #

Why have one installation if you can have many?

Most applications do not allow that. You need to find ways to start multiple processes with different configurations.

In ASB MyAds virtual installations is a feature that was implemented from the very beginning. No need to start multiple app servers or change configuration files. Just tell the installation manager how many installations you want to have (1-10) and you can switch between those installations on a single app server with a single web app deployed.

This also saves a lot of server resources (CPU, memory, disk space).

So why did we initially need multiple instances?

We have multiple users (publishers) that need separate environments to run their ads separately.