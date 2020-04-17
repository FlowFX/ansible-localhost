## Prerequisites
Install ansible on the machine, e.g. `brew install ansible` / `sudo pacman -S ansible`.

Create a SSH key, and upload it to GitHub! Otherwise, cloning this repo and dotfiles-local will not work.

Install Ansible AUR plugin. It's only required on Arch linux, but if it's not there, then ansible detects a misspelled plugin in the yml files. And then just stops.

```
$ git clone https://github.com/kewlfft/ansible-aur.git ~/.ansible/plugin/modules/aur
```

Run the playbook.
```
$ ansible-pull -U https://github.com/flowfx/ansible-localhost.git
```

## Installing on a ThinkPad X61s
1. Start Debian installer.
2. Add network cable
3. Set hostname
4. Software to install: standard system utilities

sudo apt update
sudo apt install ansible git vim
ssh-keygen -o -a 100 -t ed25519 -C "flowfx@hostname"

Add public SSH key to GitHub

mkdir ~/code
$ git clone git@github.com:FlowFX/ansible-localhost.git ~/code/ansible-localhost

echo 'localhost ansible_connection=local' | sudo tee -a /etc/ansible/hosts

$ cd ~/code/ansible-localhost
$ ansible-playbook --tags bootstrap local.yml
$ ansible-playbook local.yml

asdf install ruby 2.8.x
asdf install python 3.8.x
asdf install nodejs ..
asdf install yarn ..


Activate firefox sync
