
Debian 9 stretch .config
==========================
My Debian Testing (stretch) packages install and configurations.
«desktop MATE»
##first of all, the repositories are in the folder aptStretchTesting

...if lacking some public key:

    apt-key adv --keyserver keyserver.ubuntu.com --recv-keys PUBLicKEY
 or
 
    gpg --keyserver hkp://subkeys.pgp.net --recv-keys PUBLicKEY
 and
 
    gpg --export --armor PUBLicKEY | apt-key add -

Then run:

    aptitude update


To end:

    aptitude install deb-multimedia-keyring; aptitude update; aptitude upgrade

##aptitude install...
####Firmware

    firmware-linux-nonfree libgl1-mesa-dri xserver-xorg-video-ati
######Codecs for i386

    w32codecs libdvdcss2 xine-plugin ffmpeg gstreamer0.10-plugins-good gstreamer0.10-plugins-bad gstreamer0.10-plugins-really-bad gstreamer0.10-plugins-ugly gstreamer0.10-ffmpeg 
######Codecs for amd64

    w64codecs libdvdcss2 xine-plugin ffmpeg gstreamer0.10-plugins-good gstreamer0.10-plugins-bad gstreamer0.10-plugins-really-bad gstreamer0.10-plugins-ugly gstreamer0.10-ffmpeg
####To compress, decompress and extract files and package

    file-roller p7zip-full p7zip-rar rar unrar zip unzip unace bzip2 arj lha lzip 

####Flashplayer, javaplugin suport and Java

    flashplugin-nonfree
    icedtea-7-plugin openjdk-7-jre
####Package manager and config system

    gdebi synaptic system-config-printer gparted ntfs-3g gnome-disk-utility 

####Internet

    iceweasel qbittorrent chromium chromium-inspector chromium-l10n nmap

####Multimedia
    
######Audio

    alsa-tools a2jmidid alsaplayer-gtk alsaplayer-alsa alsaplayer-jack jackd2 jack-capture jack-midi-clock jack-mixer jack-tools jamin qjackctl patchage pulseaudio-module-jack ladish 
    moc soundconverter sound-juicer audacity smplayer hydrogen rosegarden qsynth ardour4 zynaddsubfx yoshimi lmms fluid-soundfont-gm fluid-soundfont-gs
    
#####Imagen

    camorama gimp mirage blender

####Burn cd dvd etc

    k3b

####Share files

    samba cifs-utils cifs
####Editors Ofimatica

    libreoffice vim vim-gtk gnuplot bc dc texmaker texlive-base texlive-base texlive-extra dia evince

####Other apps

    tmux tree terminator htop fish git build-essential synapse mongodb
    
##Configs

####Terminal
1» Change bash for fish, editing /etc/paswords

2» Install powerline font as usperuser:

        wget https://github.com/Lokaltog/powerline/raw/develop/font/PowerlineSymbols.otf https://github.com/Lokaltog/powerline/raw/develop/font/10-powerline-symbols.conf
        mv PowerlineSymbols.otf /usr/share/fonts/
        fc-cache -vf
        mv 10-powerline-symbols.conf /etc/fonts/conf.d/

3» Config files is cfgStretchTesting, make links

        ln -s PATHTOREPO/StretchTesting/terminalCfg/.vimrc ~/.vimrc
        # ln -s PATHTOREPO/StretchTesting/terminalCfg/.vimrc /root/.vimrc
        ln -s PATHTOREPO/StretchTesting/terminalCfg/.tmux.conf ~/.tmux.conf
        # mkdir -p /root/.config/fish/functions ~/.config/fish/functions
        ln -s PATHTOREPO/StretchTesting/terminalCfg/fish_promp.fish ~/.config/fish/functions/fish_promp.fish
        # ln -s PATHTOREPO/StretchTesting/terminalCfg/fish_promp.fish /root/.config/fish/functions/fish_promp.fish
