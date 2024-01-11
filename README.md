# raspberrypisetup
Scripts and Instructions to Set-Up a Raspberry Pi


Below are some notes/stream-of-consciousness for the set up.
sudo mkdir /projects
sudo chown MOAB /projects
sudo chgrp MOAB /projects

In /projects:
cpan install App::cpanminus
sudo cpan install App::cpanminus
cpanm --local-lib=~/perl5 local::lib && eval $(perl -I ~/perl5/lib/perl5/ -Mlocal::lib)

cat aptpkgs_pi4setup | xargs sudo apt install -y
sudo apt update
sudo apt full-upgrade
sudo apt --fix-broken install
cat cpanmodules_pi4setup | xargs sudo cpanm

sudo service apache2 restart

https://shiroku.net/robotics/run-cgi-program-on-raspberry-pi-as-web-server/
sudo rm -r /var/www/html
sudo ln -s /projects/ET55930-6039/Website/html /var/www/html
sudo ln -s /projects/ET55930-6039/Website/cgi-bin /var/www/cgi-bin
change the APACHE_RUN_USER and GROUP to MOAB from www-data. THis is in /etc/apache2/envars
chmod -R +755 /projects/ET55930-6039



add CPATH="/usr/include/tirpc${CPATH:+:${CPATH}}"; export CPATH; to bashrc
git clone WebpageModules
git clone https://github.com/mikef5410/perl-VXI11-Client.git
follow the make instructions. last command is make install, sudo it.
git clone https://github.com/mikef5410/gpib.git



