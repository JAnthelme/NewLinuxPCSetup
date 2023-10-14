## Dowloads
- download virtualBox [[here](https://www.virtualbox.org/wiki/Downloads)]
- download Linuxmint iso [[here](https://www.linuxmint.com/download.php)]
- download Debian iso [here]
- download Ansible iso [here]

## Installs Host
- install VBox + GuestEditions
- run and install OS iso with partition:
	- UEFI bootloader 100Mb Primary / Begining of space / EFI Syst part  
	- Linux System 50Gb Primary / Begining of space / Ext4, Mount point `/`
	- Home 50Gb Primary / Begining of space / Ext4, Mount point `/home`
	- Swap (> RAM) Primary / Begining of space / Swap Area

## Installs VM
### before VBGuestEd : 
- `sudo apt update` 
- `sudo apt upgrade`
- `sudo install build-essential linux-headers-$(uname -r)`
### After VBGuestEd:
- `sudo install git`
- `sudo apt install ansible`
- `ssh-keygen` or
- - `ssh-keygen -t ed25519 -C "foobar"`
- `git config --global user.email "mymail@yahoo.com"`
- `git config --global user.name "janthelme"`
- Github > Settings > SSH and GPG keys > New SSH keys > copy public key (file `id_rsa.pub` contents)
- Github > AnsiblePC repo > Code > copy Clone with SSH (e.g. `git@github.com:FooBar/ansiblePC.git`)
- go to home directory and then `git clone git@github.com:FooBar/ansiblePC.git`
### Quick Git test:
- go to `~\ansiblePC` folder
- e.g. modify the README.md (nano...)
- `git status` + `git add README.md` + `git commit -m "first commit"`
- `git push`

### Quick Ansible test:
in `/home/ansiblePC` copy `local.yml`:
```
- hosts: localhost
  connection: local
  become: true

  tasks:
  - name: Install htop
    apt:
      name: htop  
```
- `git status` + `git add local.yml` + `git commit -m "first commit"`
- `git push`
