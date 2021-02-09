# Deploy [WordPress](https://tw.wordpress.org/download/)

## Single Node Configuration

```bash=
# create a VCS vm
twccli mk vcs -ptype v.super -itype ubuntu -img "Ubuntu 20.04" -key augchao -fip -wait

# ssh to your new vcs
twccli ls vcs

# install ansible tools
sudo apt install ansible

# get playbook (installation guildlines)
git clone https://github.com/twcc/vcs_deploy

# init your TWCC-CLI
twccli config init

# enter git directory
cd vcs_deploy/cms_wordpress

# run installation
ansible-playbook playbook.yml

```

and access to your Wordpress Site, and run configuration

`http://$YOUR_VCS_IP/wp/`


1. db username: root
2. db password: *{{KEEP_EMPTY}}*

NOTE: Remember to keep your account and password for continuing login.
