# Online and Offline Wireless Methods for Installing Unsigned Android Apps in the Field #

Here are two easy methods to install Android applications in the field without using signed apps or Google Play. These methods do not require direct connectivity to a laptop or a laptop at all and work just using Android phones. The intent here is for the most straightforward possible methods for deploying custom or dev apps particularly if they're available in a GitHub repository.

### Preferred Method Online From an APK in a GitHub Repository ###

If the applications APK can be made available via a URL endpoint it can be downloaded and installed. GitHub provides a direct URL for each file in a repository. If there's an APK in a GitHub repository it can be pointed at in the following manner if it's standard path in GitHub is say

`https://github.com/jayventi/raw-bin-test/blob/master/FDroid.apk` 

Then the appropriate URL to download the file would be

 `https://github.com/jayventi/raw-bin-test/raw/master/FDroid.apk`

### How to Send and Receive Apps Online From a GitHub repository###

1) On GitHub Place your apk file and generate the download url, tested on a standard browser.
2) You may want to produce a TinyURL for brevity sake
3) Configure the android to receive unsigned apps; this is done in 'settings' under 'security'
4) On the target android phone entering the download URL into a browser, this should trigger an option for a file download.
5) Immediately after its downloaded if the file is an APK android will prompt you if you want to install the application.

Done

### How to Send and Receive Apps Offline ###

Offline application installation can be performed using third-party applications which facilitate sending and receiving using technologies like Bluetooth. Most, are supported through in-app purchase or advertisement. However, there is an application which attempts to entirely replace Google Play as an open source marketplace for apps, F-Droid. F-Droid which is open source itself allows for the downloading of applications from non-Google play repositories but also between phones which already have F-Droid installed. One of its most exciting features is that it allows for the pulling of F-Droid itself to the receiving phone if it does not already have it. 

Follow the instructions at [How to Send and Receive Apps Offline](https://f-droid.org/en/tutorials/swap/) found at F-Droid tutorials.

Note: F-Droid must be side installed itself 

For Popular ad-driven apps that are available on Google Play try
Apk Share
Bluetooth App Sender APK Share
