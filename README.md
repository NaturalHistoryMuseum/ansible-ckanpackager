# ansible-ckanpackager
Ansible playbook for ckanpackager

## Usage

Create your Ansible playbook with your own tasks, and include the role ckanpackager.  You will have to have this repository accessible within the context of playbook, e.g.

e.g. 

```
cd /my/repos/
git clone git@github.com:benscott/ansible-ckanpackager.git /my/repos/ansible-ckanpackager
cd /my/ansible/playbook
mkdir -p roles
ln -s /my/repos/ansible-ckanpackager ./roles/ckanpackager
```

Then create your playbook yaml adding the role ckanpackager.  By default, the user is required to specify credentials for the task manager user.

ckanpackager_secret
ckanpackager_password

```
---
- name: Simple Example
  hosts: localhost
  roles:
    - { role: ckanpackager, ckanpackager_secret: "daisy", ckanpackager_password: "daffodil" }
  vars:
```

## Development



