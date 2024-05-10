setup in windows
-----------------
1. install and enable openssh
2. verify ssh connection (ssh administrator@<ip or domain_name>)

setup in controller 
-----------------------
inventory 
---
all:
  hosts:
    my_windows_server:
      ansible_shell_type: cmd
      ansible_host: IP_OF_WINDOWS_SVR
      ansible_user: Administrator

verify inventory
-------------------
ansible-inventory --list

ping test
--------------
ansible -i inventory.yml -m win_ping my_windows_server

run the playbook
