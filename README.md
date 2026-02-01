1. create droplet
Update FILE: ```0.droplet.yml```
- api_token
- oauth_token
- name: sothy
RUN: ```ansible-playbook 0.droplet.yml -i ansible/hosts```

2. Print Message
RUN: ```ansible-playbook 1.print.yml -i ansible/hosts```

3. Create user devops

Update File: ```files/authorized_keys/devops.keys``` 
  Please copy your laptop ssh key to this file
  
Update File: ```hosts```
  please update ansible_host=ip address to your server ip address that you want to create user to host file 

RUN: ```ansible-playbook 2.user.yml -i ansible/hosts```
