# Ship IoT with Kinoma Create and PubNub

This demonstrates reading a Texas Instruments LM35 precision
temperature sensor with a Kinoma Create, and sending the
data to an exchange on PubNub.

## Usage

Setup instructions: IMPORTANT! You must set the pins before every time you start the app! If the app crashes, you should check the pins again before re-launching it!

### Connect the temperature probe

1. Connect the LM35 to the left-most pins on the front
2. The flat face of the TO-92 case should face you and the screen

### Set the pins

1. From the Kinoma launcher, select the Front Pins app
2. Make sure the switch for the left block of pins is set to 3.3v
3. Tap on the left block of pins to open it up
4. Tap on pin 51, and select Power
5. Tap on pin 52, and select Analog
6. Tap on pin 53, and select Ground
7. Tap on the back arrow, in the upper-left of the screen
8. Tap the Apply button, and then the Apply button again
9. The temperature probe should now be powered; check with a meter

### Load the app to the Kinoma

1. Open Kinoma Studio
2. File -> Import... -> General -> Existing Projects into Workspace; then hit Next
3. Select shipiot-kinoma-create-pubnub as root directory, click Finish
4. Edit the src -> main.xml file and put in your PubNub keys
5. In Project Explorer, open shipiot-kinoma-create -> src -> application.xml
6. Make sure your hardware Kinoma device appears (must be on the network and running)
7. Click the little gear for the hardware Kinoma
8. Check the box "Install on Launch"
9. Click Apply, and then Run
10. The app should be uploaded to the Kinoma
11. Click Stop in Kinoma Studio to stop the local debug session

### Notes

* The trouble with the LM35 directly in the Kinoma pin header is that the Kinoma dissipates enough heat to keep the sensor at about body temperature. This makes it hard to demo the temperature changing much by touching or breathing on the sensor.
* Use a short cable if you have it handy. A long cable may cause instability or oscillation; be careful.

## License

Copyright (c) 2015 wot.io, Inc. All Rights Reserved.

by Aaron Kondziela

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

The wot.io logo and name are trademarks of wot.io, Inc.

The pubnub.js library is Copyright 2011-2014 Marvell Semiconductor, Inc.