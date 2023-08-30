# ansible
Personal Ansible project to aid in the rapid setup of local systems.

## Running the playbook.
This is the bare minimum, but I eventually want to improve the execution invocation. Stashing here while I'm back-burnering learning Ansible.

```bash
ansible-playbook local.yml
```

## A better way of running the playbook

ThePrimeagen has this in his course notes. Don't remember using it per se, but I think I get why it'll be very useful.

```bash
ansible-playbook -t dotfiles local.yml --ask-become-pass --ask-vault-pass
```
