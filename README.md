##### :heavy_exclamation_mark: Status :heavy_exclamation_mark:
Should work on all regions as long as the opcodes are mapped. Works on Caali's and Pinkie Pie's tera-proxy.  

##### :heavy_exclamation_mark: Installation :heavy_exclamation_mark:
1) Download Negotiator: https://github.com/Foks5000/Negotiator/archive/master.zip
2) Extract the contents of the zip file into "\tera-proxy\mods\"
3) Done! (the module will auto-update on Caali's tera-proxy when a new version is released)
  
If you enjoy my work and wish to support future development, feel free to drop me a small donation: [![Donate](https://www.paypalobjects.com/webstatic/en_US/i/buttons/PP_logo_h_100x26.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=A3KBZUCSEQ5RJ)

# Negotiator
A tera-proxy module that automatically accepts or declines Trade Broker negotiations.  
This is a fork of Pinkie Pie's original auto-negotiate.  

![Screenshot](https://i.imgur.com/uB74X4o.png)

## Usage
There are several options you can change in the config.json file (Pinkie's proxy: "\settings\Negotiator.json"):  
  
* "**enabled**" - enable/disable auto negotiate
* "**AUTO_ACCEPT_THRESHOLD**" - Automatically accepts offers for *equal or more than* the specified amount in % (0 to disable)
** Example: 99 will accept offers for 99% (or more) of the asking price
* "**AUTO_REJECT_THRESHOLD**" - Automatically declines offers for *less* than the specified amount in % (0 to disable)
** Example: 75 will decline offers for less than 75% of the asking price
* "**UNATTENDED_MANUAL_NEGOTIATE**" - Set to "true" to automatically accept negotiations after clicking the "Accept" link in chat (so be careful what you click!)
* "**DELAY_ACTIONS**" - Set this to "false" to immediately handle negotiations instead of waiting for a bit to simulate human-like behavior
* "**log**" - Set this to "true" to enable the logging of negotiations to your console
  
While in game, open a proxy chat session by typing "/proxy" or "/8" in chat and hitting the space bar.  
This serves as the script's command interface.  
The following commands are supported:  
  
* **nego [on|off]** - enable/disable auto negotiate
* **nego accept [x]** - change the minimum percentage to accept a deal, e.g. "nego accept 100" [0 to disable]
* **nego reject [x]** - change the maximum percentage to reject a deal, e.g. "nego reject 75" [0 to disable]
* **nego unattended** - enable/disable automatically accepting deals after clicking the "Accept" link in chat
* **nego delay** - switch between human-like behavior and immediate negotiation
* **nego log** - enable/disable logging to console

## Safety
Whatever you send to the proxy chat in game is intercepted client-side. The chat is NOT sent to the server.  
This module uses randomized delays to simulate human-like behavior.  

## Credits
Original by Pinkie Pie -> https://github.com/pinkipi

## Changelog
<details>

### 1.0.0
* [*] BigInt compatibility
* [+] Added auto-update support on Caali's proxy
* [+] Added optional negotiation logging to console
* [+] Added ingame commands
* [+] Added display of item names and amount
* [~] Moved settings to config file

</details>
