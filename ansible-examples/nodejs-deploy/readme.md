Objective : Install Nodejs V20 in the target servers(Ubuntu OS) from main server using Ansible and deploy a sample node-app in those servers.

How can we achieve? : 
1) Need a server/Virtual Machine in which ansible is installed.
  - Created a Ubuntu VM named as Ansible-Server
    (i) Run : sudo apt update
      - Refreshes the packages list to latest version available in apt repositories.
    (ii) sudo apt install ansible
      - Install ansible
2) Need atleast one target server where the node config will be done through ansible.
3) Establish a password-less authentication between Ansible Server & target servers.
  (i) Create a SSH Key in Ansible Server
      - Run :  ssh-keygen
  (ii) Copy the contents present in .ssh/id_rsa.pub and append the contents in the target server's .ssh/authorized_keys file
  (iii) Run : ssh <target-ip> in ansible server . You will be able to connect to target server without any authentication. 
        Command : exit   :- to come out of the target-server's connection 
4) Clone the GIT Repo
  - cd Learn-Devops/ansible-examples/nodejs-deploy
  - Edit the hosts file by adding the target-servers IP Addresses in [node-servers] group.
5) Run the ansible playbook : site.yml
  - Command : ansible-playbook -i hosts site.yml
    <img width="1282" height="690" alt="image" src="https://github.com/user-attachments/assets/93aba05c-157c-403c-b018-4277c0de7ccc" />
6) Verify node-version and application deployed or not.
  - node -v
  - curl http://localhost:3000
    <img width="562" height="78" alt="image" src="https://github.com/user-attachments/assets/5e5dc48f-6386-421e-bb32-b4d387cbf672" />

Hurray🎉 ! Application successfully deployed in the terget-servers.
