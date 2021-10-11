## Prerequisites

Install git, vim, and ansible.

```
$ sudo apt update
$ sudo apt install git neovim ansible

or:

$ sudo pacman -S ansible
$ brew install ansible
```

Create a SSH key, and upload it to GitHub!

```
$ ssh-keygen -o -a 100 -t ed25519 -C "flowfx@hostname"
```

Clone the repository.

```
$ mkdir ~/src/flowfx
$ git clone git@github.com:FlowFX/ansible-localhost.git ~/src/flowfx/ansible-localhost
```

## Cautiously run the bootstrap task

```
$ echo 'localhost ansible_connection=local' | sudo tee -a /etc/ansible/hosts

$ cd ~/src/flowfx/ansible-localhost
$ ansible-playbook --tags bootstrap local.yml
```

## Go from there

Run the complete playbook.

```
$ ansible-playbook local.yml
```

etc. pp...

Install postgresql on Ubuntu https://computingforgeeks.com/install-postgresql-11-on-ubuntu-linux/

```
$ sudo apt install postgresql-11-postgis-2.5
$ sudo apt install redis
```

Install asdf plugins

$ asdf install

Install hex for elixir

$ mix local.hex

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
$ brew install ranger file chardet

For flowfx.de / Nikola
apt install yui-compressor

# Misc

$ apt install inotify-tools

For flowfx.de / nikola
apt installl yui-compressor

$ texlive / install --cask mactex








github cli
https://github.com/cli/cli/blob/trunk/docs/install_linux.md
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh


Configure autocomplete!
https://cli.github.com/manual/gh_completion



## hURL
curl -LO https://github.com/Orange-OpenSource/hurl/releases/download/1.3.1/hurl_1.3.1_amd64.deb
sudo dpkg -i hurl_1.3.1_amd64.deb
