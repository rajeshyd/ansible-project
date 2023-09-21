# ansible-project

connection between master-server to node-server


configure some changes => sudo vim /etc/ansible/hosts

[dbservers]

server_1 ansible_host=3.139.101.66

[redisservers]
server_1 ansible_host=3.139.101.66

[nginxservers]
server_1 ansible_host=3.139.101.66

[all:vars]
ansible_ssh_private_key_file=/home/ubuntu/keys/ansible-key-master.pem


connection establish then:-

1:- ansible -m ping dbservers 

2:- ansible -m ping redisservers

3:- ansible -m ping nginxservers

write playbook (write in repo) and run playbook command:-

ansible-playbook install_mysql.yaml

ansible-playbook install_redis.yaml

ansible-playbook install_nginx.yaml

check all in node side:-
mysql -V
redis-server --version
systemctl status nginx


