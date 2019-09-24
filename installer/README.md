# Installer

Explanation of how to install our demo app as well as how everything connects.  

### How to install the webapp

1. Update the inventory file with your database IP, pg_name, and pg_password
2. Set the ssh keys you want to be put on the Host in [roles/access/vars.yml](./roles/access/vars.yml)
3. `ansible-playbook -i inventory deploy_host.yml`
4. `ansible-playbook -i inventory install.yml`


To make this easier, you can make 2 Job Templates in Tower and then add them to a workflow. 
Then you can fully deploy your webapp to a cloud host in one click.  
