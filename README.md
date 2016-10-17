pyenv-ubuntu
==============

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv-ubuntu.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv-ubuntu)

Install pyenv and python build dependencies on Ubuntu.
This role uses the motemen/ghq.

Requirements
------------

* git
* [motemen/ghq](https://github.com/motemen/ghq)

Role Variables
--------------

* pyenv_nonroot: Whether the remote_user is root or not. This variable is set automatically, and is used to execute tasks with the become option.
* pyenv_ghq_executable: The executable path of ghq command. The default is "ghq".

Dependencies
------------

* [suzuki-shunsuke.ghq-module](https://galaxy.ansible.com/suzuki-shunsuke/ghq-module/)

Example Playbook
----------------

```yaml
- hosts: servers
  vars:
    pyenv_ghq_executable: "{{ansible_env.HOME}}/.go/bin/ghq"
  roles:
  - suzuki-shunsuke.pyenv-ubuntu
```

License
-------

MIT
