# Using Vuforia Spatial Toolbox with Kepware to Connect to Allen-Bradley PLCs 
 
## Hardware Needed:  
This tutorial was written and tested with two Allen-Bradley PLCs, a [Micro850](https://literature.rockwellautomation.com/idc/groups/literature/documents/um/2080-um002_-en-e.pdf ) and a CompactLogix 5840.

###
An Ethernet Cable  
Windows Computer (I used the NUC)  

## Connecting Micro850 to Windows 
Download Connected Components Workbench (CCW) 
I used this video: https://www.youtube.com/watch?v=BU7O8KXfdPA&ab_channel=TimWilborne 
Started at 2:39min and stopped at 8min  
After this, I used this video to help make a “Hello World.” I recommend googling different resources to familiarize yourself with CCW.  
https://www.youtube.com/watch?v=CI7o78YogGw&ab_channel=InsightsInAutomation 
Once connected, make sure to click Micro850 on CCW and select Ethernet 
Here, select “Configure IP address and settings” and adjust the IP to your needs 
For me my IP Address was 192.168.0.2, my Subnet Mask was 255.255.255.0, and my Gateway Address was 192.168.0.1 

## Connecting Micro850 to Kepware 

### Download Thingworx Kepware Server  
Once you open Kepware, you can add a Channel and select “Allen-Bradley Micro850 Ethernet” 
Here is a link to a video that walks through the different settings:  
https://www.youtube.com/watch?v=KRFA9YutiUs&ab_channel=LearnWithPro-Tutorial 
Watch until 9:50  
Important to note (minute 5:35): Notice how the video says to have the same address for the variable as in CCW. This address may look something like this --> _IO_EM_DO_01 
Add all of your variables that you want for the Micro850 here 

### Additional Resource: https://developer.thingworx.com/resources/learning-paths/using-allen-bradley-plc-thingworx/connect-allen-bradley-plc/configure-thingworx-kepware-server 
Another Note: As I was figuring everything out, Peter helped fix an error that I was getting when running Kepware which was to download this: https://java.com/en/download/manual.jsp 
This may not need to be downloaded, but if you are running into a bug on Kepware this may fix it 

## Connecting Kepware to Vuforia Spatial Toolbox 

### Download the Spatial Toolbox 
You can either download the official version through the Reality Team’s Website or you can download the intern version.  
Both versions are essentially the same, however the Intern version has additional tools  
Intern version can be found here: https://github.com/PTC-Academic/SpatialToolbox-Windows-Interns 
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
 