# Hosting a Minecraft Server.
## Setup.

###### Prerequisites:
> If modded, Forge/Fabric Installer
> 8-16GB of RAM

Below instructions will be written for Forge but can be used for Fabric aswell.

Forge can be obtained from http://files.minecraftforge.net/
The left hand panel will have the versions of forge that you need. 
Click on the required version and download the **Installer** in the Recommended list.

###### Host Folder and Structure:

Have a location for the minecraft server reserved. This can be desktop or anywhere else, as long as SYSTEM has write permissions there.

A folder structure is recommended. You may need to host multiple versions of minecraft or even different modpacks.

The recommended folder structure is,

Minecraft Servers
- 1.12 (Server Version)
  - RLCraft

###### Installation and first run:

After you've set up your folder structure, run the forge installer.
Click on the **"Install Server"** option and then set the location to the reserved folder. Following the above example, this will be the folder "RLCRraft".
Click install.

Once installation is complete, navigate to the folder, and run the forge .jar file. In this case the file name would be *"forge-1.12.2-14.23.5.2854.jar"*.
A CMD Terminal will open and then close. 
You'll find a new file named *"eula.txt"*, open this file with notepad and edit the last line from **false** to **true**, save and close.

###### Final server start setup:

Right click in the folder, click new and then click Text Document. 
Enable *File Name Extensions* which can be found in the View tab of the File Explorer.
Rename the file to serverStart (or something similar).
Open this file and paste the following,

> java -Xmx 1G -jar minecraft_server.jar --nogui 

*-Xmx* stands for Maximum usable memory. You should set this value depending on your requirements as well as your Memory limits.
For vanilla servers, 2-4 GB of memory should be comfortable. Most modpacks can do with 4-8GB of memory.

*minecraft_server.jar* refers to the jar file that should be run. In this case, *forge-1.12.2-14.23.5.2854.jar*. It is safer to copy the name from the server Jar file directly and paste it in here.

**Note** *If you're runninig Vanilla minecraft, there will be no forge, but a minecraft server jar file.*

**Note 2** *Server Arguments like the one given above are very important. You should consult someone on the best argument string to use for your server.*

After this, save the file and rename it to **serverStart.bat** or something, the *.bat* part is mandatory.

You can now host minecraft, but I suggest you keep reading.

## Configuration.
###### sever.properties.

After running the servevr jar for the first time, it will generate a file named *server.properties*. There's some important stuff to change in there. Get comfortable with editing this file.

> online-mode=true

This has to be changed to *false* if you want cracked minecraft accounts to be able to join.
