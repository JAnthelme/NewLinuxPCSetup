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
Before VBGuestEd : 
- `sudo apt update` 
- `sudo apt upgrade`
- `sudo install build-essential linux-headers-$(uname -r)`
- `sudo install git`

After :
- `ssh-keygen`
- Github > Settings > SSH and GPG keys > New SSH keys > copy public key (file `id_rsa.pub` contents)
- Github > AnsiblePC repo > Code > copy Clone with SSH (e.g. `git@github.com:FooBar/ansiblePC.git`)
- go to home directory and then `git clone git@github.com:FooBar/ansiblePC.git`
