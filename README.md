This is an Ansible playbook which installs Canvas LMS Open Source version on a server running Ubuntu 16.04 LTS.

Minimal hardware requirements for installation:
RAM: 8GB or more
CPU: 2000MHz dual core or better
Disk space: 20GB or more according to your project requirements

To run the script:
1) Clone repository
$ git clone https://github.com/EugeneWHZ/canvaslms-ansible-installation.git

2) Create and adjust inventory and variables files.
$ cp production.example production
$ cp staging.example staging
$ cp roles/common/vars/main.yml.example roles/common/vars/main.yml

3) Install all Canvas components at once or install web/db/redis components by choice.

To install all at once run:
$ ansible-playbook -i production master.yml

To install only webserver component run:
$ ansible-playbook -i production webservers.yml
