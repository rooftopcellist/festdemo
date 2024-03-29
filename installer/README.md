# Installer

Explanation of how to install our demo app as well as how everything connects.  

### How to install the webapp

1. Update the inventory file with your database IP, pg_name, and pg_password
2. Set the ssh keys you want to be put on the Host in [roles/access/vars.yml](./roles/access/vars.yml)
3. `ansible-playbook -i inventory deploy_host.yml`
4. `ansible-playbook -i inventory install.yml`


To make this easier, you can make 2 Job Templates in Tower and then add them to a workflow. 
Then you can fully deploy your webapp to a cloud host in one click.  


### Things you will need to configure in GCE

In GCE:
* Make a service account
* Make an ssh key pair 
  - Add public ssh key to GCE to the service account as a key (Metadata section)
* Add firewall rules for default-http-server and default-https-server 
  - Allow ingress to TCP port 80 and 443 respectively.  
  
In Tower:
* Add private ssh key to Ansible Tower as a machine credential
* Add a GCE service account credentials as a credential in Tower
* In vault.yml in the repo, replace vault secrets with your own encrypted values using ansible-vault.  
  - Add the vault password to Ansible Tower
