# Debian-Post-Instalacion
Post-Install Debian 

## Añadir usuario a sudoers root

`sudo nano /etc/sudoers`


```
 Defaults env_reset,pwfeedback
 
```

```
nombre de usuario ALL=(ALL:ALL) ALL

```
## Para Poner Usuario Group

`sudo nano /etc/group`

```
sudo:x:1000:nombre de usuario

```
## Modificar grub

`sudo nano /etc/default/grub`

```
GRUB_TIMEOUT=0
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
The resolution used on graphical terminal
# note that you can use only modes which your graphic card supports via VBE
# you can see them in real GRUB with the command `vbeinfo'
GRUB_GFXMODE=1366x768
sudo update-grub

```
## Lista de Firmware

`nano /etc/apt/sources.list`

```
#Repos oficiales no libres
deb https://ftp.debian.org/debian/ bookworm contrib main non-free non-free-firmware
#deb-src https://ftp.debian.org/debian/ bookworm contrib main non-free non-free-firmware

#Actualizaciones
deb https://ftp.debian.org/debian/ bookworm-updates contrib main non-free non-free-firmware
#deb-src https://ftp.debian.org/debian/ bookworm-updates contrib main non-free non-free-firmware
deb https://ftp.debian.org/debian/ bookworm-proposed-updates contrib main non-free non-free-firmware
#deb-src https://ftp.debian.org/debian/ bookworm-proposed-updates contrib main non-free non-free-firmware

#Seguridad
deb https://security.debian.org/debian-security/ bookworm-security contrib main non-free non-free-firmware
#deb-src https://security.debian.org/debian-security/ bookworm-security contrib main non-free non-free-firmware

#Repositorios Backports
deb https://ftp.debian.org/debian/ bookworm-backports contrib main non-free non-free-firmware
#deb-src https://ftp.debian.org/debian/ bookworm-backports contrib main non-free non-free-firmware

```
## Instalador de paquetes basico

```

sudo apt update && sudo apt upgrade -y

```

```
sudo apt install neofetch htop -y

```

```
sudo apt install synaptic -y

```

```
sudo apt install linux-headers-$(uname -r) -y

```

```
sudo apt  install build-essential checkinstall make automake cmake autoconf git git-core dpkg wget -y

```

```
sudo apt install exfat-fuse hfsplus hfsutils ntfs-3g -y

```

```
sudo apt install gdebi gdebi-core synaptic -y

```

```
sudo apt install p7zip-full p7zip-rar rar unrar -y

```

```
sudo apt install ffmpeg libavcodec-extra gstreamer1.0-libav gstreamer1.0-plugins-ugly gstreamer1.0-plugins-bad gstreamer1.0-pulseaudio vorbis-tools -y
```

