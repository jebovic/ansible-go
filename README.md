Golang
======

[![Build Status](https://travis-ci.org/jebovic/ansible-go.svg?branch=master)](https://travis-ci.org/jebovic/ansible-go) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-jebovic.go-blue.svg?style=flat)](https://galaxy.ansible.com/jebovic/go)

Install and configure golang dev environment

This role is a part of my [OPS project](https://github.com/jebovic/ops), follow this link to see it in action. OPS provides a lot of stuff, like a vagrant file for development VMs, playbooks for roles orchestration, inventory files, examples for roles configuration, ansible configuration file, and many more.

Compatibility
-------------

Tested and approved on :

* Debian jessie (8+)
* Ubuntu Trusty (14.04 LTS)
* Ubuntu Xenial (16.04 LTS)

Role Variables
--------------

```yaml
# Configurtion for download and install golang
go_tarball: "go1.7.linux-amd64.tar.gz"
go_version_target: "go version go1.7 linux/amd64"
go_download_location: "https://storage.googleapis.com/golang/{{ go_tarball }}"
go_tarball_checksum: "sha256:702ad90f705365227e902b42d91dd1a40e48ca7f67a2f4b2fd052aaa4295cd95"
go_download_path: "/tmp"
go_tarball_path: "{{ go_download_path }}/{{ go_tarball }}"
go_extract_path: "/usr/local"
go_bin_path: "/usr/local/bin/go"
go_path: "/srv/golang"
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: jebovic.go }
```

Example : config
----------------

```yaml
# Define custom $GO_PATH and install go binary in custom directory
go_bin_path: "/srv/bin/go"
go_path: /srv/data/go
```

Tags
----

* go_config : only update GOPATH

License
-------

MIT

Author Information
------------------

Jérémy Baumgarth https://github.com/jebovic
