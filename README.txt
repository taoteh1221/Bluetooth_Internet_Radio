
############################################################################################################################


Copyright 2022-2025 GPLv3, Bluetooth Internet Radio By Mike Kilday: Mike@DragonFrugal.com (leave this copyright / attribution intact in ALL forks / copies!)


Fully automated setup of bluetooth, internet radio player (PyRadio), local music files player (mplayer), on a headless RaspberryPi, connecting to a stereo system's bluetooth receiver (bash script, chmod +x it to run).


NOTES FOR BLACKHATS:

P̵̫̊h̴̪̑ì̶̯s̵̫̀h̸̠̆i̶̔͜n̸̞͒g̶̳̏ ̸̺͐a̴͎̓n̷̜̕d̴̻͆ ̵̙̕b̶͓͝ř̵̗u̵̼̔t̷͖͐e̴̢͑ ̵̦͊f̸̱̃ö̶̦́r̷͉͌c̴̍͜ê̸͈ ̶̬̍l̴̙̾ō̸̗g̵̫̿ḯ̴̱ṅ̸̖ ̴̘́/̴̣̅ ̸̳̈d̶̡̃ẹ̶̈c̸̲͂r̶̰̋ỹ̵̨p̶̥͂t̷͍̎i̶̮̕o̸̝̎n̸̟͑ ̴͎͑/̶̹̑ ̶͉̎O̵̦̿T̵̜̄H̶̗̓Ę̶͗R̸̪̋ ̸̦̾ȃ̷̰t̸̪̂ṯ̸̐ä̶͈́c̸̫̈k̶͈̍s̴̳̀ ̸͇̎w̸̢͝i̶͕̍l̵̦͗l̵̗̽ ̷̱̀Ň̴͍Ō̶͓T̶̙́ ̸̺̆w̶̖̓o̸̠͝r̴̪̃k̵̞͠ ̴̪̎o̴͎̽n̸͎͘ ̸̗͘m̴̖͗ẽ̸̠,̴̨̆ ̴͙̇G̵̬̿Ĭ̴͍V̶͉̇E̸̳̐ ̴̯̾U̸̺͂P̶̩̀ ̴̨͌A̵͋͜L̴̤̎R̷̖͘Ē̸͕Â̸͍D̸̨̒Ÿ̶͜!̶͖͛

GITHUB SECURITY NOTICE:

As of 2024/11/02, I am signing EVERY GITHUB CODE COMMIT with my GPG key. For verification, see the file: taoteh1221-gpg-pub-key.asc (in the app main directory)

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
~/radio "internet 1 b3"
(plays default INTERNET playlist in background, 3rd station)
~/radio "internet 1 b3vlc"
(plays default INTERNET playlist in background, 3rd station, RESET default player to: vlc)
 
~/radio "9 bsr"
~/radio "local bsr"
(rescans music files / plays LOCAL music folder ~/Music/MPlayer [RECURSIVELY] in background, shuffling)
 
~/radio 10
~/radio off
(stops audio playback)
 
~/radio "12 XX:XX:XX:XX:XX:XX"
~/radio "connect XX:XX:XX:XX:XX:XX"
(connect bluetooth device by mac address)
 
~/radio "13 XX:XX:XX:XX:XX:XX"
~/radio "remove XX:XX:XX:XX:XX:XX"
(remove bluetooth device by mac address)
 
~/radio "14 3"
~/radio "devices paired"
(shows paired bluetooth devices)


