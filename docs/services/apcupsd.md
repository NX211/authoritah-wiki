# APCUPSD

## Install APCUPSD

`sudo apt-get install apcupsd`
`sudo systemctl enable apcupsd`

## Edit APCUPSD Configuration

`sudo nano /etc/apcupsd/apcupsd.conf`

UPSNAME UPS-01
UPSCABLE ether
UPSTYPE net
DEVICE opnsense.authoritah.com:3551

## Manage APCUPSD Service

`sudo systemctl start apcupsd`
`apcaccess status`
