# ansible-gotify-notification-automation
This is my collection of ansible automation scripts for gotify

## requirements
- ssh keys with user in wheel or sudoers group had to be exchanged (`ssh-copy-id USERNAME_IN_WHEEL_OR_SUDOERS_GROUP@YOUR-SERVER`). 
	- if you login your server via ssh, you should be able to execute sudo commands
- add your server ip to the inventory group

## usage
for example deploy the ssh-notification via gotify your server
```inventory.yml
[all:vars]
GOTIFY_URL=https://YOUR-GOTIFY-ADDRESS
GOTIFY_TOKEN=YOUR-GOTIFY-TOKEN

[ssh-notification]
user@133.333.333.337
```

you had to run `ansible-playbook -i inventory.ini main.yml -K` the -K let you prompt your become/sudo password (will be not stored).
