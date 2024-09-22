# Geometry Dash Savefile Fixer

This tool can fix most problems that make the game unable to open due to the savefiles. (which means that the game will only launch if you move the savefiles to other folders.)
This is an ameliorated version of the [Geometry-Dash-Savefile-Fix](https://github.com/WEGFan/Geometry-Dash-Savefile-Fix) made by [WEGFan](https://github.com/WEGFan) but since he seems inactive now, and there are some issues opened, I wanted to help these people to don't lose their data. This is an entire rewrite of the code, I licensed it under [MIT License](https://hgstyle.mit-license.org/2023) so you can do almost anything you want on this software, including using it in closed-source projects and so on... Only 1 thing: credit me (plz). Thanks you all.

## Note

### 2.2 certainly fixed this bug, so if you are using 2.2 it's very very unlikely this program will fix your game. However, for 2.1 and before, this software is still quite useful, and still working great!

## Instructions

If they seem really long, its because I try to include every cases to make everyone can use this programm. You can skip sections for Linux users (since they are really long) if you aren't using Linux (remember, Ubuntu, Debian, etc... are Linux!). If its so complicated on Linux, it's because there are many different "editions" of Linux (actually called distributions or distros, example: Ubuntu and Debian are Linux distributions) and they have different applications, with different versions, and its sometimes hard to make an operation working on every distribution.

## Not working?

Firstly, check the [project FAQ](https://github.com/HGStyle/GD-SaveFileFixer/blob/master/FAQ.md) If you encounter any problem (unable to fix / doesn't work after fixed), get help by [creating an issue](https://github.com/HGStyle/GD-SaveFileFixer/issues/new) (edit: @superchupu on Discord told me issues are disabled, now they are back - sorry) or [contact me on Discord](https://dsc.gg/hgstyle).

### Using prebuilt binaries

In the [GitHub Releases](https://github.com/HGStyle/GD-SaveFileFixer/releases), I post the source code of the project per version, but also binaries (= executable files) that I build myself on my computer (mostly on live sessions like MX Linux or Hirens BootCD). You can download these and run them on your computer directly without installing the whole [Python programming language](https://python.org/) (if you dont know if your computer is 64bits or 32bits, choose the 32bits version). Note that **I dont post binaries for MacOS, iOS and iPadOS due to the fact that I dont own any Apple device since I hate Apple** (no drama please, its just my opinion. OK, actually I own some iPhones from 2013 but they are so old that I can't even install new apps on them). Even if you download prebuilt binaries, you will still have to install some apps if you are on mobile.

### Using the source code

You may use the source code because there isn't any binary file for you system, or because you dont know which binary file corresponds to your device, or simply because you think that just before compiling binaries I injected a malware in them. (which, I guarrentee it, is false) but if you dont want to risk to be hacked (which is something that I entirelly respect, even me sometimes I prefer running source code that binaries because people reads the code and sees there is no malware in it), you may download the source code in [GitHub Releases](https://github.com/HGStyle/GD-SaveFileFixer/releases), which is the only file that ends with `.py`. You could also download the source code ZIP or TAR file automatically made by GitHub, but you will have to decompress it to get the Python script file. You could also download it from the `master` branch, but I don't recommend that way since I can make changes that makes the someware buggy (since I use online GitHub code editor to edit code of this repository and then I test it on annother PC that have Geometry Dash installed, since my main PC can't support Geometry Dash for the reason that I'm on Linux and when running Geometry Dash with WINE, it says it's a 32 bits program and it can't run it since my PC is 64 bits).

### Running on Windows, MacOS or Linux

If you have downloaded the source code and you are on Windows or MacOS, go to the [Python 3.11.4 downloads](https://www.python.org/downloads/release/python-3117/) which is the latest Python version for now and is tested to be functionnal with my code, scroll down until you see the header "Files", then download and install the version that is right for you (if you dont know if your computer is 64bits or 32bits, choose the 32bits version). Linux users does not have any Python installer on the Python website. Instead, open your package manager (either in graphical UI or in command line) and install the package `python3` and `python3-pip`. After, check the Python version by running the command `python3 --version` in a terminal (don't use `python3 -v` because some old Python versions understands that `-v` means `--verbose` instead of `--version`, if you do it you will get a Python interpreter with lots of weird logs texts for debugging Python, to exit type `exit()` and validate using the Enter key). If your Python version is 3.8 or newer (Python 3.9, 3.10, 3.11, etc...) it should work fine (programm tested on Python 3.8, 3.9 and 3.11). If you get an older version (example: Python 3.6) try to install in your package manager the package called `python3.8` or `python3.10` and then, instead of running the command `python3 --version`, run `[the name of the package you installed] --version` (example for package `python3.8`: `python3.8 --version`). And make sure its Python 3.8 or newer. If the command isn't found, you will have to compile Python yourself from the source code, but don't panic, its pretty easy if you [follow this tutorial](https://ubuntuhandbook.org/index.php/2021/10/compile-install-python-3-10-ubuntu/) (if the commands containing `apt` does not works, try replacing `apt` by `yum`, `pacman` or `dnf`, else try skipping these commands containing `apt` or search Google for annother tutorial, search `How to compile Python 3.10 on [your operating system name, example: Debian]`).
For every OS, after installing Python, you will have to open a terminal (search and run `cmd` on Windows, on MacOS and Linux, search and run `Terminal`) and run the command: `pip install pycryptodome` (its really important if you are fixing MacOS or iOS savefiles, if it fails and you are not fixing MacOS/iOS savefiles its okay, but it should rarely fail).
If you have downloaded a prebuilt binary, you dont have to do anything.
To run the program, on Windows and MacOS, double-click on it. Linux users could try clicking on it (generaly one time) but in most cases it will not work. The solution in that case is to right-click anywhere in the folder on an empty zone, click on "Open terminal here". If this option isn't here, it should be accessible via the options bar at the top of the file manager window, in most cases, under tools, then click on "Open terminal here" or something similar. Then, execute this command in the terminal: `[the name of the python package you installed] [the name of the source code file you downloaded from the github repo]`. In most of case this command will be: `python3 GD-SaveFileFixer-SourceCode.py`. Also, if you downloaded a zip or a tar file, make sure to extract before running the command. You can use [7-zip](https://7-zip.org/) by example (also notice that Windows, MacOS and Linux have a tool installed by default to extract ZIP files, but not TAR files, except on Linux).

### Running on Android

Firstly, you will have to make the Geometry Dash app data accessible to you. By default, to avoid others apps to steal your data, Android has a protection that only allows the installed app to access to his data. Even you, the user, cannot access to it. To bypass this, the most known way is rooting your Android device. This task is dangerous. Really dangerous: do it incorrectly and you may never see your phone starts again. Also, rooting your Android device may cancel the warenty of the device, depending on what you have signed for while getting the warrenty. To avoid users to do this dangerous task and risk to lose all of their data, I found another way, which is still a bit hard to realise but is way much more safer. I'm sorry, but if you have a GDPS (or any Geometry Dash app that has been signed using a test development key like [old App Cloner versions](https://appcloner.blog/2023/01/14/google-play-protect-signing-keys/) or any version of APK Editor with default settings for signing apps) you can do this using only your Android device, but this way is really long to do, and if you have the real Geometry Dash or annother app that hasn't been signed using the test development key (including the Geometry Dash app from the Play Store, every Android mod menus and modified GDPS such as GDPS Editor 2.2) you will need two devices: your Android device and a Windows, MacOS or Linux (they cannot be the same). Here are the steps:

To know is your Geometry Dash app signed with testkey (so you can use the "is a GDPS" version of the fixer, which requires only your device and is less long):
  - Download and install the app [APK Signature Viewer](https://apkpure.com/fr/apk-signature-viewer/com.badzzz.apksigninfoextractor)
  - Open the app
  - Search for your Geometry Dash
  - Click on it
  - See if its written somewhere "CN=Android Debug" in the message box that popped up.
  - If there is "CN=Android Debug" written, your Geometry Dash is signed with testkey. Else, its not.

If your Geometry Dash version is a GDPS (or your Geometry Dash is signed using testkey, or has been modified and signed using any version of APK Editor with default signing settings, or [modified using an old version of App Cloner](https://appcloner.blog/2023/01/14/google-play-protect-signing-keys/)) and you aren't on a rooted device:
  - Install the app [APK Extractor](https://play.google.com/store/apps/details?id=com.ext.ui) from the Play Store.
  - Open the app. Search for your Geometry Dash (or your GDPS, in case it's a GDPS)
  - Memorise the package name (which is usually formated like `aaa.bbbbbbb.cccccccccccc`). Since there is many steps, I recommend you to write it on a sticky note.
  - Click on the app to extract his APK. We'll need it later.
  - Do not uninstall APK Extractor since we'll need it later.
  - If the package name you memorised is `com.robtopx.geometryjumq` (notice the `q` at the end !):
      - Download and install [APK Editor Pro](https://dl.hgstyle.fr/Apps/AndroidHackerKit/APK_Editor/Clean/APK_Editor_Pro.apk)
      - Download the APK of Geometry Dash (but not the one used by GDPSes, and it should be version the same version as the app). I recommend using this one: [Download Geometry Dash 2.111 APK](https://dl.hgstyle.fr/Every_Geometry_Dash_Versions/Android/GeometryDash_Normal_2.111.apk) but if you want other Geometry Dash versions, you can go [here](https://dl.hgstyle.fr/Every_Geometry_Dash_Versions/Android/) to download the right file.
      - Open APK Editor Pro, alow storage access, click "Select Apk from App" and click on your Geometry Dash or your GDPS
      - Select "Full Edit" and then "Decode All Files", then go to "Files" in the toolbar of APK Editor Pro
      - Select the folder `assets` and `lib` and click "Extract", then go to your downloads folder and click "OK" (then wait for it ends and exit the app)
      - Make sure to exit the app completely and reopen it, now click "Select an Apk File" and click on the APK file of Geometry Dash 2.111 you downloaded (make sure the APK is stored in your internal storage, not in your SD card !)
      - Click "Full Edit" and then "Decode All Files" again and go to files
      - Select the folders `assets` and `lib` and click delete
      - Click the button with a plus symbol in a folder, and go to "Import Folder"
      - Click on the "..." button and browse into the `assets` folder in your downloads folder and click "OK"
      - A field will be filled automatically, be sure to see that the last word separated by the "/" is `assets` else click cancel and repeat the two last steps
      - Click "OK" and wait for it imports the folder `assets` into the APK
      - Again, click the button with a plus symbol in a folder, and go to "Import Folder"
      - Click on the "..." button and browse into the `lib` folder in your downloads folder and click "OK"
      - A field will be filled automatically, be sure to see that the last word separated by the "/" is `lib` else click cancel and repeat the two last steps
      - Click "OK" and wait for it imports the folder `assets` into the APK
      - Click on the "Build" button and wait for it builds the APK file
      - Open your file manager, go to internal storage, go to the folder "ApkEditor" (if you see multiple files, ignore those that aren't an APK) and move the APK file to the downloas folder in your internal storage
      - Optionally, you can delete the "ApkEditor" folder and/or the APK Editor Pro app
  - Download an install [App Cloner Pro](https://dl.hgstyle.fr/AndroidHackerKit/Other_apps/App_Cloner_Pro.apk)
  - Open App Cloner
  - If the package name you memorised is `com.robtopx.geometryjumq` (notice the `q` at the end !):
      - Click on the folder icon and click OK when a message box appears
      - Click the browse files logo
      - Open your downloads folder and click on the APK you just moved here
  - Else:
      - Search the Geometry Dash app (or your GDPS) and click on it
  - Scroll down and go to "Storage options"
  - Click on "Redirect external storage" and check the "Enable" box
  - Scroll down and enable "Acessible data directory"
  - Go back to main options categories
  - Scroll up and click on "Clone number" option
  - Check the box "Replace original app" and click "OK"
  - Click the button with the App Cloner logo on it, click "OK" and wait for it ends
  - When you can, click on the "Cancel" button (this will not delete the APK modified by App Cloner)
  - Go to the "Cloned APKs" category and hold on the first of the two apps that seems the same, then stop holding
  - In the upper toolbar click the diskette logo and save the file to your downloads folder
  - Wait for the app to say "Successfully saved file" at the bottom of the app UI
  - Close the app and open your file manager
  - Go to your downloads folder by going to storage and then in the "Download" folder
  - Search for the APK made by App Cloner anc open it/click on it
  - It will normally show something like "Do you wanna update this app ?", so click "Install" (or "Update" depending on your Android version)
  - If it says "App not installed" it can means two things: you dont have much space free on your device (this normally never happens since the update only adds like 5 mb of code from App Cloner) or (in most of cases) your Geometry Dash hasn't been signed using the test development key, you will have to use the other way with two devices
  - If it worked, open your Geometry Dash, and close it. (If it still crashes like before, its not a problem)
  - Exit all the apps and go to your browser to download the latest version of the Python programm. There is a binary for Android but I dont recommend it and it may be deleted in the future since Python installation in Termux (the app we'l use to launch the programm) is easy. Download it using [GitHub Releases](https://github.com/HGStyle/GD-SaveFileFixer/releases), download the first file ending with `.py` to your Downloads folder on your internal storage (not SD card ! if its on your SD card you will have to move it to your internal storage download folder).
  - Download and install the latest version of [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk), then open the app and wait for the loading to finish. Dont use the Google Play Store version since it is no longer updated and broken. You will get a terminal like on Linux, but dont panic, I'll guide you !
  - Open the app when it's installed
  - You will have to allow the storage access since [its not enabled by default](https://wiki.termux.com/wiki/Termux-setup-storage). To do that, simply type `termux-setup-storage` and press enter. Now allow storage access and you are ready ! You can enter the next command when you see the dollar symbol back and waiting you for the next command.
  - If you are on Android 11 or later (or you dont know which version of Android you have), go to Settings (exit Termux, you can completely close it or not), Applications, Termux, Permissions, disable storage access and re-enable it. [This is due to an Android bug which cannot be fixed by the Termux community.](https://wiki.termux.com/wiki/Termux-setup-storage) Then go back to Termux.
  - Now we'll update the Termux programms. Simply type `apt update`, then press enter. After, type `apt upgrade -y` and press enter. After, remove unnecesary software (its automatic and won't break anything) by typing `apt autoremove -y` and press enter. (from now I will no longer say "Press enter", but you will still have to do it after typing a command)
  - Now we will install Python. Simply type the command `apt install python3 python-pip -y` and wait. Notice that this can take up to some minutes, depending on your device and internet connection speed.
  - Now we need to install Python depencies. This can be done by simply running `python3 -m pip install pycryptodome`. If it fails, it's not really important, just skip this step like if it was done correctly.
  - Now you will have to naviguate to your download folder. Firstly, run the command `cd /storage/emulated/0` to go to your internal storage. Then type the command `dir` to list all the files and folders. Find your download folder name and run the command `cd [entire name of your download folder]`. It's usually `cd Download`.
  - Now, find the name of the Python script file. Run the command `find . -name "*.py"` (dont forget the dots). You will get the name of every file ending with `.py` (so, for almost every user, only one file: the actual Python script we need to run).
  - Run the Python script by doing `python3 [python script full file name]`. It's usually `python3 GD-SaveFileFixer-SourceCode.py`. If the Python script filename contains spaces, run `python3 "[python script full file name]"` (dont forget the two `"`: one at the start, one at the end of the filename).
  - If the package name you memorised isn't `com.robtopx.geometryjump`, the second option won't work. That's why it is not recommended, use the recommended option 3 instead. (it should not be long)
  - Once the programm has done running (you see the `$` symbol of Termux), close Termux.
  - Try opening Geometry Dash (or your GDPS), it should be fixed. BUT DONT QUIT THIS TUTORIAL OR YOU COULD GET HACKED.
  - Now we have a problem (not really since I have the solution): every app can access to the game data. Why is this a problem ? They can access your savefiles, so they can access your account, and even, your password. Almost no apps actually steal data from Geometry Dash since they normally can't, but no one knows. To fix this high security issue, go to your file manager, internal storage, then go to the folder called "ApkExtractor", then to the folder called with the same name as your Geometry Dash or GDPS app, then install the only APK in this folder. This will remove the App Cloner changes but not the Python script changes. After this, you are 100% safe.

If you dont have a rooted phone and the method before this one does not works for you:
  - On your Android device, install [Package Name Viewer 2.0](https://play.google.com/store/apps/details?id=com.csdroid.pkg) from the Play Store
  - Open the app, and search the Geometry Dash you wanna modify and memorize its package name (which is usually formated like `aaa.bbbbbbb.cccccccccccc`) (write it on a sticky note by example)
  - Optionnally, uninstall Package Name Viewer 2.0
  - Go to Settings, go to About your device, Informations about the software, and spam the version number box. (Click on it atleast 7 times fastly)
  - Confirm your device code/schema if you have one
  - Go back to settings menu, scroll down and you will have a new category called "Developers options": go into it.
  - WARNING: YOU SHOULD NOT MODIFY A SETTING WITHOUT KNOWING WHAT ARE YOU DOING ! PLAYING WITH THESE SETTINGS MAY MAKE YOUR DEVICE COMPLETELY UNUSABLE AND USELESS, AND YOU MAY LOSE ALL YOUR DATA !
  - Scroll down and enable USB Debugging, so we can use special software to access your device from the other device
  - Accept the warning
  - Be sure you trust the computer: if it has a malware on it, the malware could steal your Android device data or even infect it ! Also, try to not use a MacOS computer, because I made a mistake in the code so MacOS users will have to install extra software.
  - On the computer, download ADB from one of these three links, depending what OS it is running: [Windows version](https://dl.hgstyle.fr/Android_Platform_Tools/PlatformTools_Windows.zip) - [MacOS version](https://dl.hgstyle.fr/Android_Platform_Tools/PlatformTools_MacOS.zip) - [Linux version](https://dl.hgstyle.fr/Android_Platform_Tools/PlatformTools_Linux.zip)
  - Decompress the downloaded ZIP file in a folder
  - Download the ABE utility by [clicking here](https://github.com/nelenkov/android-backup-extractor/releases/download/master-20221109063121-8fdfc5e/abe.jar) and move it to the folder where are ADB files
  - Open the folder in your file manager and to open a terminal:
      - On Windows: [Click on the path of the folder and type "cmd" then validate (click to see screenshot)](https://cdn.mos.cms.futurecdn.net/KdeamF4DcfAorSckFR69ZW.jpg)
      - On MacOS: [Click Finder, then services and finally "Open terminal at folder" (click to see screenshot)](https://www.maketecheasier.com/assets/uploads/2021/10/launch-any-folder-mac-terminal-new-terminal-at-folder-2.jpg)
      - On Linux: Right-click in an empty space and click "Open terminal here". If the option isn't here, in the toolbar click "Tools" and then "Open terminal here"
  - In the terminal, type the command `java --version` and press enter. If the `java` command is not found, [install Java by following the instructions here](https://www.java.com/en/download/) or if you are on Linux, search `openjdk` in your package manager and install a version of it (depeding on the package manager, Java can be found as `openjdk-11` by example) then after installing, go back to the terminal and retype the command to see if the command is found (it should be found now)
  - Link your Android device and your PC using a charging cable
  - In your file manager, make sure you can see that your device is pluged in, else change cable and recheck until you can see it
  - In the terminal, type `./adb devices` (or `.\adb.exe devices` if you are on Windows): you should see a list of devices, only one device should be detected: it's yours (you just have to check there is a device detected)
  - Now run the command `./adb backup [package name of the geometry dash app]` (on Windows, replace `./adb` by `.\adb.exe`, notice that it's an antislash on Windows, and on other systems its a normal slash)
  - On your device, you will have to enter a password: enter a simple password since the encryption for the backup is actually useless for us. The only important thing: make sure you remember it ! Also, make sure it does not contain any special characters, only letters and numbers. Then, validate the backup creation and wait for it finishes.
  - While its creating the backup, do not touch your charger to make sure it does not unplug.
  - Also (on the PC), Windows 10 users should [enable file extensions in the file manager (click for tutorial)](https://www.howtogeek.com/205086/beginner-how-to-make-windows-show-file-extensions/). MacOS users should also do it by [following this tutorial (do it for every files)](https://support.apple.com/guide/mac-help/show-or-hide-filename-extensions-on-mac-mchlp2304/mac). Linux users may see them by default in most cases.
  - There is no progress bar, but if you wanna has a proof that it's running, you can right-click on the "backup.ab" file in the folder you previously opened in your file manager, then properties: you can see the file size getting bigger and bigger with time.
  - Once the programm in the terminal has stopped, the backup is finished. But since it is encrypted and in an unknown format, we'll use the ABE utility to decrypt it.
  - Run the command `java -jar abe.jar unpack backup.ab backup.tar [your password]`. Make sure the password is exactly what you put ! Wait for the programm to end.
  - Go back to the folder containing ADB and ABE. Right-click on the file backup.tar and open it with any compatible app (Linux users can open it using their default archiving app, others OSes needs a specific archiving programm to be installed. If you don't have one, download and install [7-zip](https://7-zip.org/)), but only open it, dont extract all the files. (with 7-zip, right-click on the file, 7-zip and finally open archive)
  - In the archive manager window to the "apps" folder, then go to the folder called with the same name as the app package name, then go to the folder called "r".
  - Select the files that ends with `.dat` (maybe there is 2 files, 3 or 4) and drag-n-drop them to the folder containing the ADB and ABE programms, wait for the archiving programm to decompress the file and close the programm.
  - ~~If you are on MacOS, you will have to use [WineBottler](https://winebottler.kronenberg.org/) to run the programm as a Windows programm (because I made a mistake lol). To install WineBottler, go to [their website](https://winebottler.kronenberg.org/) and download and install the version that suits for your MacOS X version. I recommend you [this tutorial](https://www.howtogeek.com/263211/how-to-run-windows-programs-on-a-mac-with-wine/). You dont have to install from WineBottler any apps like Internet Explorer.~~ Fixed since version 2.0 which detects the format and corrects it in the original format, meaning you can fix Android/Windows savefiles on MacOS/iOS with no problem, but you will only be able to use the savefiles under the same original OS, so fixing an Android/Windows savefile won't make you able to use the fixed savefiles under MacOS/iOS.
  - Go to the [Python 3.11.4 downloads](https://www.python.org/downloads/release/python-3114/) which is the latest Python version for now and is tested to be functionnal with my code, scroll down until you see the header "Files", then download and install the version that is right for you (if you dont know if your computer is 64bits or 32bits, choose the 32bits version). MacOS users will have to download the 64bits Windows version of [Python 3.8.9](https://www.python.org/downloads/release/python-389/) (not the Python 3.11.4 since it's not compatible with Wine !) and run it directly throught Wine (dont convert it to Mac `.app` file). Linux users does not have any Python installer on the Python website. Instead, open your package manager (either in graphical UI or in command line) and install the package `python3` and `python3-pip`. After, check the Python version by running the command `python3 --version` in a terminal (don't use `python3 -v` because some old Python versions understands that `-v` means `--verbose` instead of `--version`, if you do it you will get a Python interpreter with lots of weird logs texts for debugging Python, to exit type `exit()` and validate using the Enter key). If your Python version is 3.8 or newer (Python 3.9, 3.10, 3.11, etc...) it should work fine (programm testd on Python 3.8, 3.9 and 3.11). If you get an older version (example: Python 3.6) try to install in your package manager the package called `python3.8` or `python3.10` and then, instead of running the command `python3 --version`, run `[the name of the package you installed] --version` (example for package `python3.8`: `python3.8 --version`). And make sure its Python 3.8 or newer. If the command isn't found, you will have to compile Python yourself from the source code, but don't panic, its pretty easy if you [follow this tutorial](https://ubuntuhandbook.org/index.php/2021/10/compile-install-python-3-10-ubuntu/) (if the commands containing `apt` does not works, try replacing `apt` by `yum`, `pacman` or `dnf`, else try skipping these commands containing `apt` or search Google for annother tutorial, search `How to compile Python 3.10 on [your operating system name, example: Debian]`).
  - Go back to the same terminal and run the command `pip install pycryptodome` to install a needed library for the programm. MacOS users will have to run `wine py -m pip install pycryptodome` instead. If it fails, it's not important, just skip the command.
  - Download the first file you see that ends with `.py` in the [GitHub Releases](https://github.com/HGStyle/GD-SaveFileFixer/releases). Download the file in the folder that has all the stuff such as ADB and ABE programms.
  - If you are on Windows:
      - In the terminal, run the command: `dir /s /b *.dat`
      - In the folder containing all the stuff, run the programm you just downloaded (double-click on it)
      - Enter the option 1 of the programm
      - Follow the instructions given by the programm: add the paths that were given by the command in the terminal. You can use copy-paste, but add the paths 1 by 1 only ! When you are ready to fix it, enter nothing and it'll start.
  - If you are on MacOS:
      - In the terminal, run the command: `find "$(pwd)" -name "*.dat"`
      - Open annother terminal: [Click Finder, then services and finally "Open terminal at folder" (click to see screenshot)](https://www.maketecheasier.com/assets/uploads/2021/10/launch-any-folder-mac-terminal-new-terminal-at-folder-2.jpg) but keep the old terminal open
      - Run the command: `wine py [name of the python file you downloaded]`, usually the Python script file name is `GD-SaveFileFixer-SourceCode.py`.
      - Enter the option 1 of the programm
      - Follow the instructions given by the programm: add the paths that were given by the command in the terminal. You can use copy-paste, but add the paths 1 by 1 only ! When you are ready to fix it, enter nothing and it'll start.
  - If you are on Linux:
      - In the terminal, run the command: `find "$(pwd)" -name "*.dat"`
      - Open a new terminal: right-click in an empty space and click "Open terminal here". If the option isn't here, in the toolbar click "Tools" and then "Open terminal here"
      - Run the command: `python3 [name of the python file you downloaded]`, usually the Python script file name is `GD-SaveFileFixer-SourceCode.py`.
      - Enter the option 1 of the programm
      - Follow the instructions given by the programm: add the paths that were given by the command in the terminal. You can use copy-paste, but add the paths 1 by 1 only ! When you are ready to fix it, enter nothing and it'll start.
  - When the programm is done, open a file manager and go to your Android device, go to your internal memory of your device and copy the fixed files (not the files in the backup folder !) to your Android device. Make sure to move them at the root of the memory, not in a folder and not on your SD card. For all the next steps you won't need a computer.
  - Install the app [APK Extractor](https://play.google.com/store/apps/details?id=com.ext.ui) from the Play Store.
  - Open the app. Search for your Geometry Dash (or your GDPS, in case it's a GDPS)
  - Memorise the package name (which is usually formated like `aaa.bbbbbbb.cccccccccccc`). Since there is many steps, I recommend you to write it on a sticky note.
  - Click on the app to extract his APK. We'll need it later.
  - Do not uninstall APK Extractor since we'll need it later.
  - If the package name you memorised is `com.robtopx.geometryjumq` (notice the `q` at the end !):
      - Download and install [APK Editor Pro](https://dl.hgstyle.fr/Apps/AndroidHackerKit/APK_Editor/Clean/APK_Editor_Pro.apk)
      - Download the APK of Geometry Dash (but not the one used by GDPSes, and it should be version 2.111). I recommend using this one: [Download Geometry Dash 2.111 APK](https://dl.hgstyle.fr/Geometry_Dash_Versions/Geometry.Dash.ver.2.111.build.33.apk)
      - Open APK Editor Pro, alow storage access, click "Select Apk from App" and click on your Geometry Dash or your GDPS
      - Select "Full Edit" and then "Decode All Files", then go to "Files" in the toolbar of APK Editor Pro
      - Select the folder `assets` and `lib` and click "Extract", then go to your downloads folder and click "OK" (then wait for it ends and exit the app)
      - Make sure to exit the app completely and reopen it, now click "Select an Apk File" and click on the APK file of Geometry Dash 2.111 you downloaded (make sure the APK is stored in your internal storage, not in your SD card !)
      - Click "Full Edit" and then "Decode All Files" again and go to files
      - Select the folders `assets` and `lib` and click delete
      - Click the button with a plus symbol in a folder, and go to "Import Folder"
      - Click on the "..." button and browse into the `assets` folder in your downloads folder and click "OK"
      - A field will be filled automatically, be sure to see that the last word separated by the "/" is `assets` else click cancel and repeat the two last steps
      - Click "OK" and wait for it imports the folder `assets` into the APK
      - Again, click the button with a plus symbol in a folder, and go to "Import Folder"
      - Click on the "..." button and browse into the `lib` folder in your downloads folder and click "OK"
      - A field will be filled automatically, be sure to see that the last word separated by the "/" is `lib` else click cancel and repeat the two last steps
      - Click "OK" and wait for it imports the folder `assets` into the APK
      - Click on the "Build" button and wait for it builds the APK file
      - Open your file manager, go to internal storage, go to the folder "ApkEditor" (if you see multiple files, ignore those that aren't an APK) and move the APK file to the downloas folder in your internal storage
      - Optionally, you can delete the "ApkEditor" folder and/or the APK Editor Pro app
  - Download an install [App Cloner Pro](https://dl.hgstyle.fr/Apps/AndroidHackerKit/Other_apps/App_Cloner_Pro.apk)
  - Open App Cloner
  - If the package name you memorised is `com.robtopx.geometryjumq` (notice the `q` at the end !):
      - Click on the folder icon and click OK when a message box appears
      - Click the browse files logo
      - Open your downloads folder and click on the APK you just moved here
  - Else:
      - Search the Geometry Dash app (or your GDPS) and click on it
  - Scroll down and go to "Storage options"
  - Click on "Redirect external storage" and check the "Enable" box
  - Scroll down and enable "Acessible data directory"
  - Go back to main options categories
  - Scroll up and click on "Clone number" option
  - Check the box "Replace original app" and click "OK"
  - Click the button with the App Cloner logo on it, click "OK" and wait for it ends
  - When you can, click on the "Uninstall app" button (this will uninstall the Geometry Dash, but we got a backup of the data that we fixed so you won't lose anything)
  - Go to the "Cloned APKs" category and hold on the first of the two apps that seems the same, then stop holding
  - In the upper toolbar click the diskette logo and save the file to your downloads folder
  - Wait for the app to say "Successfully saved file" at the bottom of the app UI
  - Close the app and open your file manager
  - Go to your downloads folder by going to storage and then in the "Download" folder
  - Search for the APK made by App Cloner anc open it/click on it
  - It will normally show something like "Do you wanna install this app ?", so click "Install"
  - When its done, click "Open" to open the game, then close it
  - Download and install the latest version of [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk), then open the app and wait for the loading to finish. Dont use the Google Play Store version since it is no longer updated and broken. You will get a terminal like on Linux, but dont panic, I'll guide you !
  - Open the app when it's installed
  - You will have to allow the storage access since [its not enabled by default](https://wiki.termux.com/wiki/Termux-setup-storage). To do that, simply type `termux-setup-storage` and press enter. Now allow storage access and you are ready ! You can enter the next command when you see the dollar symbol back and waiting you for the next command.
  - If you are on Android 11 or later (or you dont know which version of Android you have), go to Settings (exit Termux, you can completely close it or not), Applications, Termux, Permissions, disable storage access and re-enable it. [This is due to an Android bug which cannot be fixed by the Termux community.](https://wiki.termux.com/wiki/Termux-setup-storage) Then go back to Termux.
  - Then browse to the Geometry Dash app memory by executing `cd /data/data/aaa.bbbbbbb.cccccccccccc` (replace `aaa.bbbbbbb.cccccccccccc` by the package name you memorized)
  - Remove the current savefiles by executing `rm -rf *.dat`
  - Move the fixed savefiles of your phone memory by running the command `mv /storage/emulated/0/*.dat ./` (dont forget the dots, else you may get permission error or inexistant path error)
  - Try opening Geometry Dash (or your GDPS), it should be fixed. BUT DONT QUIT THIS TUTORIAL OR YOU COULD GET HACKED.
  - Now we have a problem (not really since I have the solution): every app can access to the game data. Why is this a problem ? They can access your savefiles, so they can access your account, and even, your password. Almost no apps actually steal data from Geometry Dash since they normally can't, but no one knows. To fix this high security issue, go to your file manager, internal storage, then go to the folder called "ApkExtractor", then to the folder called with the same name as your Geometry Dash or GDPS app, then install the only APK in this folder. This will remove the App Cloner changes but not the savefiles changes.
  - Annother "problem": USB debugging is enabled so everyone that has your phone can backup data of any apps of your smartphone. To disable it:
    - Go back to settings menu, scroll down and you will have a new category called "Developers options": go into it.
    - WARNING: YOU SHOULD NOT MODIFY A SETTING WITHOUT KNOWING WHAT ARE YOU DOING ! PLAYING WITH THESE SETTINGS MAY MAKE YOUR DEVICE COMPLETELY UNUSABLE AND USELESS, AND YOU MAY LOSE ALL YOUR DATA !
    - Scroll down and disable USB Debugging
    - Close the Settings app
  - After this, you are 100% safe.
  - Now you can uninstall all the "temporary" apps we installed (ADB and ABE on the PC, APK Editor Pro, AppCloner and Termux on the phone)

If your Android device is rooted (its a very lot more fast):
  - Go to your browser to download the latest version of the Python programm. There is a binary for Android but I dont recommend it and it may be deleted in the future since Python installation in Termux (the app we'l use to launch the programm) is easy. Download it using [GitHub Releases](https://github.com/HGStyle/GD-SaveFileFixer/releases), download the first file ending with `.py` to your Downloads folder on your internal storage (not SD card ! if its on your SD card you will have to move it to your internal storage download folder).
  - Download and install the latest version of [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk), then open the app and wait for the loading to finish. Dont use the Google Play Store version since it is no longer updated and broken. You will get a terminal like on Linux, but dont panic, I'll guide you !
  - Open the app when it's installed
  - You will have to allow the storage access since [its not enabled by default](https://wiki.termux.com/wiki/Termux-setup-storage). To do that, simply type `termux-setup-storage` and press enter. Now allow storage access and you are ready ! You can enter the next command when you see the dollar symbol back and waiting you for the next command.
  - If you are on Android 11 or later (or you dont know which version of Android you have), go to Settings (exit Termux, you can completely close it or not), Applications, Termux, Permissions, disable storage access and re-enable it. [This is due to an Android bug which cannot be fixed by the Termux community.](https://wiki.termux.com/wiki/Termux-setup-storage) Then go back to Termux.
  - Now we'll update the Termux programms. Simply type `apt update`, then press enter. After, type `apt upgrade -y` and press enter. After, remove unnecesary software (its automatic and won't break anything) by typing `apt autoremove -y` and press enter. (from now I will no longer say "Press enter", but you will still have to do it after typing a command)
  - Now we will install Python. Simply type the command `apt install python3 python-pip -y` and wait. Notice that this can take up to some minutes, depending on your device and internet connection speed.
  - Now we need to install Python depencies. This can be done by simply running `python3 -m pip install pycryptodome`. If it fails, it's not really important, just skip this step like if it was done correctly.
  - Now you will have to naviguate to your download folder. Firstly, run the command `cd /storage/emulated/0` to go to your internal storage. Then type the command `dir` to list all the files and folders. Find your download folder name and run the command `cd [entire name of your download folder]`. It's usually `cd Download`.
  - Now, find the name of the Python script file. Run the command `find . -name "*.py"` (dont forget the dots). You will get the name of every file ending with `.py` (so, for almost every user, only one file: the actual Python script we need to run).
  - Now we need to get root access. To do this, we'll use st42's termux-sudo script:
      - Install the needed packages by running `pkg install ncurses-utils wget tsu`
      - Download the script by running `wget -O "sudo" "https://gitlab.com/st42/termux-sudo/-/raw/master/sudo?ref_type=heads"`
      - Run these 2 commands to install termux-sudo completely: `cat sudo > /data/data/com.termux/files/usr/bin/sudo` and then `chmod 700 /data/data/com.termux/files/usr/bin/sudo`
  - Run the Python script by doing `sudo python3 [python script full file name]`. It's usually `sudo python3 GD-SaveFileFixer-SourceCode.py`. If the Python script filename contains spaces, run `sudo python3 "[python script full file name]"` (dont forget the two `"`: one at the start, one at the end of the filename).
  - If the package name you memorised isn't `com.robtopx.geometryjump`, the second option won't work. That's why it is not recommended, use the recommended option 3 instead. (it should not be long)
  - Once the programm has done running (you see the `$` symbol of Termux), close Termux.
  - Try opening Geometry Dash (or your GDPS), it should be fixed.
  - You can uninstall the Termux app.

## Running on iOS or iPadOS

[READ THIS. You have to extract the game files, run the program ~~on MacOS (Windows won't work until I decide to update)~~ (working fine on any OS since version 2.0 but this doesn't convert the savefile to annother format!), use the manual option, select the savefiles one by one, fix them, but them back into the folder where you got them.](https://www.reddit.com/r/geometrydash/comments/1ak4ssz/tutorial_how_to_access_the_game_files_get_nongs/) (Maybe someday I'll try to make a tutorial about this)

As I said before, I dont own any iOS or iPadOS devices that are up to date, I can't install apps on them since they are way too old. But here is a way that will probably work that I haven't tested. Firstly, [jailbreak your iDevice, here is a list of tutorials depending on your iOS/iPadOS version and/or iPhone/iPad edition](https://www.idownloadblog.com/jailbreak/). You may (or not) also see these jailbreaking tools: [unc0ver](https://unc0ver.dev/), [checkra1n](https://checkra.in/), [palera1n](https://palera.in/), [Dopamine](https://ellekit.space/dopamine/), [Taurine](https://taurine.app/), [Odyssey](https://theodyssey.dev/), [Chimera](https://chimera.coolstar.org/), [Electra](https://www.coolstar.org/electra/), [H3lix](https://h3lix.tihmstar.net/), [Phoenix](https://phoenixpwn.com/), [EtasonJB](https://etasonjb.tihmstar.net/), [backr00m (french old tutorial)](https://gamergen.com/forums/tutos-membres-ios/backr00m-jailbreak-de-l-apple-tv4-tvos-10-2-2-a-11-1-t736325.html) etc... You can find many more on the Internet but be careful ! [Malwares exists on iOS and iPadOS !](https://www.howtogeek.com/447107/can-my-iphone-or-ipad-get-a-virus/). Then install [iSH](https://ish.app/) and the Python programm, open iSH, install Python, run the Python program and exit iSH and finally open Geometry Dash, It should be fixed. NOTE: I havn't tested this because as I said, I dont own any iDevice that can install apps ! (they are too old, Apple Store refuses to install apps on it).

## More info about savefile encoding/decoding

These pages were useful to me to encrypt/decrypt GD savefiles:

[Click here to see Savefiles page backup from a GD Wiki user](https://geometry-dash.fandom.com/wiki/User:XBZZZZALT#backup_of_useful_stuff_from_Save_Files_page)

[Click here to see GD Programming Docs about Savefiles](https://github.com/gd-programming/gd.docs/blob/main/docs/topics/localfiles_encrypt_decrypt.md)

## Credits and legality

Thanks to WEGFan because this would not exist without his GitHub repo. I dont see any license on his GitHub repo, but I credit him anyways, even if its not needed.
Note that **this is an entire rewrite**, actually what was **reused from WEGFan's code** is actually **one single line of code**. And some sentances of the README.md file. But that's all.
Edit: It seems like WEGFan has seen this repo, since he made a modification in his GitHub repo to redirect users from his archived repo to mine! Just thanks bro, I think I can license the software without having problems with him. (it's the first time a known gd coder does that so thx)

## Thanks you all!
