playbook for elastic deployment and config

**Quick Start**:


Get the required roles (note that we ignore errors so we can run this multiple times):

```
ansible-galaxy install -r  requirements.yml --ignore-errors
```

Set up your inventory.  Connection variables can be added here as well.

```
vi inventory/hosts
```

Use Ansible ping to verify connectivity to targets:

```
ansible elastic -m ping
```

Set up variables

```
```

Run the playbook:

```
ansible-playbook elastic.yml
```
