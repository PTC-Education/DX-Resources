# Using Vuforia Spatial Toolbox with Kepware to Connect to Allen-Bradley PLCs
 
## Hardware Needed: ### 
 - An Allen Bradley PLC (This tutorial was written and tested with two Allen-Bradley PLCs, a [Micro850](https://literature.rockwellautomation.com/idc/groups/literature/documents/um/2080-um002_-en-e.pdf ) and a [CompactLogix5480](https://literature.rockwellautomation.com/idc/groups/literature/documents/um/5069-um002_-en-p.pdf).)
 - An Ethernet Cable  
 - Windows Computer (This tutorial and testing utilized an Intel NUC)  

## Setting up the PLC 

###Micro850 
Install [Connected Components Workbench (CCW)](https://compatibility.rockwellautomation.com/Pages/MultiProductFindDownloads.aspx?crumb=112&refSoft=1&toggleState=&versions=57681), following [these instructions](https://www.youtube.com/watch?v=BU7O8KXfdPA&ab_channel=TimWilborne) from 2:39-8min to configure the PLC with CCW. 

###CompactLogix5480
For the CompactLogix5480, install Rockwell Automation Studio 5000 Logix Designer. We used [these lessons](https://twcontrols.com/lessons/how-to-connect-to-an-allen-bradley-controllogix-plc-over-ethernet-with-studio-5000-and-rslinx) to connect to and configure our CompactLogix5480.

### Test with a simple program

Once your device is connected anad you can create a program, make a simple "Hello World" that will activate some of outputs on the PLC. A possible demo could be to use the Timer (TON) within CCW to turn your outputs on and off repeatedly. Here's an example: 
 - [This video shows the process of using the TON with CCW](https://www.youtube.com/watch?v=CI7o78YogGw&ab_channel=InsightsInAutomation).
 - [This PDF shows the ladder logic](https://github.com/PTC-Academic/DX-Resources/blob/master/Curriculum_Resources/DX-Exercises/Resources/Traffic-Light-Demo-withWalk.pdf) for a graffic light demo made in Studio 5000 Logix Designer.

### Setting up Networking

This project used the ethernet (wired) port to create a local network to communicate to the PLC, and leveraged the wireless network for outbound/internet communications. 
- For the wireless connection, a static or dynammic IP will work. 
- For the wired connection, we gave the computer a static ethernet IP Address: 192.168.0.1; Subnet Mask: 255.255.255.0; Default Gateway and Primary DNS were set to match the gateway and DNS for the wireless connection.

###Set the Micro850 IP address 
Click on the `Micro850` tab in CCW and select `Ethernet` on the bottom right. Once selected, scroll down on the right side and select “Configure IP address and settings” underneath **Internet Protocol (IP) Settings**.  
 - Adjust the IP to your settings. For us, we set the IP Address to 192.168.0.2, the Subnet Mask to 255.255.255.0, and the Gateway Address to 192.168.0.1 

###Set the CompactLogix5480 IP address 
For the CompactLogix5480, we used RSLinx to set the Ethernet IP Address to 192.168.0.2, the Subnet Mask to 255.255.255.0, and the Gateway Address to 192.168.0.1 per the instructions in the CompactLogix5480 user manual.

**To verify that the PLC should is connected to your Windows Computer, [ping](https://en.wikipedia.org/wiki/Ping_(networking_utility)) the IP address from the command prompt on the computer with ping 192.168.0.2, if the response is some number of ms, they are connected.

## Connecting the PLC to Kepware 

[Download KEPServerEX](https://www.kepware.com/en-us/content-gates/ex-demo-download-content-gate/?product=d2239b8c-36f2-4d07-8fbd-e223d0e26bbf&gate=8a5e8dd5-6edf-4d68-aa36-72f97b11e612) -- this is a free trial, but is fully functional; KEPServerEX will run for 2 hours at a time, then it needs to be restarted. Note, this product is also called "ThingWorx Indsutrical Connectivity".
<br />
[Download Java](https://java.com/en/download/manual.jsp)

Once you open Kepware, you can right click "Connectivity" and add a new Channel:
<br />
<img src="https://github.com/PTC-Academic/DX-Resources/blob/master/images/VST-PLC-image001.png" alt="Adding a new Channel on Kepware" width="300">

[THIS](https://www.youtube.com/watch?v=KRFA9YutiUs&ab_channel=LearnWithPro-Tutorial ) video walks through the next few steps of the different settings to alter (watch until 9:50min).
 - **IMPORTANT:** Notice at minute 5:35 how the video says to have the same address for the tag (variable) as in CCW. This address may look something like `_IO_EM_DO_01`. If the tag addresses for all your variables do not match the ones in CCW, the connection with Kepware will not work. 

To test the connection between your PLC and Kepware:
 - First, on CCW, connect you PLC and begin to run your "Hello World" program. This can be done by clicking "Disconnect" at the top. If your "Hello World" program does not run in a loop, just click "Disconnect" so that it says "Connected" but do not run the program yet. 
 - Next, on Kepware click the "Quick Client" button:
<img src="https://github.com/PTC-Academic/DX-Resources/blob/master/images/VST-PLC-image002.png" alt="Quick Client Button" width="400">
 - Once this is clicked, it should open a new window. Select <b>Chanel1."name of your PLC"</b>, The quality should be labeled as "Good" and once your program on CCW runs (or if it is already running) you should see the value update.<br/><br/>
<img src="https://github.com/PTC-Academic/DX-Resources/blob/master/images/VST-PLC-image003.png" alt="Quick Client Pannel" width="1000">

Your Allen-Bradley PLC should now be fully connected to Kepware

## Connecting Kepware to Vuforia Spatial Toolbox 

### Download the Spatial Toolbox 

You can either download the official version through the [Reality Team’s Website](https://spatialtoolbox.vuforia.com/) or you can download the [Intern version](https://github.com/PTC-Academic/SpatialToolbox-Windows-Interns).  
Both versions are essentially the same, however the Intern version has additional tools and contains a method to connect the Vuforia Spatial Toolbox with the SPIKE Prime.   

### Creating the Connection
 - Open Kepware and right click on IoT Gateway (on the right side)
 - Click "New Agent" and give it a name (We left it as "Agent")
 - Leave this Agent as "Rest Server" 
 - The URL is http://192.168.0.1:39320/iotgateway/ (This IP address is the same as the Gateway Address under Connecting Micro850 to Windows above)  
 - Click next and finish
 - Right click on your Agent and select "Properties". For the General settings it should match the information above, and make sure for "Configuration", "Enabled" is Yes. 
 - Click on "Server" (under General), the the Network Adapter should be the ethernet connection of the Micro850 (for us this was labeled as `Intel(R) Ethernet Connection (4) I219-V)`
 - The "Port Number" should be 39320, "Use HTTPS" should be No, everything else afterwards except the URL should be Yes
 - Click Apply or Ok
 <br/>
<b>IMPORTANT</b> When you save and close out of Kepware, the "Network Adapter" changes back to "Localhost only" for the Agent. Make sure that you change this to the Ethernet Connection above when you open Kepware to insure the connection works. 

After everything above is done, click on "Runtime" above (which is next to "Help") and select reinitialize. If you have the Intern Version of the Spatial Toolbox, follow the instructions on the [README](https://github.com/PTC-Academic/SpatialToolbox-Windows-Interns) to start the server.

When the server starts, navigate to your local host (mine is http://localhost:8080/) on your web browser. Select "Manage Hardware Interfaces" and make sure Kepware is turned on. If it is not on, turn it on and restart the Spatial Toolbox Server in Terminal. Make sure your screen looks like the one below: 

<img src="https://github.com/PTC-Academic/DX-Resources/blob/master/images/VST-PLC-image004.png" alt="Quick Client Pannel" width="600">

After, you should restart the Spatial Toolbox Server once more and now you should be fully connected! See our [Youtube Playlist](https://www.youtube.com/watch?v=TBEV5K3dprA&list=PLhL0fv9JyKMaWhaHmm21J6mgpp841zYYw&index=2&ab_channel=CEEOInnovations) to add image targets and how to use the Spatial Toolbox! 
 
