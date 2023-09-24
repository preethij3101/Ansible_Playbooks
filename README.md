# Ansible_Playbooks

About Ansible:
  1. Ansible is popular in the DevOps Community for its simplicity,flexibility and extensive community support.
  2. It helps automate repetitive tasks, improve effeciency and ensure consistency in Infrastructure and application Configuration.
  3. Ansible is a tool written in "Python" and it uses the declarative markup language "YAML" to describe the desired state of devices and configuration.
  4. Developer is "Redhat Software"

Machanism:
  1. Push Based Configuration mechanism - Ansible
  2. Pull Based Configuration mechanism - Chef or Puppet

Methodology:
  1. Master 
  2. Slave

Ansible Components:
  1. Adhoc Command - Single Task Exceution - Single Commands - called Repostory Methods. 
  2. Playbook - Multitasking(Yaml) - Active Project - Online - Set of Adhoc Commands - called Bootstrap Method.
  3. Valut - Encryption - Security Reason.
  4. Roles - Offline Template - Ansible Galaxy - Set of Playbook.

Restriction in Ansible:
  1. Windows can't be an master
  2. Ansible shouldn't be executed as root user.

Ansible Home Directory:
  1. Inventory file - /ect/ansible/inventoryfile.txt
  2. Configuration file - /ect/ansible/ansible.cfg

Ansible Commands
  1. ansible --version -> To check ansible verison
  2. ansible all -i yourInventoryfilename -m ping -> m means modules
  3. ansible all -i yourInventoryfilename> -a "date" -> a means arugments
  4. ansible all -m ping -> Excute the command without -i
  5. ansible all -m yum -a "name=httpd state=present" -b -> Install apache -b means become root
  6. ansible all -m service -a "name=http state=started" -b -> To start apache
  7. ansible-playbook youryamlfilename --syntax-check  -> To check the syntax
  8. ansible-playbook youryamlfilename -> To run the playbook
  9. ansible-galaxy init rolename -> To use galaxy for intilaize the role.
  10. sudo yum install tree -y -> to use see the complicated file or folder will see easily
  11. ansible -vault encrypt youryamlfilename -> To encrypt the file
  12. ansible -vault view youyamfilename -> To view the encrypt file using password
  13. ansibe -vault Edit youyamfilename -> To Edit the file using password
  14. ansible -vault rekey youyamfilename -> To change the New Password
  15. ansible -playbook youyamfilename --ask-vault-pass -> To execute the encrypted playbook
  16. ansible -vault decrypt youyamfilename -> To decrypt the Password
