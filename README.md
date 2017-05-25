# freeGdial

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

<h3>Installation</h3>
<code>
git clone https://github.com/groldo/freeGdial.git \<br>
cd freeGdial \<br>
chmod 755 freegdial \<br>
./freegdial<br>
</code>

If you want to connect to your mobile carrier on a regular basis you can put this script into 
<br>
/etc/cron.daily
<br>
(or 'hourly' whatever you need)
