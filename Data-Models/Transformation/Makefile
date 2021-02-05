configs/%.cfg: host_vars/%.yml hosts.yml
	ansible-playbook -i hosts.yml create-configs.yml
	touch $@

hosts.yml: network.yml
	ansible-playbook transform-data.yml
	touch $@
