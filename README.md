# multi-gadget

USB gadget service for Raspberry Pi Zero W/H and Zero 2W.   
Supports Serial, Ethernet, and Mass Storage.

# Config

In rpi

/boot/config.txt
~~~~
dtoverlay=dwc2
~~~~

/etc/modules
~~~~
dwc2
~~~~

# Install

In rpi
~~~~
sudo chmod +x multi-gadget
sudo cp multi-gadget /usr/bin/
sudo cp multi-gadget.service /usr/lib/systemd/system/
sudo systemctl daemon-reload
sudo systemctl start multi-gadget.service
sudo systemctl stop multi-gadget.service
sudo systemctl enable multi-gadget.service
~~~~

# How to use commands.
~~~~
sudo multi-gadget up
sudo multi-gadget down
sudo multi-gadget reset
~~~~
