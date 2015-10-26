# Remotely Control the Volume on Your Mac

There are two solutions available.

## Folder Actions (Recommended)

Detailed instructions are available in my Medium article [here](https://medium.com/@nicholasyan11/remotely-controlling-the-volume-on-your-mac-732f84282d8f#.ofxgh6gjg).

The short of it is create a special Dropbox folder and attach a folder action to this folder. Drop the remote_adjust_vol and adjust_volume scripts into the folder.

Here is the configuration for my folder action:

![Image of Folder Action](https://cdn-images-1.medium.com/max/2000/1*jFdOV7Zz60OgWRSeYygOMA.png)

To run, simply start the bash shell and type `sh adjust_volume [arg]`.

The arguments are as follows:
* **mute**
* **unmute**
* *x* (between -100 and 100, alters the volume by x%)

## Remote Apple Events:

To use this, simply download the remote_volume_control file. Ensure that the Remote Apple Events option is checked under System Preferences > Sharing on the Mac who's volume you want to control.

To run, simply start the bash shell and type `sh remote_volume_control [arg]`.

The arguments are as follows:
* **mute**
* **unmute**
* *louder* (increases the volume by 10%)
* *quieter* (decreases the volume by 10%)
* *louder x* (increases the volume by x%)
* *quieter x* (decreases the volume by x%)

The downside to this approach is that each time Apple will prompt you to enter the username and password for the computer you are connecting to.