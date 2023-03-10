
# WhatsApp Key/DB Extractor

Allows WhatsApp users to extract their cipher key and databases on non-rooted Android devices.

See [this XDA Forums thread](https://forum.xda-developers.com/t/tool-whatsapp-key-db-extractor-crypt6-12-non-root-updated-october-2016.2770982) for discussions on how to use this script and some issues you might encounter.

## BRANCH UPDATES:

 * v4.8.1 - Fixed small error where installed version number wasn't being parsed and preserved properly.
 * v4.8   - Legacy URLs no longer work; replaced with links to [APKsFree.com](https://androidapksfree.com/whatsapp-messenger/com-whatsapp).
 * v4.7.9 - Flattened code structure and added local binary dir to path.
 * v4.7.1 - Refactored code to make structure clearer and reduce redundancy.
 * v4.7   - Added new sanity checks and support for Android API 24 (7.0 Nougat).
 * v4.6   - Updated primary mirror for legacy apk (again).
 * v4.5   - Fixed issue pushing cipher key to emulated storage.
 * v4.4   - Changed primary mirror for legacy apk.
 * v4.3   - Added PowerShell version as optional alternative to bat version.
 * v4.2   - Added support for specifying adb backup passwords.
 * v4.1   - Added support for Android API 23 (6.0-6.0.1 Marshmallow).
 * v4.0   - Fixed issues with Android API 14-17 (4.0-4.2 Jelly Bean).

## PREREQUISITES:

 1. O/S: Windows Vista, Windows 7, Windows 8, Windows 10, Mac OS X or Linux
 1. Java - If not installed: https://www.java.com/en/download/
 1. ADB (Android Debug Bridge) Drivers
 1. USB Debugging must be enabled on the target device. Settings -> Developer Options -> (Debugging) USB debugging.
    If you cannot find Developer Options then please go to: Settings -> About phone/device and tap the Build number multiple times until you're finally declared a developer.
 1. Android device with Android 4.0 or higher - i.e, Ice Cream Sandwich, Jelly Bean, KitKat, Lollipop, Marshmallow or Nougat.

## INSTRUCTIONS:

 1. Extract "WhatsApp-Key-DB-Extractor-master.zip" maintaining the directory structure.
 1. Click on "WhatsAppKeyDBExtract.bat" (Windows) or "WhatsAppKeyDBExtract.sh" (Mac OS X / Linux).
 1. Connect your device via USB, unlock your screen and wait for "Full backup" to appear.
 1. Enter your backup password or leave blank (if none set) and tap on "Back up my data".
 1. Confirm backup password in your command console and then check your "extracted" folder.

## TROUBLESHOOTING:

 1. If you have never used USB Debugging before, you may also need to verify the fingerprint.
 1. If you have set a default backup password in your Android settings, then this MUST be the
     backup password that you PROVIDE when prompted to backup your data. Else it WILL fail!
 1. Linux and Mac OS X users may need to set the script permissions as executable. Depending on the
     adb permissions, you may also need to "sudo ./WhatsAppKeyDBExtract.sh" from your command console.
 1. If you're having issues with "WhatsAppKeyDBExtract.bat" then right click "WhatsAppKeyDBExtract.ps1"
     and select "Run with PowerShell". You may have to enter "y" at first run for execution policy.
 1. If you get an error saying "AES encryption not allowed" then you need to update your Oracle Java
    Cryptography Extension (JCE) to Unlimited Strength Jurisdiction Policy Files.

## CREDITS:
 AUTHOR: TripCode  
 THANKS: dragomerlin for Android Backup Extractor and Abinash Bishoyi for being cool.  