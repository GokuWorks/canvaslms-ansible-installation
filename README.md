This Ansible playbook installs open source Canvas LMS on a server running Ubuntu 22.04 LTS 64bit.
<br />
Minimal hardware requirements:<br />
RAM: 8GB or more<br />
CPU: 2000MHz dual core or better<br />
Disk space: 20GB or more according to your project requirements

To run the script:
1) Clone repository<br />
$ git clone https://github.com/EugeneWHZ/canvaslms-ansible-installation.git

2) Create and adjust inventory file.<br />
$ cp production.example production<br />
$ vim production<br />

3) Create a variables file.<br /> 
$ cp roles/common/vars/main.yml.example roles/common/vars/main.yml<br />
$ vim roles/common/vars/main.yml<br />

4) Install all Canvas components at once or install web/db/redis components by choice.

To install all at once run:<br />
$ ansible-playbook -i production master.yml

To install only webserver component run:<br />
$ ansible-playbook -i production webservers.yml

To install only redis-server run command:<br />
$ ansible-playbook -i production redis.yml
