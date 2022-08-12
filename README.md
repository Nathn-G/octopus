# Octopus

***

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
