# Instalación Debian Buster

HP envy 7

## Basics

### Network controller: Intel Corporation Wireless 7260 (rev c3)
  
  wget -c https://wireless.wiki.kernel.org/_media/en/users/drivers/iwlwifi-7260-ucode-25.30.14.0.tgz
  
  tar -xvzf iwlwifi-7260-ucode-25.30.14.0.tgz
  
  cp iwlwifi-7260-ucode-25.30.14.0/iwlwifi-7260-14.ucode /lib/firmware/
  
  $(modprobe -r iwlwifi ; modprobe iwlwifi) || reboot

### other firmware

  firmware-linux-nonfree

### Package and compress files

  file-roller p7zip-full p7zip-rar rar unrar zip unzip unace bzip2 arj lzip 

### Java

  default-jre default-jdk
  
### system config

  gdebi synaptic system-config-printer lxappearance gnome-system-monitor gparted ntfs-3g gnome-disk-utility
  
### codecs?

  ffmpeg

### Internet

  qbittorrent nmap

#### chrome

  wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
  apt install ./google-chrome-stable_current_amd64.deb


### Share files Samba

  samba cifs-utils
  
### ofimatica

  apt install libreoffice vim vim-gtk gnuplot bc dc texmaker texlive-base texlive-base texlive-extra dia evince

#### visual code

  apt install software-properties-common apt-transport-https curl
  curl -sSL https://packages.microsoft.com/keys/microsoft.asc | apt-key add -
  add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
  apt update
  apt install code

### others 

   wireless-tools tmux tree terminator supercat htop
   
## next packages

git python python-pip ctags build-essential

