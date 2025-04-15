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
## PARA PONER USUARIO GROUP

`sudo nano /etc/group`

```
sudo:x:1000:nombre de usuario

```
