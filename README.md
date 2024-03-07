# NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor
A basic ncd.io dashboard for machine up time monitoring sensor.

Product info: https://ncd.io/blog/machine-up-time-monitoring-product-manual/

This project is a basic subflow developed by **ncd** based on Node-RED and the new Dashboard 2.0 module, which allows you to visualize the data provided by the “Machine Up Time Monitoring Sensor” in an intuitive way.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/ba210754-5960-4b7d-b327-dd3cfb97787a)

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

It is possible to view the relevant sensor data.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/dbef2a5a-632a-468d-a5d4-208ecafdbea9)

> [!IMPORTANT]
> This Subflow only works with type sensors (“sensor_type”: 108) which corresponds to **Machine Up Time Monitoring**.​


## Requirements/Dependencies:

To import this subflow it is necessary to have previously installed:

- Node-RED development tool.
- @ncd-io/node-red-enterprise-sensors npm
- @flowfuse/node-red-dashboard npm


## Install "ncd-io/node-red-enterprise-sensors":

Within your Node-RED instance go to the main menu (top right) and select the **"Manage palette"** option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/48c0b0a3-9a63-4cde-9103-54501e2bb6e2)

In the window, select the **"Install"** tab:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/a9a9421f-4a99-4dd4-b15f-0f5f0a6707c9)

In the search field enter **"@ncd-io/node-red-enterprise-sensors"** you will see the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/625eecf4-8d6b-463d-9671-9999e45142a6)

Click the **"Install"** button to start the installation process, a window will appear at the top of the screen, asking you to confirm the installation:

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
Copy the raw JSON file **"node-red/Machine-Up-Time-Monitor-Dashboard.json"** from this repository: 

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/be5f26c8-61fb-4f97-8400-52ea46c8c77c)

### Step 2 - Import nodes
Go to Node-RED, you can add a new flow in the node editor of node-red (optional):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/32c4b072-d7af-4626-8a69-7d08e1c004d4)


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

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/32aef3f8-a649-4bee-997e-63133654351b)

Your Dashboard will automatically open in a new window, where you can see something like this (depending on sensor configuration):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/8984197c-db2c-4f67-a928-d3d806ff4b56)


## ncd.io Dashboard Features

### The Main Menu

You can navigate between the ui-pages (this menu allows you to navigate between two or more ncd-dashboards, in case you have configured different ncd-dashboards):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/84b1190d-62b3-4426-9b26-237bd2b86ddf)

> [!NOTE]
> For example if you have configured an ncd-uptime-dashboard and you import an ncd-environment-dashboard, you will be able to navigate between the subflows from the main menu:
>
> ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/047ab0ea-b04b-4ea2-987d-998b7a5f7f00)

A step-by-step configuration for importing two or more ncd-dashboard subflows and accessing them from the main menu is presented later in this post.

### Gauges and Graphs

#### - You can display the counter and uptimer data individually by type of probe (**Digital Inputs, Accelerometer and Magnetometer**). 

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/e8e88de0-37ce-460c-91f8-987030c47932)

#### - A battery level and electric current indicator is also incorporated.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/9bafcc4e-402d-481c-8cc2-8e2ee253de7e)

#### - Historical data for the electric current and battery level variables.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/ca50f6cc-d33e-4a3d-bbfe-36dbb627d27f)

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/e2fbfd8d-edcd-49be-a0ae-e0e5f558e83d)

## Inspect Button

By pressing this button it is possible to access the information received from the sensor (Payload, NodeID, Firmware version, battery voltage, sensor type, MAC address, etc.), if pressed again it returns to the graphs and indicators view.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/467eb689-c6b2-47df-9dbc-6c8c3203fb0b)


## Layout

It is possible that the distribution of the indicators inside the ncd-dashboar is different depending on the size of your monitor, it is possible to adjust to a better distributed view by adjusting the zoom of the web browser.

For example:

### 1.- With a large monitor/screen:
It is possible that if you open the dashboard on a large monitor, you will see something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/b6e6ba54-ca34-4330-b27c-5e476707973b)

This works, but you may want a better distribution of the dashboard elements (as shown in the dashboard image at the beginning of this post) to do this just adjust the zoom of the web browser window, in this case increase the zoom, until you have the right distribution:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/4c12cb6f-a03c-4a3b-9ac4-147e95687824)

### 2.- With a smaller monitor/screen: 
It is possible that if you open the dashboard on a computer with a small screen/monitor (such as a laptop), you will see something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/c5d292e1-c46d-4bc1-8d4d-97dada133e6e)

Where you will have to scroll to navigate between the dashboard elements, this works, but you may want a better distribution of the dashboard elements (as shown in the dashboard image at the beginning of this post) just adjust the zoom of the web browser window, in this case reduce the zoom, until you have the right distribution:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/117f541c-c02c-4304-90ff-186020a91acd)

## Working with two or more ncd-dashboards in the same Node-RED project

This instructions refers to the scenario where you have previously installed and configured an ncd-dashboard (subflow) and you want to import another ncd-dashboard (subflow) to the same project.

The procedure is the same as mentioned above, with the simple difference that as soon as you press the import button in the "Import nodes" window you will see the following message at the top of our Node-RED flow editor:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/8abe29b2-d7d0-4da9-b287-e685ba079da3)

