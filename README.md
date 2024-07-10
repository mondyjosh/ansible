# ansible
Personal Ansible project to aid in the rapid setup of local systems.

## Running the playbook.
This is the bare minimum, but I eventually want to improve the execution invocation. Stashing here while I'm back-burnering learning Ansible.

Run the following script to execute the `local` playbook, specifying `hosts/local.ini` as the inventory, and prompting for privilege escalation password.

```bash
ansible-playbook local.yml -i hosts/local.ini -K
```

## A better way of running the playbook

ThePrimeagen has this in his course notes. Don't remember using it per se, but I think I get why it'll be very useful.

```bash
ansible-playbook -t dotfiles local.yml --ask-become-pass --ask-vault-pass
```
