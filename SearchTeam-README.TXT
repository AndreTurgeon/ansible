This ansible installation is used to create our base Amazon Machine Image (AMI).
This base AMI is used as a base to install our wars, NoSQL DB, etc.

To use:

1) source envivironment variable

source ./hacking/env-setup

2) set AWS keys

export AWS_SECRET_ACCESS_KEY="fill in..."
export AWS_ACCESS_KEY_ID="fill in..."

3) set ANSIBLE_HOSTS to point to file ansible_hosts at the base of this repository 

export ANSIBLE_HOSTS=$PWD/ansible_hosts

4) run playbook

ansible-playbook playbooks/create-base-image.yml -v --private-key=~/amazon/search-default.pem

