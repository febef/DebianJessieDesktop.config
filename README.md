DebianJessieDesktop.config
==========================
My Debian Testing (Jessie) Desktop packages install and configurations.
####First of all the repo:

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
####Instaled Packages:

aptitude install...

######Descktop 

    xorg awesome awesome-extra
######Firmware

    firmware-linux-nonfree libgl1-mesa-dri xserver-xorg-video-ati
######Codecs for i386

    w32codecs libdvdcss2 xine-plugin ffmpeg gstreamer0.10-plugins-good gstreamer0.10-plugins-bad gstreamer0.10-plugins-really-bad gstreamer0.10-plugins-ugly gstreamer0.10-ffmpeg 
######Codecs for amd64

    w64codecs libdvdcss2 xine-plugin ffmpeg gstreamer0.10-plugins-good gstreamer0.10-plugins-bad gstreamer0.10-plugins-really-bad gstreamer0.10-plugins-ugly gstreamer0.10-ffmpeg
######To compress, decompress and extract files and package

    file-roller p7zip-full p7zip-rar rar unrar zip unzip unace bzip2 arj lha lzip 
######Folder explorer

    nautilus nautilus-gtkhash nautilus-open-terminal nautilus-share 
######Flashplayer, javaplugin suport and Java

    flashplugin-nonfree
    icedtea-6-plugin openjdk-6-jre
######Package manager and config system

    gdebi synaptic dconfig system-config-printer
######Internet

    iceweasel qbittorrent chromiun chromiun-inspector chromiunm-l10n nmap
######Multimedia

    mpd mpc ncmpcpp soundconverter sound-juicer audacity
    smplayer
    gimp mirage
* Pulseaudio

    pulseaudio pavucontrol pavumeter pulseaudio-equalizer
######Burn cd dvd etc

    k3b brasero-cdrkit
######Config and system tools

    dconf-editor gparted ntfs-3g ntfsprogs
######Programin compile tools

    build-essential
######Sensors

    lm-sensors hddtemp
then run:

    sensors-detect
######Share files

    samba cifs
######Editors Ofimatica

    libreoffice vim vim-gtk gnuplot bc dc texmaker texlive-base texlive-base texlive-extra
######IRC FCB GTL chats...
    irssi 
######Network Manager

    wicd wicd-gtk wicd-curses wireless-tools
######Terminal Other apps
    tmux tree terminator puty supercat 
