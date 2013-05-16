Alfred-Indigo-Workflow
======================

An Alfred workflow to control your Indigo (http://www.perceptiveautomation.com) devices, action groups, variables.  This workflow works great if you have set up your indigo in convenient ways, such as configuring macros based on variables or action groups.  For example, a variable that controls the brightness level for several lights in a room would allow you to change the lights via a command to Alfred: indigo variable lights 50

The workflow is partitioned into three steps, started through the keyword "indigo"

Step 1: Selection of Device, Variables, or Actions (static)

Step 2: Selection of the specific device, variable, or action desired (dynamically loaded from Indigo)

Step 3: Giving a command (on, off) or value (for devices and variables only, action groups are immediately executed)

Change Log
-----
2013-05-15: Many improvements to the coding.  Added support for password protected Indigo servers.  Added a separate configuration file to configure server, login, password, and debugging options.

2013-05-10: Improved debugging, fixed bugs with devices being given the "isOn" command.  Added some checks to see if the scripts had the appropriate permissions to execute.

2013-05-07: Initial release


Known Issues
-----
1. Only devices that respond to "isOn" and "Brightness" parameters work (in other words, only Lamps)

2. The Workflow does not remove options as you type more specific names of your devices, actions, and variables, I plan on working on this.

3. If you stop in the middle of one of the "steps" (see above) without completing, the workflow will pick up where you left off.  For example. if you type "indigo Devices" into Alfred then hit escape, the next time you type "indigo" into Alfred, no matter how long it has been since Step 1, it will pick up with the "Device Selection Step" (Step 2).  This is a consequence of how I store the state information, I also plan to find a way to better way in the future, or at least have it time sensitive.

Troubleshooting
-----
To turn on logging, go to your workflow directory and edit "indigo.config" and change DEBUG="TRUE"
Recreate the problem and send me the log.txt (or the log file name you specify) file in the workflow directory and I will try to help

Install
-----
1. You should be able to simply add the workflow to your Alfred simply by double clicking.
2. Set your server address by typing: "indigo http://HOST:PORT" (be sure to not add a trailing slash "/").  You can reset your server at any time by typing: indigo server http://HOST:PORT into Alfred.
3. If you have a login / password set on your indigo server, edit the indigo.config file to set it (you will find this file in your workflow directory, I plan to make a command to configure the login and password in a future release)
3. Should be good to go!

Keep in mind this could potentially be buggy.  Please reach to me if you discover problems.