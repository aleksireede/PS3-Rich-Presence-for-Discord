# PS3-Rich-Presence-for-Discord
Discord Rich Presence script for PS3 consoles on HFW&HEN or CFW.

Display what you are playing on your PS3 via Discord's game activity.

# Installation
pip3 install networkscan bs4 pypresence --break-system-packages

## Display Example
<table>
	<tr>
		<th>XMB</th>
		<th> <img src="https://github.com/aleksireede/PS3-Rich-Presence-for-Discord/blob/main/img/xmb.png?raw=true"> </th>
	</tr>
	<tr>
		<th>PS3</th>
		<th> <img src="https://github.com/aleksireede/PS3-Rich-Presence-for-Discord/blob/main/img/ps3.png?raw=true"> </th>
	</tr>
	<tr>
		<th>Retro</th>
		<th> <img src="https://github.com/aleksireede/PS3-Rich-Presence-for-Discord/blob/main/img/retro.png?raw=true"> </th>
	</tr>
</table>

## Download
* [version 1.9.4 .exe](https://github.com/aleksireede/PS3-Rich-Presence-for-Discord/releases/download/1.0.0/PS3RPD.exe)  
or
* [version 1.9.4 .py](https://github.com/aleksireede/PS3-Rich-Presence-for-Discord/releases/download/1.0.0/PS3RPD.py)

### Note
The executable file will very likely be flagged as a virus on your computer due to pyinstaller being used to compile it.
As far as I know, there is nothing I can do to fix this.

## Limitations
* __A PC must be used to display presence, there is no way to install and use this script solely on the PS3__
* The script relies on webmanMOD, and a major change to it will break this script, please message me about updated versions of webman so that i can test the script with them
* PSX and PS2 game name depends on the name of the file
* PSX and PS2 game detection will **not** work on PSN .pkg versions because webman cannot show those games as mounted/playing.
* PS2 ISO game detection can be inconsistent, varying on degree of consistency by the value of "Refresh time."
* Using Windows 7 or lower is not possible :/

## Usage

### Requirements
* PS3 with either HFW&HEN, or CFW installed
* PS3 with [webmanMOD](https://github.com/aldostools/webMAN-MOD/releases) installed 
* PS3 and PC on the same network/internet connection
* Discord installed and open on the PC running the script
* A Python 3.9 interpreter installed on the PC if you do not wish to use the executable file

### Installing as a Windows service (optional)
Download [NSSM](https://nssm.cc/release/nssm-2.24.zip) and run `nssm install <service name ie. ps3rpd>` from command-line to install PS3RPD as a Windows service.
WARNING: PS3RPD.exe must be in a location that won't change ie. C:\ps3rpd\PS3RPD.exe

## Additional Information

### External config file
PS3RPD makes use of an external config file to persistently store a few variables, on creation, the default values will be:
* Your PS3's IP address 	(where the script will find your PS3 on the network)
* My Discord developer application's ID 		(where the script will send presence data to)
* A refresh time of 35 seconds 					(how often to get new data (minimum value of 15 seconds)
* To show the PS3's temperature
* To use a shared cover for PS2&PSX games
* To display the time elapsed


### Using your own images
If you would like to have complete control over what images are used per game, you must create your own Discord developer application over at https://discord.com/developers/applications.

Once created, copy the "APPLICATION ID" from the developer portal and paste it into the external config file "PS3RPDconfig.txt", replacing the value of "ID".

You will now be able to add your own art assets in the developer portal under "Rich Presence > Art Assets". Note that the name of the art assets uploaded must be the same as whatever is output from the script when that specific game is open.  
It will be a lowercase titleID, e.g. blxxx12345

## [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/N4N87V7K5) [![pypresence](https://img.shields.io/badge/using-pypresence-00bb88.svg?style=for-the-badge&logo=discord&logoWidth=20)](https://github.com/qwertyquerty/pypresence)
