# role-automatic-updates
This Ansible roles contains a set of tasks to configure automatic updates.


Example(s)
----------------


```
- hosts: server
  become: yes

  vars:
    # -- roles/role-automatic-updates --
    apt_update_package_list            : '1'
    apt_unattended_upgrade             : '1'
    apt_mail                           : ''
    apt_mailreport                     : 'on-change'
    apt_remove-unused-kernel-packages  : 'true'
    apt_remove-new-unused-dependencies : 'true'
    apt_remove-unused-dependencies     : 'false'
    apt_automatic-reboot               : 'true'
    apt-automatic-reboot-withusers     : 'true'
    apt_automatic-reboot-time          : '04:00'    

  roles:
    - role-automatic-updates

  tasks:
```
