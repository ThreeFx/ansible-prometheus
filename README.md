prometheus
=========

Ansible role to set up prometheus for monitoring.

Requirements
------------

None.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
`prometheus_scrape_interval` | "15s" | Time interval in which to scrape hosts
`prometheus_scan_hosts` | [] | Hosts to scan

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
