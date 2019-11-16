## Prerequisites
Install ansible on the machine, e.g. `brew install ansible` / `sudo pacman -S ansible`.

Create a SSH key, and upload it to GitHub! Otherwise, cloning this repo and dotfiles-local will not work.

Install Ansible AUR plugin. It's only required on Arch linux, but if it's not there, then ansible detects a misspelled plugin in the yml files. And then just stops.

```
$ git clone https://github.com/kewlfft/ansible-aur.git ~/.ansible/plugin/modules/aur
```
