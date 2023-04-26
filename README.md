
<p align="center"><img src="./img/rpicm4.webp" height="200" alt=" " /></p>
<h1 align="center">Raspberry Pi Compute Module 4 RPI CM4 Getting Started</h1> 
<h4 align="right">May 23</h4>

<img src="https://img.shields.io/badge/OS%20-Raspbian%20GNU%2FLinux%2010%20(buster)-yellowgreen">

<br>
# Flashing RPi CM4 with eMMC on Windows 

> :warning: **Warning:** No funciona para RPi CM4 lite (no posee el eMMC), tiene otro procedimiento.
no se necesita una SD-ext en la placa base (se usa el eMMC).

## Pasos

1. Ponemos el swich Boot en On para que arranque desde USB (debe ser un OTG cable) 
2. Conectamos al PC (en Control Panel/System/Device encontraremos un dispositivo BCM2711 Boot)
3. Correr [rpiboot.exe](https://www.mediafire.com/file/bo6gg4sxd9rkk95/Rpiboot_setup.zip/file) como administrator (esto flashea la eMMC del modulo)
4. Se abre el [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
	* Seleccionar Storage: eMMC RPi-MSD-0001 - 31.3GB
	* Choose OS/Erase FAT32 
	* Habilitamos SSH, SSID-PASSWORD, VNC
	* Escribimos OS
5. Al terminar de instalar OS cerramos RaspberryPi-Imager y quitamos cable USB
6. Pasamos el swith BOOT a off (para que inicie desde la eMMC) 
7. Ready!
8. Update & Upgrade

```
sudo apt-get update && sudo apt-get dist-upgrade -y
```
<br>

> :memo: **Note:** 
l USB Port esta desabilitado por default para ahorrar energia. para habilitarlo
se edita el config.txt y agregar:
```
sudo nano /boot/config.txt
```
add the following code at the end of the file
```
  dtoverlay=dwc2,dr_mode=host
```

## Referencias:
Documentation
https://www.raspberrypi.com/documentation/computers/compute-module.html

flashing RPi CM4
https://www.waveshare.com/wiki/Write_Image_for_Compute_Module_Boards_eMMC_version

imagen firmware
https://www.raspberrypi.com/software/operating-systems/


# CM4 Dual Eth mini Board

<p align="center">
    <img src="./img/CM4-DUAL-ETH-MINI-details-intro.jpg" height="300" alt="www.instintodigital.net">
    <img src="./img/CM4-DUAL-ETH-MINI-details-intro2.png" height="300" alt="www.instintodigital.net">
    <img src="./img/CM4-DUAL-ETH-MINI-details-size.jpg" height="270" alt="www.instintodigital.net">
</p>

wiki
https://www.waveshare.com/wiki/CM4-DUAL-ETH-MINI

<br>

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="./img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>