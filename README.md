**Quick Start**:

Clone this repository:

```
git clone https://github.com/UMNET-perfSONAR/ansible-playbook-elastic.git
cd ansible-playbook-elastic
```

Get the required roles (ignore errors so we can run this multiple times):

```
ansible-galaxy install -r  requirements.yml --ignore-errors
```

Set up your inventory.  Connection variables can be added here as well.

```
vi inventory/hosts
```

Set up template variables by running the defaults.sh script and then editing:

```
./defaults.sh
vi inventory/group_vars/all/template/*
```

Use Ansible ping to verify connectivity to targets:

```
ansible all -m ping
```

Run the playbook:

```
ansible-playbook elastic.yml
```

----------------------
Developer Instructions
----------------------

```
ssh its-perfsonar-bastion.dsc.umich.edu
ssh 198.111.224.158
```

template for Ansible playbooks

**Quick Start**:

Set up ssh keys with Github

```
cat ~/.ssh/id_rsa.pub
```

Clone this repository:

```
git clone git@github.com:UMNET-perfSONAR/ansible-playbook-elastic.git
cd ansible-playbook-elastic
```

Clone the required roles (ignore errors so we can run this multiple times):

```
cd roles
git clone git@github.com:UMNET-perfSONAR/ansible-role-elastic.git
cd ..
```

Run Vagrant

```
vagrant up
```

Develop Role
```
vi roles/ansible-role-elastic/tasks/main.yml
vagrant provision
```

Check your work
```
vagrant ssh elastic
```

Clean up when done
```
vagrant halt
```
