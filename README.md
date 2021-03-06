docker-ansible
=========

this ansible code includes 2 roles. first role checks the host for docker installation. if docker is installed installation process stops. if we want to force installing or upgrade we use -e force=true in the shell.in the second role checks mentioned items and then install docker-compose. 
for example if we want check and install docker :
```bash
ansible-playbook -vv -i inventory.ini play.yml
```
if we want to force upgrade and install :
```bash
ansible-playbook -vv -i inventory.ini play.yml -e force=true
```


Requirements
------------
```txt
ansible==5.5.0
ansible-core==2.12.3
cffi==1.15.0
cryptography==36.0.2
Jinja2==3.0.3
MarkupSafe==2.1.1
packaging==21.3
pkg_resources==0.0.0
pycparser==2.21
pyparsing==3.0.7
PyYAML==6.0
resolvelib==0.5.4
```


Role Variables
--------------

variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role:
```yaml
docker_required_packages:
  - apt-transport-https
  - ca-certificates
  - curl
  - gnupg
  - lsb-release

docker_new_packages:
  - docker-ce
  - docker-ce-cli
  - containerd.io
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
   - hosts: all
     become: yes
     roles: 
       - docker-ansible      
```

License
-------

Apache License 2.0



Author Information
------------------

this code is written by peyman safiri.



[@dwsclass](https://github.com/dwsclass)dws-ops-003-ansible
 
[@dwsclass](https://github.com/dwsclass)dws-ops-003-ansible

