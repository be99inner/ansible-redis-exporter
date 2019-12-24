Role Name
=========

Ansible role for provision a Redis exporter for Prometheus.

Requirements
------------

Ansible version >= 2.9

Role Variables
--------------

```yaml
redis_exporter_version: 1.3.5
redis_exporter_binary_local_dir: ""
redis_exporter_web_listen_address: "0.0.0.0:9121"
redis_exporter_web_telemetry_path: "/metrics"

redis_exporter_system_group: "redis-exp"
redis_exporter_system_user: "{{ redis_exporter_system_group }}"

redis_exporter_redis_address: "redis://localhost:6379"
redis_exporter_redis_password: ""
redis_exporter_redis_namespace: "redis"

redis_exporter_custom_option: "-redis-only-metrics"
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  gather_facts: true
  roles:
      - be99inner.redis-exporter
```

License
-------

MIT

Author Information
------------------

be99inner
