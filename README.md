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
- `sudo apt install ansible`

## Ansible:
### Structure:
- `local.yml` in the ansible folder e.g. `~/andiblePC/`
- then `packages.yml` in `~/andiblePC/tasks/`

### Pulling:
-   Github > AnsiblePC repo > Code > copy Clone with HTTPS (e.g. `https://github.com/FooBar/ansiblePC.git`)
-   go to ansible directory and then `sudo ansible-pull -U https://github.com/JAnthelme/ansiblePC.git`
