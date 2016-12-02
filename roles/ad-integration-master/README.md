ad integation for RHEL
========

Ansible role to configure RHEL  to use Microsoft Active Directory for authentication. 

Tested on RedHat Linux 6.6

Requirements
------------

keytab file has been provided by AD server. This method will not use net join to add Linux into AD. Keytab needs to be provided before using this playbook. 



Role Variables
--------------

The role uses the following variables, which you should override in your playbook:
* `ad_workgroup` - The short domain name uppercase.
* `ad_realm` - The domain name uppercase.
* `ad_pdc` - The primary domain controller.
* `ad_pdc_ip` - The primary domain controller ip (for dns).
* `ad_sdc` - The secondary domain controller.
* `ad_sdc_ip` - The secondary domain controller ip (for dns).


Example Playbook
-------------------------

    - hosts: servers
      vars_files:
        - group_vars/ad.yml

      roles:
         - ad-integration

Where group_vars/ad.yml is defaults/main.yml modifed to your needs.


License
-------

HPE

Author Information
------------------
ysong
