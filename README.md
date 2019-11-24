# Ansible_roles

Creating Ansible roles for managing a Linux server.

The goal of this repository is to convert common deployment as a LAMP setup for a CMS or improve the security of the server into Ansible roles.

**Considerations:**

* The roles have been created to use in a clean installations.
* All the roles have been tested on Ubuntu 18.04.


### **Roles released**

- openvpn_server
- server_settings
- apache
- php
- reprepro


### **Description of the released roles**

**- openvpn_server:**

This role will configure the latest version of OpenVPN to acts as a secure VPN server. A brief summary of the tasks that the role does:

* It will install the OpenVPN packages along with EasyRSA to manage the certificates.

* After define a few variables it will create a Authority of Certification and then, will generate a certificate for the server and the client.

* The OpenVPN configuration will be added through a template which also contains the recommended security practices from OpenVPN.

* It will create a Client directory which contains the OpenVPN configuration for the Client side.

**- server_settings:**

This role will do some common tasks that a new server requires. Below are a list of the tasks this role does:

* It will set the hostname, timezone and locales of the server.

* The server will be update until it is up-to-date.

* A few packages will be installed to manage the system.

* A custom configuration file for 'vim' will be copied and also, it will set as a default editor.

* The prompt of the root user will be modified to be more legible.

* Some settings will be added for the history of the root user.

**- apache:**

This role will install Apache2 and configure a virtualhost for the web site. A summary of the tasks that this role can do:

* It will install Apache2 and disable the default virtualhost along with the default content directory.
* It will hide the Apache2's version.
* It can create a virtualhost for secure and non secure web sites and also, a redirect virtualhost for HTTP to HTTPs.
* The secure virtualhost has been hardening.

**- php:**

This role will install PHP, concretely, the action that the role does are:

* This module requires Apache2 package installed.
* The PHP versions available are: 5.6, 7.0, 7.1, 7.2 and 7.3 .
* It will hide the PHP version and set the timezone.

**- mariadb:**

This role will install MariaDB. Below are the actions that the role does:

* It will install MariaDB server package.
* It will set a password for database 'root' user.
* Optional the role can create a database with its user or import a SQL file.

**- wordpress:**

This role will download and configure Wordpress. The requirement for this role is:

* Apache, PHP and Mysql have to be installed and configured.

And the action that the role does are the following:

* It will download the version of Wordpress that was defined.
* A database and its user will be created.
* The Wordpress site will be created automatically.
