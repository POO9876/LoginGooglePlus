LoginWithGooglePlusAccount
==========================

Google+ sign-in lets users sign in to your Android app with their existing Google account and get their profile information like name, email, profile pic and other details. By integrating google plus login in your apps, you can get all the user details in one shot. Not only login, you can do other things like posting to their g+ account, getting list of circles, friends list and lot more. The major advantage of integrating G+ login is, you can drive more users to your app by providing quicker & easiest way of registration process.


Enabling G+ API on google console
In order to consume google plus services, first we need to enable the Google Plus API on google console and we need to register our digitally signed .apk file’s public certificate in the Google APIs Console.

Java keytool can be used to generate SHA-1 fingerprint. Open your terminal and execute the following command to generate SHA-1 fingerprint. If it ask for password, type android and press enter.

On windows
keytool -list -v -keystore "%USERPROFILE%\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android

On Linux or Mac OS
keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android

Open Google APIs consoleOn the left, under APIs & auth section, click on APIs and on the right enable Google+ API service


Now again on the left, click on Credentials and on the right, click on CREATE NEW CLIENT ID button. It will open a popup to configure a new client id.

In the popup, select Installed application as Application type.

Under Installed application type section select Android and give your project package name. This package name should be equal to your android project. I gave my package name as info.androidhive.gpluslogin

Enter your SHA1 fingerprint in Signing certificate fingerprint (SHA1) field.

Enable Deep Linking and click on Create Client ID button. Now you should see a new client created for your android application.

we need to import the play services library into Eclipse workspace. Then add the projects with your own project
