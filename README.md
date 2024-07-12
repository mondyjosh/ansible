# ansible

Personal Ansible project to aid in the rapid setup of local systems.

## Running the playbook.

This is the bare minimum, but I eventually want to improve the execution invocation. Stashing here while I'm back-burnering learning Ansible.

Run the following script to execute the `local.yml` playbook, specifying `local.ini` as the inventory, and prompting for privilege escalation password.

```bash
ansible-playbook local.yml -i local.ini -K
```

## Testing Playbooks

Run `./build-dockers` to build Docker images for developing/testing Ansible playbooks. This helps keep the overall setup/teardown quick so focus can be kept on the Ansible playbooks themselves (and to keep the host system from mutating!).

After building the Docker images, use `docker run --rm -it <tag_name> bash` to init a new ephemeral session with the image (New changes - package installs, config changes, etc. - will be reset upon exiting the Docker session, so have fun!)

Refer to [Docker Engine install](https://docs.docker.com/engine/install/) for any Docker troubleshooting.
