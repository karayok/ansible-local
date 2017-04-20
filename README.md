ansible-local
===
Ansible roles to setup local mac ( WIP )

These roles are work in progress and not tested.

## Getting started
```
$ git clone git@github.com:KarageAgeta/ansible-local.git
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew install ansible

# Install Xcode if it's not installed
$ sudo xcodebuild -license

# set your git email/name
$ vi ansible-local/group_vars/[private|business].yml
```

If you want to use multiple github accounts, edit [roles/ssh/templates/ssh_config.j2](https://github.com/KarageAgeta/ansible-local/roles/ssh/templates/ssh_config.j2
)

See : http://karage-ageta.hatenablog.com/entry/2016/10/11/191811

## Ansible playbook
```
$ ansible-playbook setup.yml -i local -l [private|business]
```

## Setup vim
Do ` :NeoBundleInstall ` after starting vim.
