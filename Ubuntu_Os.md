## gnome-shell-extension-manager install

```bash
sudo apt install gnome-shell-extension-manager
```

## install gnome-tweaks

```bash
sudo apt install gnome-tweaks
sudo apt --fix-broken install
sudo chmod 777 
sudo chmod 775
```
**Extension Manager**

[https://prnt.sc/_76DAHjcnsd7](https://prnt.sc/_76DAHjcnsd7)  
[https://prnt.sc/6pyGlm_1nf0w](https://prnt.sc/6pyGlm_1nf0w)

## Virtual Box Problem

I get that there are 2 problems there :

1.  Missing linux headers
2.  Kernel modules are no signed

Are these 2 problems linked ? Any idea why I can not found the required linux-headers and how to find them ?

What I tried :

- Reinstall virtualbox using command line

```bash
 sudo apt install virtualbox
```
```bash
sudo apt install --reinstall virtualbox-dkms && sudo apt install libelf-dev
```
-   Reinstall virtualbox from [https://www.virtualbox.org/wiki/Linux_Downloads](https://www.virtualbox.org/wiki/Linux_Downloads)
-   Sign kernel modules : [How to sign a kernel module Ubuntu 18.04](https://superuser.com/questions/1438279/how-to-sign-a-kernel-module-ubuntu-18-04)

PS : I do not wish to deactivate Secure Boot

## How to Install KVM on Ubuntu
[Video](https://www.youtube.com/watch?v=_CkffsxpI5E)
```bash
Update and Upgrade Ubuntu 22.04
sudo apt update
sudo apt upgrade

Check if Virtualization is enabled
egrep -c '(vmx|svm)' /proc/cpuinfo

verify if KVM virtualization is enabled
kvm-ok

Install the cpu-checker package
sudo apt install -y cpu-checker

Install KVM on Ubuntu 22.04
sudo apt install -y qemu-kvm virt-manager libvirt-daemon-system virtinst libvirt-clients bridge-utils

Enable the virtualization daemon
sudo systemctl enable --now libvirtd
sudo systemctl start libvirtd

Check virtualization daemon is running
sudo systemctl status libvirtd

Add Your User to the KVM and Libvirt Group
sudo usermod -aG kvm $USER
sudo usermod -aG libvirt $USER

Run KVM Virtual Machines Manager
	Run **sudo virt-manager*
```
## Best Ubuntu Wallpaper
[Wallpaper](https://pasteboard.co/FT74uX4FQTSB.jpg)
![wallpaper](https://pasteboard.co/FT74uX4FQTSB.jpg)
