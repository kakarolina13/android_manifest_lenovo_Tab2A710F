# android_manifest_lenovo_Tab2A710F
Manifest and Howto , to build custom ROM for Tablet Lenovo A7-10F

An attempt to build custom ROM for Lenovo A7-10F tablet (In progress...)

master branch is for Omnirom Lollipop 5.

cm-12 branch is for CyanogenMod version 12.x (Lollipop)

Built from Lenovo "Open Source Code"



Local manifests for building Lenovo Tab2 A7-10F tablet
======================================================

How to use :
------------

Yes all the source code is available on Github.

These are the steps to build this rom.

- Install a suitable OS. You can use a virtual machine running Ubuntu 14.04 64-bit, or a physical one : both are supported.

- Prepare the system, do steps 1, 2 and 5 of this guide, to configure your development machine :

http://forum.xda-developers.com/showthread.php?t=1762641
Tutorial To Compile JB on Ubuntu - xda-developers

WARNING : To have success when building ROMs from repository, it's required to use Java-7 JRE (1.7)
If you don't use this one, you'll have unpredictable errors, like C header files malformed.

It's recommanded to have a PATH pointing the right Java JRE at first position, in your environment !



Then run these commands:
------------------------

mkdir YOUR_ WORKING_DIR

cd YOUR_WORKING_DIR

example for omnirom 5.0 :
-------------------------

repo init -u git://github.com/omnirom/android.git -b android-5.0

mkdir .repo/local_manifests

curl https://raw.github.com/PixNDom/android_manifest_lenovo-Tab2A710/master/A710F_manifest.xml > .repo/local_manifests/A710F_manifest.xml

repo sync


The sync will take a while and download something like 15 GB of source code.

Finally build the rom with these commands:
------------------------------------------

 source build/envsetup.sh

 brunch a710f



If all goes well this will create a zip file into 'out' folder, that can be flashed on the tablet!

