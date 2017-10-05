ansible-local
===
Ansible roles to setup local mac ( WIP )

These roles are work in progress and not tested.

Getting started
---
```
$ git clone git@github.com:KarageAgeta/ansible-local.git
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew install ansible

# Install Xcode if it's not installed
$ sudo xcodebuild -license

# set your git email/name
$ vi ansible-local/group_vars/[private|biz|biz-linux].yml
```

If you want to use multiple github accounts, edit [roles/ssh/templates/ssh_config.j2](https://github.com/KarageAgeta/ansible-local/roles/ssh/templates/ssh_config.j2
)

See : http://karage-ageta.hatenablog.com/entry/2016/10/11/191811

Have your ./ssh/config file in local directory?
---
If you have your own ./ssh/config file, set the path to your config file in [group_vars](https://github.com/KarageAgeta/ansible-local/group_vars).

### Examples
#### Your directory
```
~/private_settings/
    |- ssh/
        |- templates/
            |- ssh_config.j2
```

#### group_vars/
```
# Set path to your private settings directory
private_settings_dir: ~/private_settings/ssh/templates/
```

Ansible playbook
---
```
$ ansible-playbook setup.yml -i local -l [private|biz|biz-linux]
```

Run specific roles (use tags)
```
$ ansible-playbook setup.yml -i local -l [private|biz|biz-linux] --tags <name of tags e.g. brew>
```

Setup vim
---
Do ` :NeoBundleInstall ` after starting vi.
