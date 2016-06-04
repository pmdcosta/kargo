# Kube Spray

##Deploy a production ready kubernetes cluster
- Add the adrress of CoreOS hosts to the inventory file
- Change the master/etcd configuration to match the desired state
- Special attention to the `CHANGEME` configs

##Before Running on CoreOS
- Uncomment the variable `ansible_python_interpreter` in the file `inventory/group_vars/all.yml`
- Run `ansible-playbook -u core -e ansible_ssh_user=core  -b --become-user=root -i inventory/inventory.cfg coreos-bootstrap.yml`

##Deploy!
- `ansible-playbook -u core -e ansible_ssh_user=core  -b --become-user=root -i inventory/inventory.cfg cluster.yml` 
