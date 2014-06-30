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

    gdebi synaptic dconfig system-config-printer lxappearence gnome-system-monitor "gnome-disks"dconf-editor gparted ntfs-3g ntfsprogs
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
