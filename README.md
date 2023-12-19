# raspberrypisetup
Scripts and Instructions to Set-Up a Raspberry Pi


Below are some notes/stream-of-consciousness for the set up.

cpan install App::cpanminus

cat aptpkgs_pi4setup | xargs sudo apt install -y


sudo apt update
sudo apt full-upgrade
sudo apt --fix-broken install

cat cpanmodules_pi4setup | xargs cpanm

add CPATH="/usr/include/tirpc${CPATH:+:${CPATH}}"; export CPATH; to bashrc


make /home/YOU/projects dir
make /projects/InstrumentControl dir
change owner and group of /projects to user

Inside /projects/InstrumentControl
git clone https://github.com/mikef5410/perl-VXI11-Client.git
git clone https://github.com/mikef5410/gpib.git



