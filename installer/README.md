# Installer

Explanation of how to install our app as well as how everything connects.  

### Database Role Usage

1. Update the inventory file with your database IP, pg_name, and pg_password
2. ansible-playbook -i inventory roles/postgres/tasks/main.yml
