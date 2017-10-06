# ansible-nxrm3
Repository to Install Nexus Repository OSS 3.6.0-02

## Prerequisites and Preparation
**Supported OSes:** CentOS and RHEL

**Supported OS Versions:** 6+

**Note** This playbook runs a yum update prior to installation to ensure compatability.


## General Steps
This playbook installs httpd as a reverse proxy to allow for port 80 to be used, and install Nexus OSS v3 on the correct machine.

## Settings
Edit the hosts file, or add a [nexus] group to your config.
Ensure that group_vars/all.yml has been edited to reflect your enviornment.

### Variables
There is only a single variable to change for this playbook, **your_domain**. This is used in the logging, and httpd files.

### Command to install Nexus Repository OSS v3

    ansible-playbook -i hosts nexus.yml
