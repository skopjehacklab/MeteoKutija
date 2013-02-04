Description of the operation of the router, source code and config for the openwrt build


Serial port
===========

The OpenWrt init has the serial port opened by default, waiting for activity
and running a shell on it. We need to disable that in /etc/inittab

Also, the default flags on any serial port (even USB to serial) on the OpenWrt
are different than on desktop kernels. Programs will need to take care of
setting sane flags (ICRNL gave us a big headache before we figured out what was happening).
