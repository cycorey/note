# 添加到known_hosts中
http://stackoverflow.com/questions/30226113/ansible-ssh-prompt-known-hosts-issue

事先需编辑 /etc/ansible/hosts
```
[localhost]
127.0.0.1
192.168.126.128

[localhost:vars]
ansible_ssh_user="root"
ansible_ssh_pass="rootpassword"
```
