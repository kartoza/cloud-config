# Kartoza Cloud Configurations

This repository contains [cloudinit](https://cloud-init.io) / 
[cloud-config](https://cloudinit.readthedocs.io/en/latest/topics/examples.html) 
profiles for servers we deploy onto the cloud.

Currently all configs are public so avoid putting sensitve data like passwords (hint use ssh 
public keys rather) into your config files.

The primary use case for this repo is with rancher and rancher-os where we want to initialise newly
joined hosts with specific networking or similar configuration.

## Repository layout

This repo has distinct folders for different use cases:

* **GISBOX**: These are cloud configs for hosts being joined to our GISBOX offering. GISBOX is a remotely managed,
subscription based PostgreSQL replica of our PostGIS master database which you can deploy on your own premises. 
This allows to you to benefit from a local, fast and continually updated and improved PostGIS instance which you 
can connect to from your own services. We maintain one configuration file per box and the file name should match
the GISBOX-id of the deployed server.
* **GENERAL**: This is are generic cloud configuration files for remote managed servers. It will ensure that kartoza
employee ssh keys are installed onto any newly deployed remote servers.


## History

* Initial repostory creation: 6 August 2018

## Credits

* Tim Sutton (tim __at__ kartoza.com) github user: timlinux
