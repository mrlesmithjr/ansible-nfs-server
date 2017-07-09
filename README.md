<!-- START doctoc generated TOC please keep comment here to allow auto update -->

<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

**Table of Contents**  _generated with [DocToc](https://github.com/thlorenz/doctoc)_

-   [ansible-nfs-server](#ansible-nfs-server)
    -   [Requirements](#requirements)
    -   [Role Variables](#role-variables)
    -   [Dependencies](#dependencies)
    -   [Example Playbook](#example-playbook)
    -   [License](#license)
    -   [Author Information](#author-information)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# ansible-nfs-server

An [Ansible](https://www.ansible.com) role to install/configure an NFS Server

## Requirements

None

## Role Variables

```yaml
---
# defaults file for ansible-nfs-server

# Define export info
## Define any exports to be available to clients
##
### hostname
#### define by hostname, fqdn, ip address, ip subnet or * for all
####
### options
#### define any options or leave commented out
####
### mode
#### define the folder permissions to set which also apply to client mounts
nfs_server_exports: []
  # - export:
  #   access:
  #     # - hostname: '172.16.24.0/24'
  #     #   options:
  #     #     - 'ro'
  #     #     - 'sync'
  #     #     - 'no_subtree_check'
  #     #     - 'no_root_squash'
  #     - hostname: '192.168.250.0/24'
  #       options:
  #         - 'rw'
  #         - 'sync'
  #         - 'no_subtree_check'
  #         - 'no_root_squash'
  #   mode: "u=rwx,g=rx,o=rx"
  #   path: '/opt/nfs/test1'
  # - export:
  #   access:
  #     - hostname: '*'
  #       options:
  #         - 'rw'
  #         - 'sync'
  #         - 'no_subtree_check'
  #         - 'no_root_squash'
  #   mode: "u=rwx,g=rwx,o=rwx"
  #   path: '/opt/nfs/test2'
```

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: nfs_servers
  vars:
  roles:
    - role: ansible-nfs-server
  tasks:
```

## License

MIT

## Author Information

Larry Smith Jr.

-   [@mrlesmithjr](https://www.twitter.com/mrlesmithjr)
-   [EverythingShouldBeVirtual](http://www.everythingshouldbevirtual.com)
-   mrlesmithjr [at] gmail.com
