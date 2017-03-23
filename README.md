# eazy-connect

Connect to mobile broadband via wvdial
This script is supposed to help to establish a connection to your mobile carrier.
I'm not the maintainer or developer neither for wvdial nor usb-modeswitch, this script is a wrapper for both to ease up the installation.

Requirements
Hardware
USB-3G/4G-Stick
Any Hostdevice(Raspberry recommended)

Software
wvdial
usb-modeswitch

Setup
Before execute the eazy-connect script be adviced that there is a also config file needed.

The config file can look like this:

[Dialer Defaults]
Init1 = ATZ
Init2 = ATQ0 V1 E1 S0=0
Modem Type = Analog Modem
ISDN = 0
Modem = /dev/ttyUSB0
Baud = 115200

[Dialer pin]
Init3 = AT+CPIN='your sim-pin'
[Dialer pinstatus]
Init4 = AT+CPIN?
[Dialer umts]
Carrier Check = no
Init5 = AT+CGDCONT=1,"IP","your mobile carrier's apn"
Stupid Mode = 1
Phone = *99#
Username = any
Password = any
Dial Attemps = 2

If you want to connect to mobile broadband on purpose you can execute this script by yourself

chmod 755 eazy-connect
sudo ./eazy-connect

But if want to connect on a regular basis you can put this script into /etc/cron.daily(or hourly whatever you need)
