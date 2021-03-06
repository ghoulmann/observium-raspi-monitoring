==References==

http://www.observium.org/wiki/NetSNMPd_Client_Configuration: I used this as a reference for the scripting.

http://www.memetic.org/category/raspberrypi/: Remembered this and used it to confirm and check the script.

http://www.memetic.org/wp-content/uploads/2012/07/rpi-observium.png: visual of what a monitored Raspi can look like to Observium.

==Contents==

1. This README.md document

2. ConfigureMe.sh - edit this document to define the location of the device - presumeably the Raspi, the community to include it in (I leave mine on public), and the contact information regarding the device.

3. observium_client_config.sh - the script that takes care of the snmpd install and configuration on the device (Raspi, presumeably).

==How To Get==

You can directly download from github. I believe you'll net a zip file. unzip #nameoffile.zip#. Or perhaps it's a tarball? tar xvzf #nameoffile.tar.gz.

Alternatively, use git. Do apt-get install git -y. Then git clone git://github.com/ghoulmann/#nameofrepo#.git

==How to Use==

Keep the three files in the same folder.

Edit ConfigureMe.sh. You need to know: what to call the "community" Observium should consider your Raspi a member of; a physical location for the device; who to contact and how to contact re: device administration. You can edit using leafpad, nano, vi, vim, emacs, etc.

From the command line, navigate to the location of the downloaded scripts. Then do: sudo ./observium_client_config.sh.

==Further Consideration==

Observium wants to recognize devices by hostname, not by IP. You'll want a static IP address for your Raspi NIC. Maybe this is not best practice, but once I have a fixed IP for my Raspi, I add it to /etc/hosts on the Observium server.

