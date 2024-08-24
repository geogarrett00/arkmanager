# Ark Manager
## About
Ark Manager is a simple bash script for managing multiple ark survival evolved servers on a Linux system.
## Setup
To use Ark Manager, run the script in a bash terminal. You may add the script to a location specified in your PATH for ease of use. Create a text file called arkmanager.conf in the location you plan to run the arkmanager script from. Add your server startup options to the file in the following format:

    # Startup options for a server running The Island
    "TheIsland?SessionName=TheIsland?QueryPort=37015?Port=7777?listen" -NoTransferFromFiltering -log

Any line beginning with # will be ignored. This script was designed for running clusters easily, so you may add additional server startup options on new lines to run multiple servers. Every configuration option will be ran with the 'arkmanager startup' command.
## How to use
Ark Manager currently supports the following arguments:

start - starts an ark server for every configuration line in arkmanager.conf

shutdown - shuts down any ark survival evolved servers currently running.

backup - copies ark save data to the location specified by BACKUP_DES

version - shows current program version

help - displays how to use the program.

Every argument will be executed in order from how they are passed to the script. For example, if you run 'arkmanager shutdown backup' the script will shutdown all currently running servers and then perform a backup of the save data. 
