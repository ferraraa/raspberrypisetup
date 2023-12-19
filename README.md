# raspberrypisetup
Scripts and Instructions to Set-Up a Raspberry Pi


Below are some notes/stream-of-consciousness for the set up.

cpan install App::cpanminus

cat aptpkgs_pi4setup | xargs sudo apt install -y


sudo apt update
sudo apt full-upgrade
sudo apt --fix-broken install

cat cpanmodules_pi4setup | xargs cpanm

ExtUtils::PkgConfig
Log::Log4perl
Data::Dumper
Device::SMBus
Device::I2C
RPi::PIGPIO
Device::WebIO::RaspberryPi
Device::PiGlow
UAV::Pilot::Wumpus::Server::Backend::RaspberryPiI2C
RPi::DHT11 RPi::HCSR04
App::RPi::EnvUI
RPi::DigiPot::MCP4XXXX
RPi::ADC::ADS
Device::PaPiRus
Device::BCM2835::Timer
RPi::ADC::MCP3008
RPi::BMP180
RPi::DAC::MCP4922
RPi::DHT11
RPi::DigiPot::MCP4XXXX
RPi::HCSR04
RPi::LCD
RPi::OLED::SSD1306::128_64
RPi::Pin
RPi::SPI
RPi::StepperMotor


add CPATH="/usr/include/tirpc${CPATH:+:${CPATH}}"; export CPATH; to bashrc


make /home/YOU/projects dir
make /projects/InstrumentControl dir
change owner and group of /projects to user

Inside /projects/InstrumentControl
git clone https://github.com/mikef5410/perl-VXI11-Client.git
git clone https://github.com/mikef5410/gpib.git



