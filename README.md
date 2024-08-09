# ansible

Workstation configuration for mondyjosh, powered by [Ansible](https://docs.ansible.com/)!

This Anisible playbook aids in the rapid setup of local systems I plan on working on.

## Getting Started

Run `./scripts/install-ansible` to ensure that the basic packages (`curl git ansible`) are installed prior to running the playbook.

## Running the playbook

Run `workstation-setup` to execute the playbook.

## Testing Playbooks

Run `./scripts/build-dockers` to build Docker images for developing/testing Ansible playbooks. This helps keep the overall setup/teardown quick so focus can be kept on the Ansible playbooks themselves (_and to keep the host system from mutating!_).

After building the Docker images, use `docker run --rm -it <tag_name> bash` to init a new ephemeral session with the image (New changes - package installs, config changes, etc. - will be reset upon exiting the Docker session, so have fun!)

## Configuration

Configuration is provided via [my dotfiles repository](https://github.com/mondyjosh/dotfiles). Chezmoi is the dotfile manager of choice, and is installed as part of this playbook's pre-tasks.

## References

- [Ansible Community Documentation](https://docs.ansible.com/) - main documentation portal for Ansible
  - [Ansible Tips and Tricks](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html)
  - [Handling OS and Distro Differences](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html#handling-os-and-distro-differences)
- [Docker Docs - Install Docker Engine](https://docs.docker.com/engine/install/) - installation docs for Docker
- [Github - The Primagen/ansible](https://github.com/ThePrimeagen/ansible) - The initial inspiration for this project, especially the Docker image testing environments
- [Github - TechDufus/dotfiles](https://github.com/TechDufus/dotfiles) - The inspiration for the project's layout and multi-distribution targeting
