
# TinyScanner-Connector

During the Covid pandemic, I've been using my old iPad to scan PDF with the Tiny Scanner+ v4.1.1 application that I bought a while back. I didn't want to buy the latest Tiny Scanner application since it requires a monthly payment. Therefore, I've designed this connector to quickly dump my scanned PDF's from my old iPad iOS 9.3.5 to my Mac.
  
# Technicality  

The app was design using Automator, some Applescript, and some Shell script.  
  
The icon was taken from the official TinyScanner application released in 2013 by Li Yunzhang.  
https://www.amazon.com/Tiny-Scanner-Pro-scanner-document/dp/B00FR88VTC  
  
The app works with the Tiny Scanner v4.1.1 (Tiny Scanner+ v4.1.1) using Wi-Fi Drive option enabled. It utilize the 'wget' command to download the content from the TinyScanner application on iPad iOS 9.3.5, and it dumps it into the "TinyScanner.app/Contents/Dump" directory on your Mac.  
  
# Small Guide
  
By opening the app, a Finder message box will open asking for the Server Address. This address can be found inside the iPad Tiny Scanner application, under 'Wi-Fi Drive' in the settings.  
<p align="center">  
  <img src=".media/Server-Address-Prompt.png" alt="drawing" width="450"/>  
</p>  
  
After providing the Server Address, the Finder will open the directory  "TinyScanner.app/Contents/Dump/$ServerSocket", where the $ServerSocket is the IP Address and Port number from the server address previously provided. Then the user is prompt to either "Do Nothing", "Sync", or "Download".  
<p align="center">  
  <img src=".media/Action-Prompt.png" alt="drawing" width="700"/>  
</p>  
  
- **Do Nothing:** Will only dismiss the message box. The directory will remain open. Select this option if you only want to access the directory on your Mac.
- **Sync:** Will download missing files only. *(If a file was modified but use the same name as the old one, deleting this particular file from your Mac directory is necessary before using the "Sync" option).*  
- **Download:** Will overwrite the whole directory with the content of the server (Redownload all files).  
  
  
If you have a lot of files that need to be transferred, it may take some times. As long as you see the following rotating gear in the menu bar, then files are being transfered from your iPad to your computer.  
![Menu-bar-Progression](.media/Menu-bar-Progression.gif)
  
  
# To download the app:

Downloading and unzipping the TinyScanner.zip file may results in a message saying *"App is damaged and can’t be opened. You should move it to the Trash"*. 
<p align="center">  
  <img src=".media/app-is-damage-message.png" alt="drawing" width="550"/>  
</p>  
A way around this, is to open the unzipped app using Automator and hit save. After, you can right-click on the app and click open.

