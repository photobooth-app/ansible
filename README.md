# Ansible Installer for the Photobooth-App and Multicam-Nodes

**[Photobooth-App](https://photobooth-app.org/)** - **[Wigglecam-Camera](https://photobooth-app.org/wigglegramcamera/)**

## What is this about?

xxx

## How to use?

Use ansible to automate the installations of the photobooth-app and the wigglecam-nodes.
You need to use ansible first, check their instructions and test it is available on your host computer.
`ansible --version`

Also, you need the host computer setup to login the nodes/photobooth-devices using passwordless ssh.

You may want to check if all hosts in the inventory are online:

```sh
ansible wigglenodes -i hosts.ini -m ping
ansible photobooth -i hosts.ini -m ping
```

```sh
ansible-playbook playbooks/install_nodes.yaml -i inventories/hosts.ini
ansible-playbook playbooks/install_photobooth.yaml -i inventories/hosts.ini
ansible-playbook playbooks/install_photobooth.yaml -i inventories/hosts.ini --limit photobooth-wigglecam
```
