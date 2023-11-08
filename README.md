NOTE: Playbook is being upgraded from Ubuntu 16.04 LTS to Ubuntu 22.04 LTS. 
Work in progress, so bugs and errors are possible.
<br />
This is an Ansible playbook which installs open source Canvas LMS on a server running Ubuntu 22.04 LTS 64bit.
<br />
Minimal hardware requirements for installation:<br />
RAM: 8GB or more<br />
CPU: 2000MHz dual core or better<br />
Disk space: 20GB or more according to your project requirements

To run the script:
1) Clone repository<br />
$ git clone https://github.com/EugeneWHZ/canvaslms-ansible-installation.git

2) Create and adjust inventory and variables files.<br />
$ cp production.example production<br />
$ cp staging.example staging<br />
$ cp roles/common/vars/main.yml.example roles/common/vars/main.yml<br />

3) Install all Canvas components at once or install web/db/redis components by choice.

To install all at once run:<br />
$ ansible-playbook -i production master.yml

To install only webserver component run:<br />
$ ansible-playbook -i production webservers.yml
