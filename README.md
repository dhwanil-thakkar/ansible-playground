# ansible-playground
This repository provides a simple Ubuntu docker container to create ansible-child machines.

### Requirements

- We use dockers to create these machine , so you need the **docker engine** installed on the host system.

### Basic File Structure

- docker\
  - Contains the files necessary to build the docker image
- playbooks\
  - All the plays that need to be run with ansible can go here and this directory becomes a starting point for building out plays to test.
- ansible.cfg
  - This is the configuration file for ansible , more details can be found in ansible documentaion [here](https://docs.ansible.com/).
- inventory
  - This is the inventory file for ansible, more details can be found in ansible documentation [here](https://docs.ansible.com/).