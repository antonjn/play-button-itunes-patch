Play Button iTunes patch
========================

[Official Website](http://www.thebitguru.com/projects/iTunesPatch)

Overview
--------
This is a patch for removing the default OS X behavior of always starting iTunes when the play button on the keyboard is pressed. This feature can be useful for a lot of users, but it can also be annoying if you are using VLC, Nightingale or other similar programs that support the media keys.

The application will patch the Remote Control Daemon to prevent it from starting iTunes whenever you press the play button on the keyboard or an external remote control. This will only prevent iTunes from starting, all other functions (like play/pause while iTunes is running) will continue to work as before. The original file is backed up in case you would like to restore the original functionality.

![Screenshot](Images/Screenshot-1.0.png "Screenshot")

OS X El Capitan Compatibility
--------

This patch works by modifying a system file (rcd). With the new System Integrity Protection (SIP) functionality introduced in El Capitan you have to take additional steps to temporarily disable SIP. Hopefully I will get some time soon to update the binary to guide the user through this, but for now please follow the instructions documented on the [project page](http://www.thebitguru.com/projects/iTunesPatch).


General Information
-------------------
Author: Farhan Ahmad (<http://www.thebitguru.com/projects/iTunesPatch>)


Change Log
----------
    2015-03-02, fa: Farhan Ahmad
     * Published the all new GUI application!
     * Version changed to 1.0

    2014-01-19, fa: Farhan Ahmad
     * Added the '-KILL' to killall command because rcd doesn't seem to respect SIGTERM
       anymore.  Thanks for @quicksnap (https://github.com/quicksnap) for helping
       troubleshoot.
     * Version changed to 0.8.3

    2013-05-11, fa: Farhan Ahmad
     * Added step to self-sign the modified binary. This should
       prevent rcd from crashing on Mountain Lion.  Thanks to user48986 at
       http://apple.stackexchange.com/questions/64408/can-you-disable-a-code-signature-check
     * Version changed to 0.8.2

    2011-09-03	Farhan Ahmad
     * Added Michael Winestock's info.
	     http://www.linkedin.com/pub/michael-winestock/18/579/972

    2011-08-18	Farhan Ahmad
     * Added a fix to account for spaces in the directory where the patch is
       uncompressed. Patch submitted by Michael Winestock.
     * Version changed to 0.8.

    2010-11-28	Farhan Ahmad
     * Wrote a new python based patching script that dynamically patches the files
    	 instead of using bspatch and relying on a pre-supplied patch file. This
    	 should make the patch work with pretty much all versions of rcd.

    2010-11-23	Farhan Ahmad
     * Packaged and released the first version.


