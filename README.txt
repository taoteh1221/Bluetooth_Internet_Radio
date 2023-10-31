
############################################################################################################################


Bluetooth Internet Radio - Developed by Michael Kilday <mike@dragonfrugal.com>

Copyright 2022-2023 GPLv3


Fully automated setup of bluetooth and an internet radio player (PyRadio), on a headless RaspberryPi, connecting to a stereo system's bluetooth receiver (bash script, chmod +x it to run).

Project Website: https://sourceforge.net/projects/bluetooth-internet-radio/

Download Latest Version: https://github.com/taoteh1221/Bluetooth_Internet_Radio/releases

Issue Reporting (Features / Issues / Help): https://github.com/taoteh1221/Bluetooth_Internet_Radio/issues

Discord: https://discord.gg/WZVK2nm

Telegram: https://t.me/dragonfrugal

Twitter: https://twitter.com/taoteh1221

Private Contact: https://dragonfrugal.com/contact


Donations support further development... 

Bitcoin:  3Nw6cvSgnLEFmQ1V4e8RSBG23G7pDjF3hW

Ethereum:  0x644343e8D0A4cF33eee3E54fE5d5B8BFD0285EF8

Solana:  GvX4AU4V9atTBof9dT9oBnLPmPiz3mhoXBdqcxyRuQnU

Github Sponsors:  https://github.com/sponsors/taoteh1221

Patreon:   https://www.patreon.com/dragonfrugal

PayPal:    https://www.paypal.me/dragonfrugal

Venmo:     https://account.venmo.com/u/taoteh1221


#############################################################################################


To install automatically on Ubuntu / RaspberryPi OS, copy => paste => run the command below in a terminal program (using the 'Terminal' app in the system menu, or over remote SSH), while logged in AS THE USER THAT WILL RUN THE APP (user must have sudo privileges):

wget --no-cache -O bt-radio-setup.bash https://tinyurl.com/bt-radio-setup;chmod +x bt-radio-setup.bash;./bt-radio-setup.bash


AFTER installation, ~/radio is installed as a shortcut command pointing to this script, and paired bluetooth reconnects (if disconnected) when you start a new terminal session. 


A command line parameter can be passed to auto-select menu choices. Multi sub-option selecting is available too, by seperating each sub-option with a space, AND ecapsulating everything in quotes like "option1 sub-option2 sub-sub-option3".

Running normally (displays options to choose from):

~/radio
 
Auto-selecting single / multi option examples (MULTI OPTIONS #MUST# BE IN QUOTES!):
 
~/radio "1 y"
~/radio "upgrade y"
(checks for / confirms script upgrade)
 
~/radio "7 1 b3"
~/radio "play 1 b3"
(plays pyradio default playlist 3rd station in background)
 
~/radio 8
~/radio stop
(stops pyradio playback)
 
~/radio "10 XX:XX:XX:XX:XX:XX"
~/radio "connect XX:XX:XX:XX:XX:XX"
(connect bluetooth device by mac address)
 
~/radio "11 XX:XX:XX:XX:XX:XX"
~/radio "remove XX:XX:XX:XX:XX:XX"
(remove bluetooth device by mac address)
 
~/radio "12 3"
~/radio "devices paired"
(shows paired bluetooth devices)


