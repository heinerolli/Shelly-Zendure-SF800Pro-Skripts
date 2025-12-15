# Shelly-Zendure-SF800Pro-Skripts
A collection of scripts to run on a shelly device to i.e. do Zero Grid feed wo cloud and / or other hardware then the Shelly and the SF800pro (plus WLAN)
The 1st script is based on the ideas of ZenUser2421C25j and what he shared in this thread in the Zendure forum:
https://forum.zendure.com/d/18610
All is based on and further details / instructions / ideas can be obtained from the Zendure SDK:
https://github.com/Zendure/zenSDK

My script for Zero Grid Feed (Zen_Script_Nulleinspeisung.txt) is using a Shelly Plus Plug S to measure Power.
Changing this to i.e. using a Shelly Pro 3EM and similar devices is easy using the Shelly script library:
[https://www.shelly.com/de/blogs/scripts-library](https://shelly-api-docs.shelly.cloud/gen2/Scripts/Tutorial)
Also, I put into the comments of the script the changes needed for 2 other devices.

Also, the script Zen_Script_BattHealth.txt grabs the information from the SF800pro in to iterations (with a puse inbetween). This is done to manuver around a limited buffer size for print commands on the Shellydevice.

To use the scripts, just use the Shelly App, go to the device you want to run them on (i.e. Shelly plus plug S) and go to the Scripts Tab and add the script. You can start/stop it from there. (Or let it start automatically when the Plus powers on).
One note and odd thing: To see debug responses (i.e. print instructions), you need to enable "Websocket debug", which is not enabled by default. And strangely, you can not enable  that through the Shelly App (at least at the time of writing this), but you need to go to the devices lokal Web page here: http://IP_Address_of_Shelly_Plug/#/settings/debug
to enable it.
Also, on the Zendure side, the SF800pro must obviously be taken out of a Zendure HEMS. Because the Shelly Plug is now the 'HEMS' and it would conflict with the Zendure cloud HEMS.
