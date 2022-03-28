
---------------------------------------------------
WSL2 Ubuntu
sguillier belen521

### actualiza ubuntu
sudo apt update && sudo apt -y upgrade


### instals un cliente grafico
sudo apt-get install -y kubuntu-desktop

---- hasta aqui llegue



### install xrdp
sudo apt-get install xrdp

### Copia de seguridad de la configuracion por defecto de xrdp
sudo cp /etc/xrdp/xrdp.ini /etc/xrdp/xrdp.ini.bak

### insercion en archivo /etc/xrdp/xrdp.ini de algunas modificaciones
sudo sed -i 's/3389/3390/g' /etc/xrdp/xrdp.ini  
sudo sed -i 's/max_bpp=32/#max_bpp=32nmax_bpp=128/g' /etc/xrdp/xrdp.ini
sudo sed -i 's/xserverbpp=24/#xserverbpp=24nxserverbpp=128/g' /etc/xrdp/xrdp.ini


### enable dbus
sudo systemctl enable dbus
sudo /etc/init.d/dbus start
sudo /etc/init.d/xrdp start
### check xrdp status
sudo /etc/init.d/xrdp status




## Paginas de Refirencia
* https://websetnet.net/es/how-to-enable-wsl2-ubuntu-gui-and-use-rdp-to-remote/
* https://tecnotraffic.net/como-habilitar-la-gui-de-ubuntu-wsl2-y-usar-rdp-en-remoto/

* https://www.lawebdelprogramador.com/foros/WSL2/1772348-Instalar-un-entorno-grafico-en-WSL2-accesible-desde-el-escritorio-remoto-en-Windows-10.html



