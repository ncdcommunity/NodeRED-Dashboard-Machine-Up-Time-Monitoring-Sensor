# NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor
A basic ncd.io dashboard for machine up time monitoring sensor.

Product info: https://ncd.io/blog/machine-up-time-monitoring-product-manual/

This project is a basic subflow developed by ncd based on Node-RED and the new Dashboard 2.0 module, which allows you to visualize the data provided by the “Machine Up Time Monitoring-Sensor” in an intuitive way.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/9877645e-6d23-4136-9783-f55c6bb11262)

For more information visit:
[ncd.io](https://ncd.io/)

## Subflow characteristics:

It allows to visualize the data in real time of the variables sent by the sensor:

- Digital Input Counter 1.
- Digital Input Uptimer 1.
- Digital Input Counter 2.
- Digital Input Uptimer 2.
- Digital Input Counter 3.
- Digital Input Uptimer 3.
- Accelerometer Counter.
- Accelerometer Uptimer.
- Magnetometer Counter.
- Magnetometer Uptimer.
- Current value.
- Current value History.
- Battery Level.
- Battery Level History.

It is possible to view the relevant sensor data in a "Data" tab.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/4ace4531-8b2e-4a90-8c5e-a37a3e2ae1f4)

> [!IMPORTANT]
> This Subflow only works with type sensors (“sensor_type”: 108) which corresponds to Machine Up Time Monitoring.​

## Requirements/Dependencies:

To import this subflow it is necessary to have previously installed:

- Node-RED 
- @ncd-io/node-red-enterprise-sensors 
- @flowfuse/node-red-dashboard 

## Install "ncd-io/node-red-enterprise-sensors":

Within your Node-RED instance go to the main menu (top right) and select the "Manage palette" option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/48c0b0a3-9a63-4cde-9103-54501e2bb6e2)

In the window, select the "Install" tab:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/a9a9421f-4a99-4dd4-b15f-0f5f0a6707c9)


In the search field enter "@ncd" you will see the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/625eecf4-8d6b-463d-9671-9999e45142a6)

Click the "Install" button to start the installation process, a window will appear at the top of the screen, asking you to confirm the installation:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/9c540c5e-6f01-478c-9ce0-8d5975d9344c)

Once the process is completed you will see the following window:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/079747b8-a929-433d-ae95-407424349af5)

## For installing Dashboard 2.0:

FlowFuse's Node-RED Dashboard 2.0 is available in the Node-RED Palette Manager. To install it:

Open the menu in the top-right of Node-RED 
- Click "Manage Palette" 
- Switch to the "Install" tab 
- Search node-red-dashboard 
- Install the @flowfuse/node-red-dashboard package (not node-red/node-red-dashboard) 

Source: https://dashboard.flowfuse.com/getting-started.html

## Procedure to import Sub-flow:

### Step 1 - Copy JSON 
Copy the raw JSON file "/MachineUpTimeMonitoring.json" from this repository.

--- insert imagen ---

### Step 2 - Import nodes
Go to Node-RED, you can add a new flow in the node editor of node-red (optional):

Then, go to the main menu, select the “Import” option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/95c00480-0223-4feb-a9ff-f4add5bace90)

A field will be opened. Right click and paste the JSON code you just copied from GitHub:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/43b17109-6285-4689-875e-5beeb19b58a2)

You will see the JSON code, now you can press the red “Import” button at the bottom right (by default the “current flow” option is selected):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/deb03eef-2e70-4123-a889-2ea530a27c65)

In the upper part of the node editor, you will see information of the subflow you just imported, and automatically you will have the subflow available inside the node editor, now you can position it inside the editor by left clicking:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/af4cc512-ca67-49fe-853c-6a180234cfe6)

You may also notice that the subflow has been added to the **ncd.io** node group.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/bef6ba42-60e8-44e0-acbb-879c3ecde22b)

### Step 3 - Configure NCD.io nodes

