# CognitiveIoT Reference Architecture + simple example
This repository contains samples for a fast-track deployment of the Edge part of an IoT system based on NodeRED. It is part of an overall tutorial which can be found [HERE](https://ibm.biz/CognitiveIoT). This repository is used in the fast-track recipe which can be found [HERE](https://developer.ibm.com/recipes/tutorials/realtime-anomaly-detection-on-the-iot-edge-using-nodered-and-moving-zscore/). Those are the steps:

* Deploying NodeRED to the cloud
* Starting the test data generator
* Stream data into a NoSQL database
* Analyze it using ApacheSparkSQL
* Update the model on the Edge
* Finally, implement an Edge based Anomaly Detector using moving zscore

---

# Journey

Follow the fast-trakc recipe instructions [HERE](https://developer.ibm.com/recipes/tutorials/realtime-anomaly-detection-on-the-iot-edge-using-nodered-and-moving-zscore/) first. Afterward, you need to wire up the Watson IoT platform to your simulated device.

1) Go to the menu in Bluemix console
2) Select Apps
3) Select Dashboard
4) Select your App's Name (not route) (CognitiveIoT-<timestamp>)
5) Under "connections", select "cognitive-iot-iotf-service"
6) Under the "Welcome to Watson IoT Platform" text, click "Launch"
7) On the WIoT page, Click the microchip icon on the left-hand side. It is labeled "Devices"
8) Click the "+ Add Device" button on the right side.
9) Click the "Create device type" button.
9) Click the "Create device type" button on the next dialog as well.
10) On the "general information" dialog, enter the name "RemoteDevice", and click the "Next" button.
11) Let's skip this page, but this is where you'd fill in metadata about an actual physical device. Click "next".
12) Click "Next" again, then "Create"

Now that your device type is created, you will create a device.

13) Select "RemoteDevice" in the dropdown under "Add Device", and click the "Next" button.
14) For Device ID, put "VoltageSensor01". This matches details under the ibmiot out node in Node-RED, which you can investigate by double-clicking the node.
15) Continue to click the "Next" button, until you get to the Summary view, and then click "Add".
16) You will now have a view of details about your VoltageSensor01 device. Scroll down to "Recent Events" and you should see voltage events occurring continuously. Under "Sensor Information", you can see the most recent data being received, including voltage, frequency, count, and timestamp ('ts'). Click the 'x' to the upper-right to close this view.
17) On the upper-left, click the menu item called "Boards".
18) Click the "Device-Centric Analytics" board. You'll now see cards representing much of the same info we saw in the device details. However, this view is a dashboard to easily allow seeing multiple devices at the same time, and you could create additional cards to display further analytics.

This completes our journey...

----

# Deploy to Bluemix

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/rattboi/CognitiveIoT.git)

----

### License
-----------------------

The project is shipped with Apache License and refer to the [License file](https://github.com/romeokienzler/CognitiveIoT/blob/master/LICENSE) for more information about the licensing.

