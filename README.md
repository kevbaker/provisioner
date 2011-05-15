Simple Server Provisioning
==========================

**Provisioner** is a collection of shell scripts, structured in a simple/modular way, that'll do the initial software installations and configurations on your remote server. It's very straightforward and easy to extend, when you look at the source code. The goal is to get a server (particularly for **ruby** web applications) up and running quickly after deploying a fresh server.

### Current module list:

- nginx
- rvm
- deployer
- mysql
- postgresql
- sqlite
- mongodb
- redis
- security
- imagemagick
- ffmpeg

See `lib/<module-name>/provision` for more details on each of the above modules.

*Note that this is opinionated software. It was written and tested only on Ubuntu 10.04. It might work on other versions or linux distributions. I wrote it for myself to save time (and research time) when setting up new servers.*


Usage
-----

SSH in to your remote server and run

    wget --no-check-certificate https://github.com/meskyanichi/provisioner/raw/master/provisioner

to download the provisioner file to your server.

From there, open it up and uncomment the modules you'd like to install. Once you've done that, save the file and run it.

    bash ./provisioner

That's it - if all goes well it should install the requested modules on your server.


Contributing
------------

If you find ways to improve the current code-base, or to add/improve functionality, feel free to fork it. If I find it a worthwhile addition I'll merge it in to master. Try to keep it consistent with the rest of the scripts.