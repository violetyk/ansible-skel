# ansible-skel

This is Ansible playbooks to generate [best practices](http://docs.ansible.com/ansible/playbooks_best_practices.html) configuration.

## How to use it

```sh
$ ansible-playbook -i hosts site.yml
```

Playbooks will be created in the current directory.

```sh
$ tree -F ./playbooks
playbooks
├── dbservers.yml
├── filter_plugins/
├── group_vars/
├── host_vars/
├── hosts-development
├── hosts-production
├── hosts-staging
├── library/
├── roles/
│   └── common/
│       ├── defaults/
│       │   └── main.yml
│       ├── files/
│       ├── handlers/
│       │   └── main.yml
│       ├── meta/
│       │   └── main.yml
│       ├── tasks/
│       │   └── main.yml
│       ├── templates/
│       └── vars/
│           └── main.yml
└── webservers.yml
```


## Add a new roll

```sh
$ ansible-playbook -i hosts role.yml -e role=nginx
```


## Specify the destination directory
```sh
$ ansible-playbook -i hosts site.yml -e dest=/path/to/dest
$ ansible-playbook -i hosts site.yml -e "dest=/path/to/dest role=nginx"
```
