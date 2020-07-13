Neo4j Community Server role for RedHat/CentOS 8

## Role Variables

```yaml
# OPTIONAL defaults to latest stable version if not defined
neo4j_version: 4.10

# OPTIONAL defaults to accepting connections from localhost only
# define it like in the example below, to expose neo4j on all interfaces
neo4j_listen_address: 0.0.0.0
```

## Usage

Use latest version of the role in your ansible-galaxy requirements.yml file

```yaml
- src: mhitza.neo4j
  version: 1.0.0
```

Example playbook:

```yaml
- hosts: all
  become: true
  tasks:
    - include_role: name=mhitza.neo4j
      vars:
        neo4j_listen_address: 0.0.0.0
```
