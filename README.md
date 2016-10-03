Golang
======

[![Build Status](https://travis-ci.org/jebovic/ansible-go.svg?branch=master)](https://travis-ci.org/jebovic/ansible-go) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-jebovic.go-blue.svg?style=flat)](https://galaxy.ansible.com/jebovic/go)

Install and configure golang dev environment

Role Variables
--------------

```
# Configurtion for download and install golang
go_tarball: "go1.7.linux-amd64.tar.gz"
go_version_target: "go version go1.7 linux/amd64"
go_download_location: "https://storage.googleapis.com/golang/{{ go_tarball }}"
go_tarball_checksum: "sha256:702ad90f705365227e902b42d91dd1a40e48ca7f67a2f4b2fd052aaa4295cd95"
go_download_path: "/tmp"
go_tarball_path: "{{ go_download_path }}/{{ go_tarball }}"
go_extract_path: "/usr/local"
go_bin_path: "/usr/local/bin/go"
```

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - { role: jebovic.go }
```

License
-------

MIT

Author Information
------------------

Jérémy Baumgarth https://github.com/jebovic
