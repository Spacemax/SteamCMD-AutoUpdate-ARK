# SteamCMD-AutoUpdate-ARK

Windows SteamCMD to automaticly update and run ARK servers.

This project reworks C0nw0nk's original concept to focus on ARK:Survival Evolved and introduce patch automation and an alert system since that game has no form of RCON access and frequent patches.

About Twitter...
Obviously since no one uses twitter in normal circumstances as soon as RCON (remote server connection) is available in ARK the code can be adjusted to instead do an admin broadcast directly on the server warning of restarts and we'll ditch dirty twitter. :)

You can find C0nw0nk's project here - https://github.com/C0nw0nk/SteamCMD-AutoUpdate-Any-Gameserver

#Features :
- Works with both 32bit and 64bit architecture.
- Installs ARK game server.
- Checks for Steam patches automatically (define interval in seconds)
- Should work with both Normal versions of Windows and Server versions.
- Suppress application hung messages to prevent server crash problems
- Checks for ARK server running and restarts if process not found
- twitter restart notifications (Dependencies detailed below)

#Requirements :
You need to have a SteamDEV API key you can obtain one from the following link | http://steamcommunity.com/dev/apikey

For the twitter updates you need to install the below:
- Twitter CLI "t" by Sferik | https://github.com/sferik/t
- Ruby 2.2 which can be downloaded from | https://www.ruby-lang.org/en/downloads/
- SteamCMD.exe which can be downloaded from | http://media.steampowered.com/installer/steamcmd.zip

#F.A.Q
I edited beyond the "Do not edit" point and now it does not work ?
I told you in the file not to touch anything beyond that point. (Just redownload the script to get a default working version.)

#Known bugs / issues :
If your game server is to crash you may have to wait for the next automatic update check as defined by the interval so the script checks if the game server is infact running or not. (Current soloution is to keep the update interval to a max of 10-15mins so if your server crashes it is not offline for long) set interval=60 (1 minute)

Minor error - If steams servers do not respond in the 'normal' way to the update check the code will still perceive this as a change from previous state, e.g a patch, and will start the update process. This can happen even if something as simple as "Connecting to steam....retrying..success" instead of "Connecting to Steam....success"


#How to use :
Download the dependencies defined above and setup in a directory structure similar to this:

\Servers\ARK

\Servers\Steamcmd\steamcmd.exe

\Servers\arkupdate.cmd

Edit the config to your liking


#Configuration : (EDIT | arkupdate.cmd file)

In order to configure the script just edit the "arkupdate.cmd" file and define your install directory and server startup parameters.

Please drop a reply if you have a question / issue i shall try to help you as much as i can.

Notes / Changes
CURL is no longer required for the auto update functions.
