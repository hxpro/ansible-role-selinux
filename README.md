hxpro.selinux
=============

set selinux fact (boolean) true if selinux is Enforced
Install packages for SELinux enforced system


Example Playbook
----------------

    - hosts: servers
      roles:
          - role: hxpro.selinux
            selinux_booleans:
              - name: httpd_can_network_connect
                persistent: yes
                state: yes
              - name: httpd_can_network_connect_db
                persistent: yes
                state: yes
      tasks:
          - include: my_selinux_tasks.yml
            when: selinux|bool

License
-------

[WTFPL](https://raw.githubusercontent.com/hxpro/ansible-role-selinux/master/LICENSE)

Author Information
------------------

Matěj Koudelka <matej@hxpro.cz>