The next step is to configure your **ncd.io** nodes (you may have already configured your nodes), but it is important to remember that this procedure only works for the “108 - Machine Uptime Monitor” type:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/9e6d0bae-e719-4ca1-8051-80360477e072)

Once you have the Machine Uptime Monitor sensor configured, the next step is to connect the sensor output (node) to the subflow input:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/dc47bf6c-164d-4d9c-944a-977b7b1131ca)

If you double left click on the subflow you can open the settings:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/f10fca07-7bed-4fcd-b98e-7fcb53bfc59a)

**Name:** you can assign an identifier to the subflow, and this will only serve to identify your specific flow within the node editor (to differentiate it from other nodes).

### Step 4 - Check your Dashboard

The next step is to go to your Dashboard to see the real time data coming from the sensor by clicking on the Dashboard 2.0 option in the sidebar:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/9b911300-3e59-495f-8c9e-ccd4b509d2e3)

> [!NOTE]
> In case you have deployed and cannot see the “Dashboard 2.0” content, you should reload the current page of the web browser with the “F5” key or “Reload page”.
> 
> ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/794f5fcd-6f15-4784-b607-d1c45f310091)

Then click on the **“Open Dashboard”** option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/c9f53ec3-d0aa-40ac-a157-2c11604f0616)

Your Dashboard will automatically open in a new window, where you can see something like this (depending on sensor configuration):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/5717dd71-6ee8-4bbf-8f7e-b379a8f30a29)


## ncd.io Dashboard Features

### The Main Menu

The main menu: where you can navigate between the tabs (Machine Up Time Monitor sensor and data).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/76fa488e-8675-459a-89ac-655d8397ccab)

### Gauges and Graphs

#### - You can display the counter and uptimer data individually by type of probe (**Digital Inputs, Accelerometer and Magnetometer**). 

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/4c3ce108-bb72-482e-a167-ba5c792adc19)

#### - A battery level and electric current indicator is also incorporated.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/824e99b8-3e0a-4647-abb9-abb2620ae9dc)

#### - As well as historical data for the electric current and battery level variables.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/dab86823-8ef8-4537-bba1-e808a470f655)

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/0e1cb03e-6aa5-4bbd-b22f-fc44202985cc)

## Layout

It is possible that the distribution of the indicators inside the dashboar is different depending on the size of your monitor, it is possible to adjust to a better distributed view by adjusting the zoom of the web browser.

For example:

### 1.- With a large monitor/screen:
It is possible that if you open the dashboard on a large monitor, you will see something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/70b4c725-fb03-48cc-b70d-a068cb55494a)

This works, but you may want a better distribution of the dashboard elements (as shown in the dashboard image at the beginning of this post) to do this just adjust the zoom of the web browser window, in this case increase the zoom, until you have the right distribution:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/9f1ca4f5-8c64-48f1-a0f7-3e93836f5171)

### 2.- With a smaller monitor/screen: 
It is possible that if you open the dashboard on a computer with a small screen/monitor (such as a laptop), you will see something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/5e3686e9-5c7e-4b56-9340-39bc1fd31a2e)

Where you will have to scroll to navigate between the dashboard elements, this works, but you may want a better distribution of the dashboard elements (as shown in the dashboard image at the beginning of this post) just adjust the zoom of the web browser window, in this case reduce the zoom, until you have the right distribution:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/95ebe77a-4d3f-492b-bb39-9b5d4637cf43)

## Possible errors during subflow import

If you import the flow without having previously installed Dashboard 2, you will get a message like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/fa895ce1-df3a-40ee-aac2-650297891756)

So you must delete the subflow and install the module **“@flowfuse/node-red-dashboard”** as mentioned at the beginning, and repeat the process. To delete the subflow you must double-click on the subflow in the Node-RED node editor to open its properties:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/cd045a99-7b54-4ae4-bbfa-0c011023be02)

Then click on the “Delete” button at the top of the window.

## Conclusion

For more information visit:
[ncd.io](https://ncd.io/)

