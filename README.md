# Ansible Role: Galera Arbitrator

Install Galera arbitrator on Debian servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    # Name of the Galera cluster (should be the same on all nodes)
    galera_cluster_name: "my-cluster"

    # IP of cluster nodes
    galera_cluster_adress: "gcomm://10.0.0.1,10.0.0.2"

## Dependencies

None.

## Install role

    ansible-galaxy install gaeldb.galera_arbitrator

## Example Playbook

    - hosts: servers
      vars:
      	galera_cluster_name: "my-cluster"
      	galera_cluster_adress: "gcomm://10.0.0.1,10.0.0.2"
      roles:
        - role: gaeldb.galera-arbitrator
          become: yes

## License

MIT / BSD

## Author Information

This role was created in 2023 by Gael Barbier, founder of [Skalab](https://www.skalab.fr).
