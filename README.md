Prerequisite: 
- python3
- python3-pip: ``` apt install -y python3-pip ```
- ansible: ``` pip3 install ansible --break-system-packages```
- DigitalOcean API Token (full access)
- Check your python3 path (```which python3```) then put it in ./hosts (ansible_python_interpreter=/usr/bin/python3)

``` git clone https://github.com/SothyLorn/ansible-demo.git ```
1. create droplet
Update FILE: ```0.droplet.yml```
- api_token
- oauth_token
- name: sothy
RUN: ```
- ansible-galaxy collection install community.digitalocean
- pip3 install dopy>=0.3.2 --break-system-packages
- ansible-playbook 0.droplet.yml -i hosts```

2. Print Message
RUN: ```ansible-playbook 1.print.yml -i hosts```

3. Create user devops

Update File: ```files/authorized_keys/devops.keys``` 
  
  Please copy your laptop ssh key to this file
  
Update File: ```hosts```
  
  please update ansible_host=ip address to your server [nginx] grup ip address that you want to create user to host file 

RUN: ```ansible-playbook 3.user.yml -i hosts```
