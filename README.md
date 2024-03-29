# MHWI Editor for Linux

## DISCLAIMER
As of 03-18-2023 I'm no longer planning to tinker with this. <br>
As of 05-14-2023 I've archived this repo. <br>

## Overview
A wrapper for the Nexus Mods MHWI save editor. <br>
Created since I run Linux, MHWI runs on Linux and I found out the save editor works on Linux with wine. <br>

Original editor can be found here, <br>
https://www.nexusmods.com/monsterhunterworld/mods/5995 <br>

I've included the zip file I found to work for this script. I tested and confirmed everything working on
Pop OS 22 (Ubuntu 22). No warranties and YMMV. <br>

## Requirements
You'll need at least the following software:
* steam
  - Proton enabled
  - Monster Hunter World
* wine
* unzip

## Functions
The script can take BASH flags to perform specific functions. These functions are as follows: <br>

### Help
Outputs script help function one-liners and exits.

### Setup
The script has a 'setup' function to help put everything in place for ease of use. <br>
This function check the following:
* If a `~/bin` folder exists
  - Offer to copy script if it exists
  - If not, tell user to run script from git repo
* If wine is installed
  - To be distro agnostic, the script will exit if Wine not installed
* If the filepath required for the project exists in `~/Documents`
* Create required folders in `~/Documents`
* unzip save editor to created folders in `~/Documents`

### Uninstall
Removes the script from `~/bin` if applicable and all created files in `~/Documents`. <br>

### Restore
Will put backed up save file in place. Potentially destructive if run on accident! <br>

### Running
To run the save editor pass the 'run' flag: <br>
`% ./saveEditorWorld run`

Script will copy the save file from installed Steam files to `~/Documents/saveEditorWorld/saveBackups`. <br>
A backup of the save file will created called `SAVEDATA1000-BK` just in case. <br>
Once the editor loads use the filepath option in the editor to open the copied save at `~/Documents/saveEditorWorld/saveBackups/SAVEDATA1000`. <br>
From there edit your save, and save when complete. <br>
On closing the save editor the edited save file will be put in place in Steam files. <br>
Launch World and enjoy! <br>
