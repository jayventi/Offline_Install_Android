# Online and Offline Wireless Methods for Installing Unsigned Android Apps in the Field #

Here are two easy methods to install Android applications in the field without using signed apps or Google Play. These methods do not require direct connectivity to a laptop or a laptop at all and work just using Android phones. The intent here is for the most straightforward possible methods for deploying custom or dev apps particularly if they're available in a GitHub repository.

### Preferred Method Online From an APK in a GitHub Repository ###

If the applications APK can be made available via a URL endpoint it can be downloaded and installed. GitHub provides a direct URL for each file in a repository. If there's an APK in a GitHub repository it can be pointed at in the following manner if it's standard path in GitHub is say

`https://github.com/jayventi/Offline_Install_Android/blob/master/FDroid.apk` 

Then the appropriate URL to download the file would be

`https://github.com/jayventi/Offline_Install_Android/raw/master/FDroid.apk`

 A zip version 

`https://github.com/jayventi/Offline_Install_Android/raw/master/FDroid.zip`

### How to Send and Receive Apps Online From a GitHub repository###

1) On GitHub Place your apk file and generate the download url, tested on a standard browser.
2) You may want to produce a TinyURL for brevity sake
3) Configure the android to receive unsigned apps; this is done in 'settings' under 'security'
4) On the target android phone entering the download URL into a browser, this should trigger an option for a file download.
5) Immediately after its downloaded if the file is an APK android will prompt you if you want to install the application.

Done

##How to Side Install Android Apps Using Peer-to-Peer Bluetooth##
<br/>
###The Intent###
The intent of this app transmission-installation method is to produce a file on the receiving phone that itself can be used to retransmit the app again without Internet access, allowing for a self-sustaining retransmission network.  The method uses a zip file containing an APK which can be downloaded from the net; we were going to using a GitHub repository as an example, onto your phone and then your phone transmitted without the Internet using Bluetooth to a receiving phone. The receiving phone can open the zip, and install the application from it. Importantly the receiving phones zip file remains available for retransmission to new phones. This method relies on all internal android functionality except for the zip compression app which depending on your particular phone may require a separate third-party app. There are many generic compression programs if one is required try using RAR app.

###General Background On Downloading Files###
When downloading, generic files like zip files, downloads ended up in the /storage/emulated/0/download directory when using a browser and connected to the Internet via Wi-Fi or your cellular connection. If you're using Bluetooth file transfer, the file will be placed in /storage/emulated/0/bluetooth directory. The built-in tool we use will see these two directories as 'download' and 'bluetooth' respectively.

###General Process###
1) We start by downloads the zip file containing an APK over the Internet from our GitHub repository. The file will end up in the download directory. Once downloaded you will automatically be prompted to open the zip file once you open the file you can click on the APK which will trigger its install. 

2) The phone that obtained zip from the Internet can be paired with a receiving phone and the sending phone can navigate to the zip file in the download directory selected it for file transfer to the receiving phone. After receiving the zip will reside in the bluetooth directory where you will be automatically prompted to open and given the opportunity to extract and install it.

3) The phone that receives, the zip can now be used to transmit it as in step 1) with the exception that the zip file for phones that have received the zip file over Bluetooth will find it in the bluetooth directory.

Helpful note when Bluetooth pairing an android phone if you're not sure what the name of the target phone is navigate to Settings > About phone, on the target and check under 'Model number'.

###Steps for Bluetooth Side APK Installation###

1. In your android settings under security allow for the installation of unsigned applications by selecting settings> security > 'Unknown sources' on.
2. Using the steps in Preferred Method Online From an APK in a GitHub Repository download the zip APK file to your download directory using a browser.
3. Pair the transmitting and receiving phones using Bluetooth.
	1. On both phones and settings > Bluetooth locate the two phones to be paired and select the target phones. When pairing occurs correctly the phone being paired with will be prompted to accept the transmission, make sure that phone has no apps showing on the screen when that occurs. Some apps interfere with the pairing process notification showing up.
4. Navigate to the zip APK file on the sender phone.
	1. This can be done with a number of third-party file explorers but on modern android applications that can be done inside of settings Settings > Storage and USB > Explore.
	3. Inside of the Explorer view select either 'Downloads' or 'bluetooth' depending on whether the the file was obtained from the Internet or from a Bluetooth transmission. 
4. Select the file for sharing and choose sharing through Bluetooth.
	1. Highlight the zip file, the sharing symbol should appear at the top of the screen, select the sharing symbol.
	2. You should have a number of sharing sources if it's a generic zip file Bluetooth sharing should be an option, selected it.
5. You should be presented with a list of paired Bluetooth partners choose your transmission targets name. If initiation is successful a box should open on the target phone asking permission to receive the transmission, accept it.
6. To extract the zip file and install the APK.  Automatically on successful download either on the screen or in the successful download notification element that at the top of the screen you should be given the option to open the downloaded zip file.
	1.   Once this occurs you should see the uncompressed APK file, clicking on it should trigger it's install. 
	2.   Alternatively you may use the navigation steps outlined above in 4. Settings > Storage and USB > Explore and quick click on the zip should open the zip and give you the opportunity to click on the APK to install the app.
6. When complete don't forget to re-secure the phones and set 'Unknown sources' to off.

