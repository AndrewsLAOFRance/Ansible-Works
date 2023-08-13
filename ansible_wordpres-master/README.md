# Deploy WordPress via Ansible
In the launch_instance.yml file we create a new instance for our WordPress server.

To run this playbook that will create an instance we need to use the following command:
```sh
ansible-playbook --ask-vault-pass launch_instace.yml
```

To deploy WordPress we use deploy_wordpress.yml file and roles. Also we can run command to deploy WordPress with next variables for secure conection to DB
```sh
ansible-playbook deploy_wordpres.yml --extra-var "db_root_password=<your_passwd_for_root> db_user=<user_name_for_wp_db> db_user_password=<your_passwd_for_wp_user> db_name=<DB_name_for_wp>"
```