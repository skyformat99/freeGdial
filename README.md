# eazy-connect

<h2>Connect to mobile broadband via wvdial</h2><br>
This script is supposed to help to establish a connection to your mobile carrier.
I'm not the maintainer or developer neither for wvdial nor usb-modeswitch, this script is a wrapper for both to ease up the installation.

<h3>Requirements</h3>
<h4>Hardware</h4>
USB-3G/4G-Stick
<br>
Any Hostdevice(Raspberry recommended)

<h4>Software</h4>
wvdial
<br>
usb-modeswitch

<h3>Setup</h3>
<del>Before execute the eazy-connect script be adviced that there is a also config file needed.</del>
<br>
The config file can look like this:
<br>
<pre>
<code>
[Dialer Defaults]
Init1 = ATZ
Init2 = ATQ0 V1 E1 S0=0
Modem Type = Analog Modem
ISDN = 0
Modem = /dev/ttyUSB0
Baud = 115200
<br>
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
</code>
</pre>
<br>

If you want to connect to mobile broadband on purpose you can execute this script by yourself

<code>chmod 755 eazy-connect</code>
<br>
<code>sudo ./eazy-connect</code>

But if want to connect on a regular basis you can put this script into 
<br>
/etc/cron.daily
<br>
(or 'hourly' whatever you need)