This indicates that you are importing a subflow that contains one or more nodes that already exist in your current project (workspace). Specifically it refers to the configuration node **"ncd-ui-base"** which represents the base configuration of all our **ncd-dashboards**, simply click on the **"Import copy"** option. This shows us the detail of the elements that were imported in our project.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/c566a6b4-4e49-40a7-8920-9091c5cd5101)

If everything is correct, the next step is to deploy in order to apply and execute the changes in our project, using the "Deploy" button:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/c8b74a91-3a0b-43b8-a917-8d8c431cff0d)

Now, if you go to the "Dashboard 2.0" tab and click on "Open Dashboard" or simply refresh the dashboard browser tab, you will see in the main dashboard menu the new imported ncd dashboard:

View from ncd-uptime-dashboard ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/451bbf16-f06a-460b-9c46-b461bc7c196b)

View from ncd-environment-dashboard ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/719f0e88-0a59-4bd2-84ea-1893bec02e8f)

## Import subflow to an existent dashboard 2.0 project.

This procedure refers to the scenario where you already have a dashboard 2.0 configured and you want to import an ncd-dashboard within the same Node-RED project.
For example, if you already have a dashboad 2.0 configured with some elements, in the dashboard you would have something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/5865af41-5428-4ce6-9b63-f61dadca3fe9)

To import an ncd-dashboard to your existing project you use the same steps mentioned above; copy the JSON file from the GitHub repository, use the import window (or Key shortcut Ctrl-i), paste the JSON and click on import, the imported elements will be shown at the top, but if you deploy inside the dashboard 2.0 you will have the following message:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/ee377bea-d286-4ea9-af17-e95aa8415ca9)

To solve this you must return to the Node-RED flow editor, go to the "dashboard 2.0" tab and inside "Layout" you will be able to see something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/8d979d71-a12d-43ab-9165-5a89fcf1291a)

You can identify the ui-pages of the ncd-dashboard by the fact that they are preceded by "ncd".

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/7ab69877-7c68-4071-8a02-5bb6a3b0e357)

Next to the "Your Page Name" identifier, if you hover the cursor you will see the "Edit" button, click on it:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/6825f1e7-9a30-4d3e-b5cc-1af3205d13a9)

This opens the page configuration window, in the UI property you will click on the "Edit" (pencil icon).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/d6e9c47b-23b2-4adf-be52-219c7bf00562)

Now the configuration window of the "ui-base" configuration node opens, you should click on the "Delete" button (located in the upper left part of the window):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/63effc99-e982-4b75-8f7b-e16ae42953e3)

Automatically it returns to the ui-page window, and it shows us the box of the property "UI" with the outline in red color:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/aa4c2327-e507-4fd6-8f0f-dae368ac8328)

Click on the arrow and then select the property "ncd-ui-base[/dashboard]":

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/3b6a12c3-d9a3-4786-b20a-9ee18fd37c2c)

Finally click on the "Update" button at the top right of the window:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/0ae58d18-67f4-4a69-b0c1-d7e1cba9f27d)

>[!NOTE]
>this same procedure must be done if you have two or more pages previously configured in dashboard 2.0.

Now click on deploy button to apply the changes made to the project:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/31f73feb-300e-4b08-8616-7c7b23c13920)

Go to the "Dashboard 2.0" tab and click on the "Open Dashboard" button:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/beb9679a-b433-438d-9519-2f8d693812c9)

You will notice that the ncd-dashboard identifier has been added to the dashboard 2.0 main menu:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/c8c512d3-7bb9-4a7a-a1e3-010ac1f0b8c7)


## Possible drawbacks during subflow import 

### 1.- Import subflow without dependencies installed

If you import the flow without having previously installed Dashboard 2, you will get a message like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/fa895ce1-df3a-40ee-aac2-650297891756)

So you must delete the subflow and install the module **“@flowfuse/node-red-dashboard”** as mentioned at the beginning, and repeat the process. To delete the subflow you must double-click on the subflow in the Node-RED node editor to open its properties, then click on the “Delete” button at the top of the window.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/d84cbca8-c32d-4726-8dc6-9948cea52491)

You must also delete the subflow node from the node palette in the "NCD" or "Sublows" group, double click on the node.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/e679d4a4-d758-423f-a388-dc93f6af50cf)

This opens the subflow window, at the top click on the "delete subflow" button:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/822f59d2-6733-4272-a66b-054a5dc6fa2d)


### 2.- Import the same subflow twice / delete subflow.

In case by mistake or by some procedure you have imported twice the same subflow, or you simply want to remove an ncd-dashboard subflow from the nodes palette, you must follow this quite simple procedure.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/022f60e9-f435-4ed6-a3c2-c7d728e3dd90)

- 1.- Double click on the subflow node you wish to delete, the ncd-dashboard subflows are located in the node palette within the NCD group. 
- 2.- Once the "Edit subflow template" tab opens at the top, click on the "delete subflow" button. 

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/31be9aff-c818-4481-aea9-5a975afd4595)

This completely removes the subflow, as well as the associated configuration nodes, you will notice that it no longer appears in the nodes palette.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/6f23509b-c251-4cd2-852a-5a0f7a5948b1)

Do not forget to deploy in order to save and apply the changes made to your project.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Machine-Up-Time-Monitoring-Sensor/assets/159818736/05220fd5-758c-4d86-a254-bc012eaf8240)



For more information visit:
[ncd.io](https://ncd.io/) | [Machine Up Time Monitoring Product Manual](https://ncd.io/blog/machine-up-time-monitoring-product-manual/)

