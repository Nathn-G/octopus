# Octopus

The Octopus is a Devops project the goal of this project<br>
is deploying an application onto remote machines using Ansible and its playbooks<br>
we had to initialise 5 Virtual Machine and setup all services to run 2 linked websites.

## Usage

To use this project correctly, you need to add a file named 'production'.  
In this file you need to specify 5 groups:  
- redis  
- postgresql  
- poll  
- result  
- worker  
  
for each of these groups you need to follow this structure:  
```
[redis]
redis ansible_host=ip_of_the_vm ansible_become_password=mdp_user ansible_ssh_user=user_name
```
***

Once done, in your terminal, in need to do the following commands:  
`export ANSIBLE_VAULT_PASSWORD_FILE=/tmp/.vault_pass`  
`echo verySecretPassword > /tmp/.vault_pass`  

***

Now, you can do the command to set-up all you vm.  
`ansible-playbook -i production playbook.yml`

## Credits

**Nathan Guiu**  https://github.com/Nathn-G</br>
**Mathis Lorenzo**  https://github.com/mathis-lorenzo