Name ❓
=========POC for  using Ansible Tower as a CI/CD tool for 
continuous deployment of an internal 3tier application on QA and production environments.

Requirements 👀
===========

      1) Ansible Tower Homework Lab
      2) OpenStack for Ansible
      3) Ansible Advanced
      4) https://github.com/Funkydhi/Ansible.git


Role Variables 😎
==============

      export TOWER_GUID=     export MYKEY=~/.ssh/mykey.pem
      export MYUSER=dhiren.shastry@atos.net

Dependencies 🛒
============

  1) {{tower_guid}} is the GUID (unique identifier)   2) {{osp_guid}} is the GUID for workstation machine 
  3) Tower Url: [tower1.guid.example.opentlc.com](https://tower1.guid.example.opentlc.com)
  
Example Playbook 🐧
================
 example of how to use your role :

      - hosts: localhost
        gather_facts: false 
        become: yes 
        roles:
      - config-tower

License 🔐
=======

Opensource