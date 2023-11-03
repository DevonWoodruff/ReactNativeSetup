# Lab Assignment 1: Spinning Up React Native App

## System Requirements
**CPU**: 12th Gen Intel(R) Core(TM) i5-12600K   3.69 GHz
**RAM**: 16GB
**Windows Version**: Windows 10 Pro

## Installation Instructions
* Download and install Android Studio (use default setup settings). [2]
* Download and install Node.js (use default setup settings but don't install chocolatey).

## Configuration Steps
1. Open Android Studio then click "More Actions" --> "SDK Manager".
2. Tick the "Show Package Details" button on the bottom right, then find Android 13.0 ("Tiramisu") and tick **Android SDK Platform 33** and **Intel x86 Atom_64 System Image** then click apply and install.
3. Switch to the "SDK Tools" tab and tick the "Show Package Details" button again then tick **33.0.0** and install it.
4. Go to your Windows Control Panel --> User Accounts --> User Accounts (again) --> Change my environment variables --> New --> then enter ANDROID_HOME as the variable name and the location of your SDK folder as the variable value. You can find the SDK location by searching **%LOCALAPPDATA%\Android\Sdk** in your start menu search bar.
5. Open Windows PowerShell and enter **Get-ChildItem -Path Env:\\** to check that your ANDROID_HOME has been added successfully. 
6. Return to Change my environment variables then click on **"Path"** and select Edit... --> New --> then paste **%LOCALAPPDATA%\Android\Sdk\platform-tools** --> Click Ok. [2]

## Project Creation
1. Open up a command prompt by running **CMD** as administrator in your windows search bar then enter **npm uninstall -g react-native-cli @react-native-community/cli** if you've previously installed a global react-native-cli package, then enter **npx react-native@latest init AwesomeProject** (you can change "AwesomeProject" to whatever you want your project to be called. Wait for the project to finish setting up before the next step.
2. Go to Android Studio and open an existing project, then find your project from the file explorer (you can find out where you project is located by checking the command prompt that you used to create your project) and open the file with the Android logo (it will take time to load the project).
3. Create a virtual device to open your project with by opening the device manager tab and click the "Create Device" button. Select a device you'd like to use then press "Next" and download the "Tiramisu" with the API level 33 by clicking the download button next to it. Go to the next page and name the Android Virtual Device or leave it as is and click "Finish". [2]

## Running The Project
1. In Android Studio, click the "Build" tab and select "Make Project", this will take a while to complete.
2. Click "Run", then Run 'app'. If you haven't already selected your target device, do so now.
3. Once everything is finished loading and your Android Virtual Device is open, you will notice errors on the phone screen. Go to the location of your project folder and type "cmd" in the folder address bar to open a command prompt that points to your project folder.
4. Type "npm run start" then when prompted, type "r". Once it finishes loading you should see the React Native screen on your Android Virtual Device. [2]

## Troubleshooting
* Always make sure you're targeting the correct folders when using the command prompt, otherwise you will get errors when running commands.
* Be patient with the Android Virtual Device when it's booting up, if you try to turn it off and on while its loading you may cause it to freeze and will require you to restart Android Studio to fix.
* If you encounter an error running your project through the command prompt that resembles: "error listen EADDRINUSE: address already in use", follow this troubleshooting guide: https://medium.com/@antonrosh/address-already-in-use-a-simple-guide-to-freeing-up-ports-fbc6a3822983 [1]
* Be sure to save your project files somewhere on your computer where you have full permissions otherwise you may encounter problems with modifying it in the future.

## Resources
[1] A. Rosh.  (May 26th). “Address Already in Use”: A Simple Guide to Freeing Up Ports [Online]. Available: https://medium.com/@antonrosh/address-already-in-use-a-simple-guide-to-freeing-up-ports-fbc6a3822983
[2] React Native. (Aug 29, 2023). Setting up the development environment [Online]. Available: https://reactnative.dev/docs/environment-setup?guide=native
