Automation
==========

First thing you need to do is to start the Emulator. 

<B>Install the Android SDK</B>

Download the Android SDK, and unpack it to ~/android_sdk/. NOTE: The location of the Android SDK must exist in ../android_sdk, relative to the directory containing the Selenium repository.

<B>Setup the Environment</B>

Android test can run on emulators or real devices for phone and tablets.

<B>Setup the Emulator</B>

To create an emulator, you can use the graphical interface provided by the Android SDK, or the command line. Below are instructions for using the command line.


<B>First, let's create an Android Virtual Device (AVD):</B>

$cd ~/android_sdk/tools/

$./android create avd -n my_android -t 12 -c 100M

-n: specifies the name of the AVD.

-t: specifies the platform target. For an exhaustive list of targets, run:

./android list targets
Make sure the target level you selected corresponds to a supported SDK platform.

-c: specifies the SD card storage space.

When prompted "Do you wish to create a custom hardware profile [no]" enter "no".

<B>Note:</B> An Android emulator bug prevents WebDriver from running on emulators on platforms 2.3 (Gingerbread). Please refer to AndroidDriver#Supported_Platforms for more information


Now, start the emulator. This can take a while, but take a look at the FAQ below for tips on how to improve performance of the emulator.

$./emulator -avd my_android &

<B>Setup the Device</B>

Simply connect your Android device through USB to your machine.
