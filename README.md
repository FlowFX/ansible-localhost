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

Run the complete playbook.

```
$ ansible-playbook local.yml
```

Install asdf.

```
$ asdf update
$ asdf plugin add nodejs
$ asdf plugin add yarn
$ asdf plugin add ruby
```

etc. pp...


Install postgresql on Ubuntu https://computingforgeeks.com/install-postgresql-11-on-ubuntu-linux/

```
$ sudo apt install postgresql-11-postgis-2.5
$ sudo apt install redis
```


## More work foo

$ sudo apt install libcurl4-openssl-dev

required for `curb`


apt install brightnessctl


Install MS Teams

https://docs.microsoft.com/de-de/microsoftteams/get-clients#install-manually-from-the-command-line


Install fonts


https://gist.github.com/matthewjberger/7dd7e079f282f8138a9dc3b045ebefa0

https://www.nerdfonts.com/font-downloads


Re-instll vim-plug?

https://github.com/junegunn/vim-plug#unix-linux

install imagemagick!

install thefuck

install ctags !!


$ ansible-galaxy collection install ansible.posix
$ ansible-galaxy collection install community.general.
