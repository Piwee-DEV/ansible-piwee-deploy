# ansible-piwee-deploy

Deploy the whole PIWEE infrastructure.

### Deploy a master node

Example:

ansible inventory file :

    [piwee_server]
    91.121.223.193 assetsfolder=/Users/alexandrenguyen/web/provisioning/piwee-assets mysql_root_password=xxxxx is_slave=true master_ip=xxxxx master_ssh_password=xxxxxx slave_ssh_password=xxxxx
    
Run it :

    ansible-playbook playbook.yml -i ansible-inventory --user=root
  
### Deploy a slave node

  Set the is_slave to true and set a master_ip, master_ssh_password, and slave_ssh_password.
