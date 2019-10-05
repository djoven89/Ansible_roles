# Ansible_roles

Creating Ansible roles for managing a Linux server.

The goal of this repository is to convert common deployment as a LAMP setup for a CMS or improve the security of the server into Ansible roles.

### **Roles released**

- openvpn_server
- server_settings


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

