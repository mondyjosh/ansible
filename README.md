# ansible

Personal Ansible project to aid in the rapid setup of local systems.

## Getting Started

Run `./scripts/install-ansible` to ensure that the basic packages (`curl git ansible`) are installed prior to running the playbook. 

## Running the playbook

Run the following script to execute the `local.yml` playbook, specifying `local.ini` as the inventory, and prompting for privilege escalation password.

```bash
ansible-playbook local.yml -i localhost.ini -K
```

## Testing Playbooks

Run `./scripts/build-dockers` to build Docker images for developing/testing Ansible playbooks. This helps keep the overall setup/teardown quick so focus can be kept on the Ansible playbooks themselves (_and to keep the host system from mutating!_).

After building the Docker images, use `docker run --rm -it <tag_name> bash` to init a new ephemeral session with the image (New changes - package installs, config changes, etc. - will be reset upon exiting the Docker session, so have fun!)

## References

- [Ansible Community Documentation](https://docs.ansible.com/) - main documentation portal for Ansible
  - [Ansible Tips and Tricks](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html)
  - [Handling OS and Distro Differences](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html#handling-os-and-distro-differences)
- [Docker Docs - Install Docker Engine](https://docs.docker.com/engine/install/) - installation docs for Docker
- [Github - The Primagen/ansible](https://github.com/ThePrimeagen/ansible) - The initial inspiration for this project, especially the Docker image testing environments

