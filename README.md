## Prerequisites

Install git, vim, and ansible.

```
$ sudo apt update
$ sudo apt install git neovim ansible

or:

$ sudo pacman -S ansible
$ brew install ansible
```

Install Ansible AUR plugin. It's only required on Arch linux, but if it's not there, then ansible detects a misspelled plugin in the yml files. And then just stops.

```
$ git clone https://github.com/kewlfft/ansible-aur.git ~/.ansible/plugin/modules/aur
```

Create a SSH key, and upload it to GitHub!

```
$ ssh-keygen -o -a 100 -t ed25519 -C "flowfx@hostname"
```

Clone the repository.

```
$ mkdir ~/code
$ git clone git@github.com:FlowFX/ansible-localhost.git ~/code/ansible-localhost
```

## Cautiously run the bootstrap task

```
$ echo 'localhost ansible_connection=local' | sudo tee -a /etc/ansible/hosts

$ cd ~/code/ansible-localhost
$ ansible-playbook --tags bootstrap local.yml
```


## Go from there

$ ansible-playbook local.yml


## asdf

asdf install ruby 2.8.x
asdf install python 3.8.x
asdf install nodejs ..
asdf install yarn ..
