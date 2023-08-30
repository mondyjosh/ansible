# ansible
Personal Ansible project to aid in the rapid setup of local systems.

## Running the playbook.

```bash
# Bare minimum; want to improve here
ansible-playbook local.yml

# prime has this in his course notes. Don't remember it, but I think I get why it'll be very useful.
ansible-playbook -t dotfiles local.yml --ask-become-pass --ask-vault-pass
```
