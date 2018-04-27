<!-- TITLE: Ansible -->
<!-- SUBTITLE: A quick summary of Ansible -->

## Ansible

$ ansible all -m ping
$ ansible vmware-dockerswarm -m ping
$ ansible all -m command -a 'ps aux' -f1 -i inventory
	-f1 => limit processes

- Create new Role
- Create playbook/deploy-rolename.yml

$ ansible -i inventory/cluster.ini masters -m ping

Update distro over ansible
$ ansible -i inventory/cluster.ini all -m command -a 'sudo apt-get update'
$ ansible -i inventory/cluster.ini all -m command -a 'sudo apt-get upgrade -y'

Deploy nfs
- include: deploy-nfs.yml


Use privilege escalation
  become: yes
  become_user: root