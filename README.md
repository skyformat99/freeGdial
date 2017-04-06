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

<h3><del>Setup</del></h3>
<del>Before executing the freeGdial script, be adviced that there is a also config file needed.</del>
<br>
<del>The config file can look like this:</del>
<br>
The wvdial configuration file is now built into the freeGdial script.
You just need to enter your PIN and APN inside of the script to establish connection.
<br>
The script writes a temporarily configuration file to /tmp/freeGdial.conf
<br>

<h3>Execution</h3>
If you want to connect to mobile broadband on purpose you can execute this script by yourself

<code>chmod 755 freeGdial</code>
<br>
<code>sudo ./freeGdial</code>

But if want to connect on a regular basis you can put this script into 
<br>
/etc/cron.daily
<br>
(or 'hourly' whatever you need)
