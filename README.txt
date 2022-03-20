
############################################################################################################################


Bluetooth Internet Radio - Developed by Michael Kilday <mike@dragonfrugal.com> (Copyright 2022 GPLv3)


Fully automated setup of bluetooth and an internet radio player (PyRadio), on a headless RaspberryPi / DietPi, connecting to a stereo system's bluetooth receiver (bash script, chmod +x it to run).


To install automatically on Ubuntu / DietPi OS / RaspberryPi OS, copy => paste => run the command below in a terminal program (using the 'Terminal' app in the system menu, or over remote SSH), while logged in AS THE USER THAT WILL RUN THE APP (user must have sudo privileges):

wget --no-cache -O bt-radio-setup.bash https://tinyurl.com/bt-radio-setup;chmod +x bt-radio-setup.bash;./bt-radio-setup.bash


AFTER installation, ~/radio is installed as a shortcut command pointing to this script, and paired bluetooth reconnects (if disconnected) when you start a new terminal session. 


A command line parameter can be passed to auto-select menu choices. Multi sub-option selecting is available too, by seperating each sub-option with a space, AND ecapsulating everything in quotes like "option1 sub-option2 sub-sub-option3".

Running normally (diplays options to choose from):

~/radio
 
Auto-selecting single / multi sub-option examples (MULTI SUB-OPTIONS #MUST# BE IN QUOTES!):
 
~/radio "1 y"
(checks for / confirms script upgrade)
 
~/radio "6 1 b"
(plays pyradio default station in background)
 
~/radio 7
(stops pyradio background playing)
 
~/radio "9 XX:XX:XX:XX:XX:XX"
(connect bluetooth device by mac address)
 
~/radio "10 3"
(shows paired bluetooth devices)


