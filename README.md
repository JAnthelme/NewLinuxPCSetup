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

After :
- `ssh-keygen`
- Github > Settings > SSH and GPG keys > New SSH keys > copy public key (file `id_rsa.pub` contents)
