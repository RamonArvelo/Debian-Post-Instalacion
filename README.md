# Debian-Post-Instalacion
Post-Install Debian 12

## Añadir usuario a sudoers root

`sudo nano /etc/sudoers`

`sudo vim /etc/sudoers`


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
sudo apt update-grub -y

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


## Actualiza tu sistema

```

sudo apt update && sudo apt upgrade -y

```

## Instalador de paquetes neofetch htop

```
sudo apt install neofetch htop -y

```

## Synaptic es un gestor de paquetes, de programas visual

```
sudo apt install synaptic -y

```

## linux-headers, son archivos que contienen la definición de funciones del kernel de Linux


```
sudo apt install linux-headers-$(uname -r) -y

```
## Instalador de paquetes basico copilaccion

```
sudo apt  install build-essential checkinstall make automake cmake autoconf git git-core dpkg wget -y

```

## exFAT-fuse es un controlador que permite usar el sistema de archivos exFAT en sistemas que no son compatibles con el kernel

```
sudo apt install exfat-fuse hfsplus hfsutils ntfs-3g -y

```

## Gdebi es una herramienta que permite instalar paquetes .deb en Linux

```
sudo apt install gdebi gdebi-core  -y

```

## 7-zip es un compresor de archivos gratuito, multiplataforma y de código abierto

```
sudo apt install p7zip-full p7zip-rar rar unrar -y

```
## códec es un programa o dispositivo que codifica o decodifica señales digitales de audio o video

```
sudo apt install ffmpeg libavcodec-extra gstreamer1.0-libav gstreamer1.0-plugins-ugly gstreamer1.0-plugins-bad gstreamer1.0-pulseaudio vorbis-tools -y
```

## Font es un tipo de letra, y puede referirse a un elemento HTML o a un archivo electrónico

```
sudo apt-get install fonts-freefont-ttf fonts-freefont-otf -y

```
```
sudo apt -y install fonts-inconsolata fonts-droid-fallback xfonts-terminus fonts-droid-fallback ttf-bitstream-vera fonts-cantarell fonts-liberation fonts-oflb-asana-math fonts-mathjax

```
```
sudo apt-get install ttf-mscorefonts-installer

```

```
sudo apt-get install fonts-ubuntu

```

```
sudo apt-get install fonts-powerline -y

```

## Linux, los backports son paquetes de software que se adaptan de versiones posteriores para usarse en versiones antiguas

```
sudo apt install -t bookworm-backports linux-image-amd64

```
## UFW (Uncomplicated Firewall) es un programa que administra el firewall en sistemas Linux

```
sudo apt install gufw -y

```
## riseup-vpn es un proyecto que ofrece herramientas de comunicación segura y anónima, incluyendo un servicio VPN

```
sudo apt install riseup-vpn -y

```

## VLC Media Player es un reproductor multimedia gratuito, de código abierto y multiplataforma

```
sudo apt install vlc -y

```
## Kvantum es un personalizador de estilos para Qt6 que permite dar una apariencia uniforme a las aplicaciones Qt y GTK

```
sudo apt install qt5-style-kvantum qt5-style-kvantum-themes -y

```

## fastfetch es una herramienta de línea de comandos que muestra información del sistema operativo en la terminal

```
sudo add-apt-repository ppa:zhangsongcui3371/fastfetch

```

```
sudo apt update

```

```
sudo apt install fastfetch -y

```

## Liquorix es un kernel de Linux que está optimizado para mejorar el rendimiento de sistemas interactivos, como aplicaciones multimedia y juegos

```
curl -s 'https://liquorix.net/install-liquorix.sh'| sudo bash

```


## FIN











