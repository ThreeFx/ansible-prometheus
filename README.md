prometheus
=========

Ansible role to set up prometheus for monitoring.

Requirements
------------

A TLS client certificate (certificate and key concatenated) placed in
`/etc/haproxy/prometheus-server.pem`, and the corresponding CA certificate
placed in `/etc/haproxy/prometheus-ca.pem`.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
`prometheus_scrape_interval` | "15s" | Time interval in which to scrape hosts
`prometheus_scan_hosts` | [] | Hosts to scan
`prometheus_recording_rules` | [] | Recording rules, configuration in YAML according to the Prometheus documentation
`prometheus_alerting_rules` | [] | Alerting rules, configuration in YAML according to the Prometheus documentation
`prometheus_alertmanagers` | [] | Alertmanagers to use, configuration in YAML according to the `<alertmanager_config>` section in the Prometheus documentation

Dependencies
------------

* [SOSETH haproxy](https://github.com/SOSETH/haproxy) role, or a role providing an identical `conf.d` style configuration interface for haproxy.
* (optional) [SOSETH local-ca](https://github.com/SOSETH/local-ca) role, or a role providing a similar interface for automatic CA cert generation.

Example Playbook
----------------



License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
