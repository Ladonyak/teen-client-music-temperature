http://www.tinycorelinux.net/install.html
http://www.tinycorelinux.net/arch_copymode.html

passwd

openssh
http://forum.tinycorelinux.net/index.php?topic=9407.0
tce-load -wi pkg

http://www.brianlinkletter.com/persistent-configuration-changes-in-tinycore-linux/
http://wiki.tinycorelinux.net/wiki:remove_apps

https://www.centos.org/docs/5/html/yum/sn-yum-proxy-server.html

Persistence in TinyCore
TinyCore Linux runs in RAM so all changes made while the system is running will be lost after a system reboot unless the user takes action to back up the configuration changes.
The TinyCore Linux filetool.sh script provides the backup function that supports persistence. The script backs up files created in the /opt and $HOME directories. The script will also back up directories containing configuration files associated with networking software like Quagga if those directories are listed in the /opt/.filetool.lst file. Network configuration changes made using Linux commands like the ip command cannot be saved. But, we can add these commands to the /opt/bootlocal.sh shell script, which runs at startup.
Once you have created the network configurations you wish to save, by editing the /opt/bootlocal.sh script and/or saving the Quagga or Openvswitch config files, back up the configuration using the filetool.sh script as follows:
$ filetool.sh -b


When the system is running, you can restore the saved base configuration by running the command:
$ filetool.sh -r
crontab
http://forum.tinycorelinux.net/index.php?topic=12771.0

Во многих дистрибутивах есть /etc/profile.d, файлы из которой выполняются при инициализации shell'а, если переменные окружения связаны с каким-то приложением, лучше включить файл для /etc/profile.d с установкой переменных окружения в пакет приложения или создать его там вручную.


ntp
http://forum.tinycorelinux.net/index.php?topic=15783.0

timezone
http://forum.tinycorelinux.net/index.php/topic,5017.30.html


http://distro.ibiblio.org/tinycorelinux/3.x/tcz/src/



ALSA

 tce-load -wi compiletc

Надо alsa-lib    и   alsa-utils(не надо тоже) , и все.

./configure && make
 make install


/mnt/sda1/tce/mydata/alsa-utils-1.1.3$ tce-load -wi gettext python-de
v 

http://distro.ibiblio.org/tinycorelinux/3.x/tcz/src/

tce-load -iw compiletc Xorg-7.6-dev

tar jxvf alsa-driver-xxx.tar.bz2    не надо

sudo ./configure --prefix=/usr/local --enable-languages=c,c++ --disable-multilib --disable-bootstrap --with-system-zlib --libexecdir=/usr/local/lib --enable-frame-pointer --with-mpfr=/usr/local --with-gmp=/usr/local --with-cl
oog=/usr/local --with-isl=/usr/local --with-kernel=/usr --with-sequencer=yes



http://stackoverflow.com/questions/7412548/error-gnu-stubs-32-h-no-such-file-or-directory-while-compiling-nachos-source

http://gentoo.theserverside.ru/book/ar53s02.html

https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9)#.D0.A3.D1.81.D1.82.D0.B0.D0.BD.D0.BE.D0.B2.D0.BA.D0.B0

http://alsa.opensrc.org/Quick_Install



