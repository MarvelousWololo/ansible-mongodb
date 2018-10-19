Sources:
- https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04
- https://www.youtube.com/watch?v=icR-df2Olm8&list=PLFiccIuLB0OiWh7cbryhCaGPoqjQ62NpU


Initial Server Setup with Ubuntu 18.04

Step 1 — Logging in as Root
ssh root@your_server_ip

Step 2 — Creating a New User
adduser wololo

Step 3 — Granting Administrative Privileges
usermod -aG sudo wololo

Step 4 — Setting Up a Basic Firewall
ufw allow OpenSSH
ufw enable
ufw status

Step 5 — Enabling External Access for Your Regular User
rsync --archive --chown=wololo:wololo ~/.ssh /home/wololo

Step 6 — Change project IP
search and replace for SERVER_IPV4

Step 7 — Run Ansible Playbook
ansible-playbook -K playbook.yml
