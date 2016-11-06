gps_test.py has been tested with a raspi model B+ and GPS unit
GlobalSat BU-353-S4

To install gpsd:

sudo apt-get install gpsd gpsd-clients python-gps

To get GPS reading working:

sudo systemctl stop gpsd.socket
sudo systemctl disable gpsd.socket

sudo gpsd /dev/ttyUSB0 -F /var/run/gpsd.sock

After this, run cgps -s to check that GPS unit has a fix
