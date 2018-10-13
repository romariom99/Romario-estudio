Building a simple LAMP stack and deploying Application using Ansible Playbooks.
-------------------------------------------

These playbooks require Ansible 1.2.

These playbooks are meant to be a reference and starter's guide to building
Ansible Playbooks. These playbooks were tested on CentOS 6.x so we recommend
that you use CentOS or RHEL to test these modules.

This LAMP stack can be on a single node or multiple nodes. The inventory file
'hosts' defines the nodes in which the stacks should be configured.

        [webservers]
        localhost

        [dbservers]
        bensible

Here the webserver would be configured on the local host and the dbserver on a
server called "bensible". The stack can be deployed using the following
command:

        ansible-playbook -i hosts site.yml

Once done, you can check the results by browsing to http://localhost/index.php.
You should see a simple test page and a list of databases retrieved from the
database server


* Ya esta corregido para ejecutarlo de manera facil
1) entrar a roles
2) ejecutar      ./easy.sh
3) en caso de que aparezca este error : fatal: [server01]: FAILED! => {"changed": false, "msg": "AnsibleUndefinedVariable: 'dict object' has no attribute 'ansible_default_ipv4'"} EJECUTE EL PASO 2 DE NUEVO Y SE ARREGLARÁ


* Para ejecutarlo paso a paso

---- PASOS A SEGUIR ---
1)   entrar a la carpeta roles
2)   ./makeall.sh
3)   ansible-playbook -i ../hosts ../site.yml

