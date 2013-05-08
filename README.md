Alfred-Indigo-Workflow
======================

An Alfred workflow to control your Indigo (http://www.perceptiveautomation.com) devices, actions, variables

There are three stages, started through the keyword "indigo"

Stage 1: Selection of Device, Variables, or Actions
Stage 2: Selection of the specific device, variable, or action desired
Stage 3: Giving a command (for devices and variables only)

Change Log
-----
2013-05-07: Initial release

Known Issues
-----
1. Only devices that respond to "isOn" and "Brightness" parameters work (in other words, only Lamps)
2. Plugin does not remove options as you type, I plan on working on this.

Install
-----
1. You should be able to simply add the workflow to your Alfred simply by double clicking.
2. Set your server address by typing: "indigo server http://HOST:PORT" (be sure to not add a trailing slash "/")
3. Should be good to go!

NOTE: I'm particularly interested in anyone who has problems because the permissions of the bash script files are not correct.  I didn't have a way of testing that thoroughly.

Keep in mind this could potentially be buggy.  Please reach to me if you discover problems.