# CUPS

## Install

Install CUPS
`sudo apt-get install cups`
Start CUPS service
`sudo systemctl start cups`
Enable CUPS service
`sudo systemctl enable cups`

CUPS configuration file
`/etc/cups/cupsd.conf`

Edit CUPS configuration file

`Browsing Off`

Comment out `Listen localhost:631`

`Port 631`

Add user to lpadmin group
`sudo adduser username lpadmin`

Install HP printer drivers
`sudo apt-get install hplip`

Search printer drivers on openprinting.org

Install Avahi-daemon for Bonjour/IPP printing
`sudo apt-get install a avahi-daemon`

Start Avahi-daemon
`sudo systemctl start avahi-daemon`

Enable Avahi-daemon
`sudo systemctl enable avahi-daemon`

Daemon listens on port 5353
