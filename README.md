
Role infomation
--------------

Role install postgresql cluster vs repmgr
Support: Centos 7, Postgresql version 96,10,11,12,13

Role Variables
--------------

	# Version install
	version: 12 
	list_ip_node:
	  - 10.0.0.11
	  - 10.0.0.12
	  - 10.0.0.14
	cluster_name: pg-cluster
	repmgr_user: repmgr
	repmgr_pass: bAadcXTCe5s2Gwjh
	repmgr_db: repmgr
	master_ip: 10.0.0.11

	# Repmgr check
	PGHOST: "{{ip_node}}"
	PGUSER: "{{repmgr_user}}"
	PGPASSWORD: "{{repmgr_pass}}"
	PGPORT: 5432
	PGDATABASE: "{{repmgr_db}}"
	PGCONNECT_TIMEOUT: 10
	# Host_vars:
	is_master: False
	node_name: pg-1
	node_id: 1
	ip_node: 10.0.0.11
	# Repmgr check
	PGHOST: "{{ip_node}}"


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - {role: postgresql-repmgr, tags: postgresql-repmgr}

License
-------

