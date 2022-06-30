
Author: Vincent Beaulieu - https://github.com/vincbeaulieu
License: Open-Source (The Unlicense)

The icon was taken from the official TinyScanner application released in 2013 by Li Yunzhang. https://www.amazon.com/Tiny-Scanner-Pro-scanner-document/dp/B00FR88VTC

The app works with the Tiny Scanner v4.1.1 (Tiny Scanner+ v4.1.1) using Wi-Fi Drive option enabled. It utilize the 'wget' command to download the content from the TinyScanner application on iPad iOS 9.3.5.

The content is fetched from the provided server address of the app, and dumped into the "TinyScanner.app/Contents/Dump" directory.

By opening the app, the Finder open the directory "TinyScanner.app/Contents/Dump/$ServerSocket", where the $ServerSocket is the IP Address and Port available under 'Wi-Fi Drive' in the settings inside the iPad application.

Then the user is prompt to either "Do Nothing", "Sync", or "Download".

- Do Nothing: As the name implies, does nothing.
- Sync: Will download missing files only. (If a file was modified but use the same name as the old one, deleting this particular file is necessary before using the "Sync" option).
- Download: Will overwrite the whole directory with the content of the server (Redownload all files).

# Todo:
Have a file holding the default ServerAddress URL. Once this file as a valid entry, proceed with the download.
Else, prompt again for the ServerAddress and overwrite current URL.


-- DISCLAIMER --

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.


For more information, please refer to <https://unlicense.org>

