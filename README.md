# Ansible Role: navidrome-docker

Ansible role to create navidrome docker container.

## Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

    - hosts: container-workers
      roles:
        - role: wreiner.navidrome-docker
          become: yes

## Dependencies

This role depends on installed and configured docker container runtime.

## Role Variables

The version must be specified with:

```
navidrome_docker__navidrome_version: 0.47.5
```

The interface to which the port should be exposed must be sepcified.

```
navidrome__listen_address: "192.168.X.Y"
```

The port exposed will be 38084 on the specified interface.
