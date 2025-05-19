# simple-esp32-os
A simple, customizable operating system for ESP32 + OLED. Features navigation, settings, and app structure.

If you wanna add new apps you just need to increase the "appsAmount" variable and then also in the "appNames" variable you should add the name of the App.
For the icon you need to add bitmap data and for the logo it is 48x48 and the should be something like this "1,0,0,0,1,1" and the icon data should be in a variable for example "settingsIcon[] = {1,0,0,0,1,1...}" and then you would also need to put the icon data variable into the "appIcons[]" variable.
And last step would be to make the function for the app, that can be done by goin into the appOpen() function and then add if(openedApp == (your app number)) and then here the function for the app
