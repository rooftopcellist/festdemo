# Getting Started with Ansible Tower - App demo

App deployment demo for Ansiblefest 2019

> Note: This is purely to demonstate how you could deploy a web app with Ansible and is not quite production-ready.  

In this _basic_ web app deployment, we will use the following roles to stand up a web app:

**Provision Host JT**
* create host
* access


**Install JT**
* repos - install yum repos and update them
* dependencies - installs all system-level dependencies
* postgres - installs and configures the postgresql 10 db
* nginx - installs and configures nginx webserver


See the [installer](./installer/README.md) docs for how to run the installer.  

