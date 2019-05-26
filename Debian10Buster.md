# Instalación Debian Buster

HP envy 7

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

### Share files Samba

  samba cifs-utils
  
### ofimatica

  libreoffice vim vim-gtk gnuplot bc dc texmaker texlive-base texlive-base texlive-extra dia evince

#others 

   wireless-tools tmux tree terminator supercat htop
