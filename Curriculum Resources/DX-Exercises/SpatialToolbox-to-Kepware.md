# Using Vuforia Spatial Toolbox with Kepware to Connect to Allen-Bradley PLCs
 
## Hardware Needed: ### 
 - An Allen Bradley PLC (This tutorial was written and tested with two Allen-Bradley PLCs, a [Micro850](https://literature.rockwellautomation.com/idc/groups/literature/documents/um/2080-um002_-en-e.pdf ) and a [CompactLogix 5840](https://literature.rockwellautomation.com/idc/groups/literature/documents/um/5069-um002_-en-p.pdf).)
 - An Ethernet Cable  
 - Windows Computer (This tutorial utilized a NUC)  

## Connecting the PLC to Windows ### 
Download [Connected Components Workbench (CCW)](https://compatibility.rockwellautomation.com/Pages/MultiProductFindDownloads.aspx?crumb=112&refSoft=1&toggleState=&versions=57681) 
 - Use [THIS](https://www.youtube.com/watch?v=BU7O8KXfdPA&ab_channel=TimWilborne) video from 2:39-8min to configure your specific PLC with CCW

Once your device is connected to CCW, try making a simple "Hello World" demo. A possible demo could be to use the Timer (TON) within CCW to turn your outputs on and off repeatedly. 
 - [HERE](https://www.youtube.com/watch?v=CI7o78YogGw&ab_channel=InsightsInAutomation) is a video that goes through this process

After you create a simple demo program, click on the `Micro850` tab and select `Ethernet` on the bottom right. Once selected, scroll down on the right side and select “Configure IP address and settings” underneath **Internet Protocol (IP) Settings**.  
 - Adjust the IP to your settings. For us, we set the IP Address to 192.168.0.2, the Subnet Mask to 255.255.255.0, and the Gateway Address to 192.168.0.1 

Your Allen-Bradley PLC should now be fully connected to your Windows Computer

## Connecting the PLC to Kepware 

[Download Thingworx Kepware Server](https://developer.thingworx.com/en/platform)
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
 <br />
<img src="https://github.com/PTC-Academic/DX-Resources/blob/master/images/VST-PLC-image002.png" alt="Quick Client Button" width="400">
 - Once this is clicked, it should open a new window. In the new window select `Chanel1.["name of your PLC"]`. The quality should be labeled as "Good" and once your program on CCW runs (or if it is already running) you should see the value update.
 <br />
<img src="https://github.com/PTC-Academic/DX-Resources/blob/master/images/VST-PLC-image003.png" alt="Quick Client Pannel" width="400">

Your Allen-Bradley PLC should now be fully connected to Kepware

## Connecting Kepware to Vuforia Spatial Toolbox 

### Download the Spatial Toolbox 

You can either download the official version through the [Reality Team’s Website](https://spatialtoolbox.vuforia.com/) or you can download the [Intern version](https://github.com/PTC-Academic/SpatialToolbox-Windows-Interns).  
Both versions are essentially the same, however the Intern version has additional tools and contains a method to connect the Vuforia Spatial Toolbox with the SPIKE Prime.   


Open Kepware and add an IoT Gateway (click “Add Agent”)  
For the Network Adapter, I chose the ethernet connection of the Micro850 (for me this was labeled as Intel(R) Ethernet Connection (4) I219-V)  
Important Note: Sometimes when I reopened Kepware after closing it, it would change this back to Local Host. Simply change it back to the correct ethernet connection (if it is not connected to the correct one, it will give an error) 
The Port Number is 39320 (This was mine)  
CORS Allowed Origins was left blank  
Use HTTPS was No  
Enable Write Endpoint and Allow Anonymous Login were both Yes  
URL is http://192.168.0.1:39320/iotgateway/ (This IP address is the same as the Gateway Address under Connecting Micro850 to Windows above)  
Then finally, reinitialize everything (there is a reinitialize button on Kepware)  
On the Edge Server (once you have your Spatial Toolbox running), click on Manage Hardware Interfaces, and select Kepware (this should be on) 
The IP should be the same as the IP above: 192.168.0.1 
You can then restart the server and it all should be connected!  
 
