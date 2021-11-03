<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/dwm.png" alt="DWM">
  </a>
  </p>
</div>

<!-- ABOUT THE PROJECT -->
### About The Project

This is my build of of dwm.
dwm is an extremely fast, small, and dynamic window manager for X.



### Requirements

In order to build dwm you need the Xlib header files.


### Configuration

The configuration of dwm is done by creating a custom config.h and (re)ompiling the source code.

Installation
------------
Edit config.mk to match your local setup (dwm is installed into the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm