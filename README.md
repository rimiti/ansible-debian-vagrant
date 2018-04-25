# ansible-debian-vagrant

## Description

This project provide a Debian Stretch (9) virtual machine to demonstrate how to execute a Ansible playbook. 
This repository can be useful if you want to try your playbook in your local machine.  


## Pre-requirements

* [Install Vagrant](http://www.vagrantup.com)
* [Install Ansible](https://www.ansible.com)

## Summary

* [Start VM](#vagrantUp)
* [Stop VM](#vagrantStop)
* [Destroy VM](#vagrantDestroy)
* [Execute Ansible playbook](#executeAnsiblePlaybook)
* [SSH VM](#sshVagrant)


## Commands

<a name="vagrantUp"/>

### Start VM

Start virtual machine.

__Arguments__

```bash
$ vagrant up    
```

---------------------------------------

### Stop VM

Stop virtual machine.

__Arguments__

```bash
$ vagrant halt    
```

---------------------------------------

<a name="vagrantDestroy"/>

### Destroy VM

Destroy virtual machine.

__Arguments__

```bash
$ vagrant destroy    
```

---------------------------------------

<a name="executeAnsiblePlaybook"/>

### Execute Ansible playbook

Execute Ansible playbook in verbose mode.

__Arguments__

```bash
$ ansible-playbook  -i environment/hosts-production --vault-password-file .production playbook.yml --private-key ~/repositories/ansible-debian-vagrant/.vagrant/machines/bart/virtualbox/private_key -vvv   
```

---------------------------------------

<a name="sshVagrant"/>

### Connect to VM from SSH

There are two ways to connect you to your VM.

__Arguments__

```bash
# From Vagrant command
$ vagrant ssh   

# From SSH command
$ ssh vagrant@127.0.0.1 -p 2222 -i ~/repositories/ansible-debian-vagrant/.vagrant/machines/bart/virtualbox/private_key
```
