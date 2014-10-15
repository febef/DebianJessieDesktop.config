DebianJessieDesktop.config
==========================
My Debian Testing (Jessie) Desktop packages install and configurations.
##First of all the repo:

    deb http://ftp.us.debian.org/debian/ testing main non-free contrib
    deb-src http://ftp.us.debian.org/debian/ testing main non-free contrib
      
    deb http://security.debian.org/ testing/updates main contrib non-free
    deb-src http://security.debian.org/ testing/updates main contrib non-free
      
    # jessie-updates, previously known as 'volatile'
    deb http://ftp.us.debian.org/debian/ jessie-updates main contrib non-free
    deb-src http://ftp.us.debian.org/debian/ jessie-updates main contrib non-free
      
    # jessie-backports, previously on backports.debian.org
    deb http://ftp.us.debian.org/debian/ jessie-backports main contrib non-free
    deb-src http://ftp.us.debian.org/debian/ jessie-backports main contrib non-free
      
    # Repositorios multimedia
    deb http://www.deb-multimedia.org/ testing main non-free
    deb-src http://www.deb-multimedia.org/ testing main non-free

or stable""

    # Repositorios Básicos y oficiales estable
    deb http://ftp.fr.debian.org/debian/ wheezy main contrib non-free 
    deb-src http://ftp.fr.debian.org/debian/ wheezy main contrib non-free 
    
    # Repositorio  actualizaciones de seguridad estable
    deb http://security.debian.org/ wheezy/updates main contrib non-free 
    deb-src http://security.debian.org/ wheezy/updates main contrib non-free 
    
    # Wheezy-updates, previos conocidos como "Volatile" 
    deb http://ftp.debian.org/debian wheezy-updates main contrib non-free
    deb-src http://ftp.debian.org/debian wheezy-updates main contrib non-free
    
    # Repositorios Backports 
    deb http://mirrors.kernel.org/debian wheezy-backports main contrib non-free 
    deb-src http://mirrors.kernel.org/debian wheezy-backports main contrib non-free
    
    # Multimedia estable-wheezy  
    deb http://www.deb-multimedia.org wheezy main non-free 
    deb-src http://www.deb-multimedia.org/ wheezy main non-free 
    
    # Repositorio Spotify nativo 
    deb http://repository.spotify.com stable non-free 
    
    # Repositorio de Nuvola Player 
    deb http://ppa.fenryxo.cz/nuvola-player/ wheezy main 
    deb-src http://ppa.fenryxo.cz/nuvola-player/ wheezy main 
        
    # Repositorio VirtualBox Debian Wheezy 
    deb http://download.virtualbox.org/virtualbox/debian wheezy contrib non-free
    
    # Repositorio de Google Chrome 
    deb http://dl.google.com/linux/deb/ stable main 
    
    # Repositorio de Escritorio "Mate" (gnome 2) 
    deb http://packages.mate-desktop.org/repo/debian wheezy main

stable keys?:


    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 94558F59
    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 98AB5139
    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 706C220A 


    sudo gpg --keyserver hkp://subkeys.pgp.net --recv-keys A040830F7FAC5991
    sudo gpg --export --armor A040830F7FAC5991 | sudo apt-key add -
    sudo apt-get update


Then run:

    aptitude update; aptitude upgrade
    aptitude install deb-multimedia-keyring; aptitude update
##Packages and...

aptitude install...

####Descktop 

    xorg awesome awesome-extra
####Firmware

    firmware-linux-nonfree libgl1-mesa-dri xserver-xorg-video-ati
######Codecs for i386

    w32codecs libdvdcss2 xine-plugin ffmpeg gstreamer0.10-plugins-good gstreamer0.10-plugins-bad gstreamer0.10-plugins-really-bad gstreamer0.10-plugins-ugly gstreamer0.10-ffmpeg 
######Codecs for amd64

    w64codecs libdvdcss2 xine-plugin ffmpeg gstreamer0.10-plugins-good gstreamer0.10-plugins-bad gstreamer0.10-plugins-really-bad gstreamer0.10-plugins-ugly gstreamer0.10-ffmpeg
####To compress, decompress and extract files and package

    file-roller p7zip-full p7zip-rar rar unrar zip unzip unace bzip2 arj lha lzip 
####Folder explorer

    nautilus nautilus-gtkhash nautilus-open-terminal nautilus-share 
####Flashplayer, javaplugin suport and Java

    flashplugin-nonfree
    icedtea-6-plugin openjdk-6-jre
####Package manager and config system

    gdebi synaptic xnetcardconfig   system-config-printer lxappearance gnome-system-monitor  gparted ntfs-3g ntfsprogs gnome-disk-utility 

####Internet

    iceweasel qbittorrent chromiun chromiun-inspector chromiunm-l10n nmap
    
######IRC FCB GTL chats...

    irssi bitlbee
######Skype

Run this only amd64

    dpkg --add-architecture i386
    aptitude update

Then run:

    wget -O skype-install.deb http://www.skype.com/go/getskype-linux-deb
    dpkg -i skype-install.deb
    apt-get -f install

####Multimedia

    mpd mpc ncmpcpp soundconverter sound-juicer audacity alsa-tools
    smplayer cheese camorama
    gimp mirage inkscape
######Pulseaudio

    pulseaudio libao4 paprefs libpulse-mainloop-glib0 
    pulseaudio-module-jack pavucontrol pulseaudio-module-x11 
    gstreamer0.10-pulseaudio pulseaudio-utils libasound2-plugins 
    paman pulseaudio-module-gconf libgconfmm-2.6-1c2 libpulse-browse0 
    pavumeter libglademm-2.4-1c2a pulseaudio-esound-compat libpulse0 
    libpulse-dev pulseaudio pulseaudio-esound-compat 
    pulseaudio-module-gconf  pulseaudio-module-x11  
    pulseaudio-utils lib32asound2 lib32asound2-plugins  ia32-libs-gtk pulseaudio-equalizer

Then run:

    usermod  -a -G pulse,pulse-access $(whoami)

####Burn cd dvd etc

    k3b brasero-cdrkit
####Programin compile tools

    build-essential
####Sensors

    lm-sensors hddtemp
Then run:

    sensors-detect
####Share files

    samba cifs-utils cifs
####Editors Ofimatica

    libreoffice vim vim-gtk gnuplot bc dc texmaker texlive-base texlive-base texlive-extra dia evince

####Network Manager

    wicd wicd-gtk wicd-curses wireless-tools
####Terminal Other apps

    tmux tree terminator putty supercat 
