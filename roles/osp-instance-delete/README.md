Role Name
=========

This role does the below,
       
       1) Fetch Instance Info
       2) Delete instances

Requirements
------------

  1) Ansible Tower Homework Lab
  2) OpenStack for Ansible
  3) Ansible Advanced
  4) https://github.com/Funkydhi/Ansible.git

Role Variables
--------------

    export TOWER_GUID=ccd4
    export MYKEY=~/.ssh/mykey.pem
    export MYUSER=dhiren.shastry@atos.net

Dependencies
------------

  1) {{tower_guid}} is the GUID (unique identifier)   2) {{osp_guid}} is the GUID for workstation machine 
  

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

        - name: Delete instances
          os_server:
            cloud: ospcloud
            name: "{{ item.name }}"
            state: absent
          loop: "{{result.ansible_facts.openstack_servers}}"


License
-------

Opensource