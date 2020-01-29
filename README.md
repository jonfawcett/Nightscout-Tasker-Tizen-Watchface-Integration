# Display Nightscout Data on Samsung Galaxy and Android Wear

![alt text](https://github.com/jonfawcett/Nightscout-Tasker-Tizen-Watchface-Integration/blob/master/Watch%20Faces/Images/Loop%20Gradient%20Rings.png)

This will give you the instructions to setup watchfaces using tasker to pull directly from Nightscout and send the data to watchmaker for your Samsung watch. This should work for any combination of Android Phone and Samsung or Android Wear watch. If will not work with iPhones or with other watches or fitness bands. [The instructions are all in the Wiki](https://github.com/jonfawcett/Nightscout-Tasker-Tizen-Watchface-Integration/wiki).

I designed this to pull all BG and Loop data and have only tested it with mg/dl. Some of the math, text sizes, etc may need changed for mmol. Head over to the wiki for setup instructions and also how to edit the watchfaces if you are not a Loop user.

## Primary Functionality

**- BG readings**

   Pull the latest BG reading from Nightscout

**- Delta**

   Pull the latest delta (change from last reading to current reading). This is pulled into 2 variables: with +/- and also without the symbol so that it can be used in some of the math calculations.

**- Direction**

   It sets a variable for both the actual arrow character as well as the text name of the direction. Some watch faces use the arrow characters directly, but some fonts add a large gap for double arrows. My newer watch faces use images for the arrows with logic in the watch face for rotation and display based on the direction text.

**- Time since last reading**

   Each reading pulls the timestamp and the watchfaces do on-watch calculations for "minutes ago" to be displayed
   
**- BG Graph**

  The task pulls the last 20 readings to use on graph watch faces. All math for location and color is performed on-watch for each update.
  
## Loop Specific Functionality

**- IOB**

   The current Insulin on Board

**- COB**

   The current Carbs on Board
   
**- Override**

   The name of the current override that is set. If no override is set, it displays ~
   
**- Battery**

   This is the remote uploader battery %
   
**- 30 Minute Prediction

   This pulls Loop's predicted Bg for the 7th reading out, which is 30 minutes.
   
**- Temp Basal**

   If there is a currently enacted temp basal, this will be set.
   



Special Thanks to Fred for help with the main details of the setup. His method can be used locally with Xdrip if you prefer to not use data.

https://github.com/wagnefrede/xDrip-and-AAPS-Notifications-for-TiZENOS-WEAROS-Watchfaces-Tasker-AutoNotification-Watchmaker/tree/master/Tasker%20Permissions/Tasker%20Permissions
