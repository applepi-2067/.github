# Apple Pi GitHub Org
This org contains current and past robot code and code from other projects like scouting software.

## Ancient repos (pre-2017)
I know I'm about 6 years too late for documenting this, but better late then never. Contact cory2067 if you have any questions, and feel free to delete this section or move it to a more hidden place.

The most relevant stuff here is probably PiScout. If using PiScout in the future, I'd recommend rewriting it entirely, but if you want some old repos for reference, here are the different iterations:
- PiScout-2015: The idea was to have a bunch of scouters with laptops. They would input match data using a Python program, with a GUI built with PyQt4. The laptops would sync to a "head scout" laptop via bluetooth, since we couldn't guarantee having wifi at events. We never ended up running this at an actual event, and I don't think we did any testing to see whether the bluetooth approach was viable.
- PiScout-2016: We ended up succesfully using this second iteration during the 2016 season. Scouters would fill in a scantron-like sheet during a match, and they'd bring the sheet to a central laptop with a USB scanner. The laptop had a Python program that reads the sheet using OpenCV for vision processing, and then would post the results to a webserver. The webserver was also written in Python, which communicates with a sqlite database that stored all the scouting data. The code for the server is a total nightmare -- any future iteration needs to certainly rewrite it. 
- PiScout-2017: This was after I graduated, but I started to rewrite the PiScout webserver to be a little more sane. I never made it very far, so this repo is probably not worth looking at.
- [Team 238's PiScout fork](https://github.com/FRCTeam238/PiScout): Team 238 forked PiScout-2016 and heavily reworked it. This is probably a better example to follow than the original.

Another interesting thing is AppleScript, which lets you write quick autonomous [scripts](https://github.com/applepi-2067/Robot-2016/blob/master/autonomous.apple) on the fly, which gets executed by an interpreter written in LabVIEW. Unlike PiScout, I tried to keep the code pretty for this one. The original code is [here](https://github.com/applepi-2067/Robot-2016/tree/master/AppleScript). And [here's the manual](https://docs.google.com/document/d/1xK6Xrt1jQ4QNUTDMHz79VnfazF0mGnUEUrCXm5Chn_Y/edit) that explains how to use it. It looks like in later years, it was updated in a separate repo [here](https://github.com/applepi-2067/AppleScript-2017). If the team ends up moving to Java, then obviously this is useless, but it might be worth creating a similar scripting language in Java. (It proved pretty convenient mid-event and at the very least, writing an interpreter is a cool programming exercise)

One more fun thing to play with is the swerve drive game (based off Aerial Assist from 2014), which still lives here: http://applepi-2067.github.io/swerve/
