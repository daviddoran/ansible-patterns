# Ansible Patterns

This is a collection of useful patterns for [ansible](http://ansible.cc/), a server management and orchestration tool.

You can use ansible to do things such as installing packages, restarting services, uploading files and enabling apache sites.

## Getting started

First, [install ansible](http://ansible.cc/docs/gettingstarted.html) and create your
ansible hosts (inventory) file with the details of the servers you're going to manage with ansible.

For convenience, here is the format of the hosts file:

    SERVERNAME ansible_ssh_user=USERNAME ansible_ssh_host=IPADDRESS ansible_connection=ssh

where

- `SERVERNAME` is the nickname of the server,
- `USERNAME` is the SSH username, and
- `IPADDRESS` is the IP address of the machine.

For example, your hosts file might look like this:

    web1 ansible_ssh_user=daviddoran ansible_ssh_host=192.0.2.1 ansible_connection=ssh

## Using a pattern

`cd` into the directory of the pattern:

    cd developer-keys

Configure the example-playbook file (follow the instructions in the folder's README file).

Run the example playbook on your hosts file:

    ansible-playbook -i hosts example-playbook.yml

where `hosts` is the path to your hosts file.

## Requirements

- ansible on your development computer
- the ansible prerequisites on your servers (usually just Python 2.6)
- a [hosts file](http://ansible.cc/docs/patterns.html) (containing the hostnames of your server)

## License

This project is released under the MIT License - see the LICENSE file for details.
