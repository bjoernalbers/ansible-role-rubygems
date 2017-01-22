Rubygems
========

Ansible's `gem` module fails to install Bundler on recent versions of macOS,
probably due to SIP (tested with Ansible 2.2).

This module takes care of that.
It just updates Rubygems and installs the latest Bundler.

No dependencies, no role variables.

Requirements
------------

Your ansible user must be an admin on macOS.
You also have to provide your password to make system-wide changes, i.e. by
running `ansible-playbook` with `-K` or `--ask-become-pass`.

Installation
------------

```
ansible-galaxy install bjoernalbers.rubygems
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - bjoernalbers.rubygems
```

License
-------

MIT
