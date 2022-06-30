# TinyScanner-Connector
 Application designed to dump previously scanned pdf from an old iPad iOS 9.3.5 having the Tiny Scanner+ v4.1.1 application. Since I've previously paid for that application in the pass, before they decided to release the same application but with a monthly payment, I've decided to recycle my old iPad to scan PDF during the Covid pandemic. I've been doing it using a bash script, but I've decided to give it a refresh and make and actual MacOS application.  
  
The app was design using Automator, some Applescript, and some Shell script.  
  
The icon was taken from the official TinyScanner application released in 2013 by Li Yunzhang.  
https://www.amazon.com/Tiny-Scanner-Pro-scanner-document/dp/B00FR88VTC  
  
The app works with the Tiny Scanner v4.1.1 (Tiny Scanner+ v4.1.1) using Wi-Fi Drive option enabled. It utilize the 'wget' command to download the content from the TinyScanner application on iPad iOS 9.3.5.  
  
The content is fetched from the provided server address, and dumped into the "TinyScanner.app/Contents/Dump" directory on your Mac.  
  
By opening the app, the Finder open the directory "TinyScanner.app/Contents/Dump/$ServerSocket", where the $ServerSocket is the IP Address and Port available under 'Wi-Fi Drive' in the settings inside the iPad application.  
  
Then the user is prompt to either "Do Nothing", "Sync", or "Download".  
  
- Do Nothing: As the name implies, does nothing.  
- Sync: Will download missing files only. (If a file was modified but use the same name as the old one, deleting this particular file is necessary before using the "Sync" option).  
- Download: Will overwrite the whole directory with the content of the server (Redownload all files).  
  
# To download the app:
Downloading the TinyScanner.zip file may results in a message saying "App is damaged and can’t be opened. You should move it to the Trash". All step to reproduce this app are provided in the Automator folder.
  
