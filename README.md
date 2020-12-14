# DX-Resources
A collection of PTC Academic Digital Transformation Resources

This is a collection of learning materials and technical resources that illustrate how to leverage PTC (and open source) [Digital Transformation](https://www.ptc.com/en/industry-insights/digital-transformation) technologies for Academic and IIoT applications. These resources are organized by the primary fundamental objective involved in each, then by primary related technology:
* [Product Design (CAD)](https://github.com/PTC-Academic/DX-Resources#product-design-cad)
    * [PTC MathCAD](https://github.com/PTC-Academic/DX-Resources#ptc-mathcad)
    * [PTC Creo Parametric](https://github.com/PTC-Academic/DX-Resources#ptc-creo-parametric)
    * [Onshape](https://github.com/PTC-Academic/DX-Resources#onshape)
* [Digital Twin (IoT or AR)](https://github.com/PTC-Academic/DX-Resources#digital-twin-iot-or-ar)
    * [ThingWorx](https://github.com/PTC-Academic/DX-Resources#thingworx)
    * [Kepware](https://github.com/PTC-Academic/DX-Resources#kepware)
    * [Other Edge Devices](https://github.com/PTC-Academic/DX-Resources#other-edge-devices)
    * [Vuforia Studio](https://github.com/PTC-Academic/DX-Resources#vuforia-studio)
    * [Vuforia Engine](https://github.com/PTC-Academic/DX-Resources#vuforia-engine-sdk)
    * [Vuforia Spatial Toolbox](https://github.com/PTC-Academic/DX-Resources#vuforia-spatial-toolbox)
    * [Vuforia Expert Capture](https://github.com/PTC-Academic/DX-Resources#vuforia-expert-capture)
    * [Vuforia Chalk](https://github.com/PTC-Academic/DX-Resources#vuforia-chalk)
* [Digital Thread (PDM &amp; PLM)](https://github.com/PTC-Academic/DX-Resources#digital-thread-pdm--plm)
    * [Onshape PDM](https://github.com/PTC-Academic/DX-Resources#onshape-pdm)

## PTC DX Concept Map
![PTC Academic Digital Transformation Products Map](https://github.com/PTC-Academic/DX-Resources/blob/master/images/AP-overview.png?raw=true)

# Product Design (CAD)
## PTC MathCAD
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
[Example Exercise/Guide](https://apps.ptc.com/schools/curriculum/DX/MathCAD-Creo-DX.pdf)|PTC MathCAD & Creo Parametric Integration Guide|

## PTC Creo Parametric
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Creo Help Centers](https://www.ptc.com/en/support/help/Creo) | Help resources for all Creo products and versions, includes [Tutorials](https://support.ptc.com/help/creo/creo_pma/r7.0/usascii/#page/tutorials_pma%2Fonline_help%2Faux_files%2Fpma_tutorials.html%23) for the latest versions.|
| [PTC MathCAD & Creo Parametric Integration Guide](https://apps.ptc.com/schools/curriculum/DX/MathCAD-Creo-DX.pdf) | This guide aims to clarify the process of intergrating MathCAD and Creo Parametric, so that a mathematical output variable in MathCAD can be used to drive a Creo model, or so that the Creo relation can be used as an input variable. |
| [Creo Augmented Reality Experience for CAD Design](https://support.ptc.com/help/creo/creo_pma/r6.0/usascii/index.html#page/fundamentals%2Far_vr%2Fabout_ar_experience_for_cad_design.html%23) | This help content from PTC support covers several topics related to creating a simple Augmented Reality Experience to show your CAD mode or assembly in AR using the Vuforia View (App Store Google Play) app. |
| [Creo Parametric → Creo Illustrate → Vuforia Studio Tutorial](http://support.ptc.com/help/vuforia/studio/en/#page/Studio_Help_Center%2FCreateAnimationSequence.html%23) | This tutorial from the Vuforia Studio Help Center covers the process of creating a simple Creo Illustrate assembly sequence; written for a user that has a Creo Assembly, and wants to animate that assembly for use in Vuforia Studio. |
| [Creo Parametric + Creo Product Insight Extension + ThingWorx](https://learningconnector.ptc.com/content/tut-5552/creo-product-insight-extension-introduction) | This tutorial from the PTC Learning Connector explains how to use the Creo Product Insight Extension to connect a Creo Parametric model or assembly to a ThingWorx server, to integrate real-world sensor data into Creo for use in modeling, simulation, analysis and presentations. [Additional detailed help on Product Insight](https://support.ptc.com/help/creo/creo_pma/r6.0/usascii/index.html#page/assembly%2Finstrumented_assemblies%2FProduct_Insight_Overview.html%23) is available from the Creo online support site. |

## Onshape
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Onshape Learning Center](https://learn.onshape.com) | Start with the Learning Pathways in the Self-Paced Courses section for lots of great learning content. For specific searches, see the [Onshape Help Center](https://cad.onshape.com/help) or, for even more specific questions, search the [Onshape Forum](https://forum.onshape.com). |
# Digital Twin (IoT or AR)

## ThingWorx
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Hello ThingWorx!](https://apps.ptc.com/schools/curriculum/DX/HelloThingWorx.pdf) | A simple Hello World ThingWorx example that shows how to use REST API to make a simple IoT temperature dashboard.  ThingWorx and Vuforia Studio both require knowledge of JavaScript. [Learn JS at W3Schools.com](https://www.w3schools.com/js/) |
| [ThingWorx Developer Portal - Learning Pathways](https://developer.thingworx.com/en/resources/learning-paths) | A great place to start with ThingWorx, the Developer Portal contains tons of free resources for learning and building IoT solutions with ThingWorx. Specifically, this course is a good place to start: [Getting Started on the ThingWorx Platform](https://developer.thingworx.com/en/resources/learning-paths/getting-started-on-thingworx-platform)|
|[Monitor Plant Equipment Using Asset Advisor](https://developer.thingworx.com/en/resources/guides/mfg-apps-hosted-asset-advisor)|ThingWorx can optionally include some out-of-the-box Manufacutring Apps, to Monitor and Control a manufacturing systems; this learning path is a good starting point.|
|[How to Display Data in Charts](https://developer.thingworx.com/en/resources/guides/display-data-charts)|This guide will show you how to graphically display multiple data points in a various charts.|
|[How to send alerts over text with Twilio](http://support.ptc.com/help/thingworx_hc/thingworx_8_hc/en/#page/ThingWorx%2FHelp%2FExtensibility%2FTwilio.html%23%26_ga%3D2.70454672.1483803700.1580137650-2099000272.1553708236)|The ThingWorx Twilio extension provides the ability to send SMS text and voice messages from ThingWorx through the Twilio communication platform.|
|[How to send alerts over email.](http://support.ptc.com/help/thingworx_hc/thingworx_8_hc/en/#page/ThingWorx%2FHelp%2FExtensibility%2FMail.html%23%26_ga%3D2.115040967.1309540450.1579614259-2099000272.1553708236)|The ThingWorx Mail extension provides the ability to read and send e-mails from ThingWorx through external SMTP mail servers that are made available to it.|
|[Purging Runtime Data](https://support.ptc.com/help/thingworx_hc/thingworx_8_hc/en/index.html#page/ThingWorx/Help/ModelandDataBestPractices/purgingdata.html)|While PTC does not have an official recommendation on how much data to store, since it is heavily dependent on the use case, it is recommended to have a plan in place for any production system to purge the old data for performance reasons.|
|[Installing ThingWorx on Windows - Guide](https://apps.ptc.com/schools/curriculum/DX/ThingWorx-Installation-Guide.pdf)|PTC Academic Guide for Installing ThingWorx on Windows. For local/on-prem ThingWorx installation administrators.|
|[Utilizing ThingWorx Projects](https://apps.ptc.com/schools/curriculum/DX/Utilizing-ThingWorx-Projects.pdf)|Learn to use projects to organize, export and import entities in ThingWorx. |
|[Connect Raspberry Pi to ThingWorx](https://developer.thingworx.com/resources/guides/thingworx-raspberry-pi-quickstart)|Connect a Raspberry Pi to ThingWorx using the Edge Micro Server (EMS).|

## Kepware
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Kepware Website](https://www.kepware.com/en-us/) | Factory-wide Connectivity for access to the right data, at the right time. [Download a free demo.](https://www.kepware.com/Demo-Downloads/Edge-Thank-You-Page?product=d41a2c0a-e93b-474a-bee3-14c1d27e9428) |
|[How to Connect Kepware to ThingWorx](http://support.ptc.com/help/thingworx_hc/thingworx_8_hc/en/#page/ThingWorx%2FHelp%2FComposer%2FIndustrialConnections%2FIndustrialConnectionsExample.html%23)|Using the Industrial Connections in ThingWorx, you can connect to ThingWorx Kepware Server to model, configure, and bind tags that exist in ThingWorx Kepware |||Server to Things in the ThingWorx model.|
|[BYU Smart Manufacturing Instructional Video](https://www.youtube.com/watch?v=8w3yWtPCTsk)|Video showcasing how easy it is to make your factory smart with Thingworx and Kepware|
|[Connect Industrial Devices and Systems](https://developer.thingworx.com/resources/guides/thingworx-kepware-server-guide)|This guide has step-by-step instructions for connecting ThingWorx Kepware Server to ThingWorx Foundation.|
|[Industrial Connections Example](http://support.ptc.com/help/thingworx_hc/thingworx_8_hc/en/#page/ThingWorx%2FHelp%2FComposer%2FIndustrialConnections%2FIndustrialConnectionsExample.html%23)| Connect ThingWorx to a Kepware Server to model, configure, and bind tags that exist in ThingWorx Kepware Server to Things in the ThingWorx model. |

## Other Edge Devices
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [OPC UA Client](https://www.kepware.com/en-us/products/kepserverex/drivers/opc-ua-client/) | For Raspberry Pi and Arduino, Kepware is not used to connect to ThingWorx. If you would like to have Kepware as the connectivity method you would likely need to use this OCP UA Client, but I am less familiar with this architecture: |
| [Connect Raspberry Pi to ThingWorx](https://developer.thingworx.com/resources/guides/thingworx-raspberry-pi-quickstart) | Raspberry Pi Resources |
 | [Connect an Arduino Developer Board Guide](https://developer.thingworx.com/resources/guides/connect-adafruit-feather) | Arduino Resources |
 | [KepServerEx and LabVIEW](https://www.kepware.com/getattachment/151e8138-b6f5-4e7a-8e01-e6dab30da3d0/LabVIEW_Connectivity_Guide.pdf) | NI Resources |

## Vuforia Studio
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
|[Vuforia Studio Academic Installation Guide](https://apps.ptc.com/schools/curriculum/DX/VS-Academic-Install.pdf)|Installing Vuforia Studio (local AR authoring enviroinment), for Academic Vuforia Studio Users|
|[Vuforia Studio Tutorials and FAQs](http://support.ptc.com/help/vuforia/studio/en/#page/Studio_Help_Center%2FTutorialWelcome.html%23)|Tutorials and FAQs for various Vuforia Studio experience levels.|
| [Search results on ThingWorx Developer Portal for "Vuforia"](https://developer.thingworx.com/en/resources/learning-paths#stq=vuforia&stp=1) | The results include several useful learning materials; some specfically included here...| 
|[Get Started with Vuforia Studio](https://developer.thingworx.com/resources/guides/getting-started-vuforia-studio)| This Getting Started guide is designed to introduce Developer Portal users to Vuforia Studio.|
|[Create an Augmented Reality (AR) Experience](https://developer.thingworx.com/resources/guides/studio-ar-experience-quickstart)| In this exercise, you'll combine 3D CAD models and 2D Widgets into an Experience that displays on mobile devices. |
|[Develop an AR Experience Demo](https://developer.thingworx.com/resources/guides/blue-pump-ar-tutorial)| You’ll build a pump demonstration, and we’ll show you how to capture, store, analyze, and visualize data utilizing Vuforia Studio. |
|[Extend Studio Functionality with Javascript:](https://developer.thingworx.com/resources/guides/extend-studio-javascript)| Explore the benefits of using JavaScript with Studio to extend the capabilities and enhance your AR Experiences |
| [Create a Model Hierarchy](http://apps.ptc.com/schools/curriculum/DX/Vuforia-Studio-Model-Hierarchy.pdf) | This document outlines the steps to create a model hierarchy in Vuforia Studio to more easily animate motion of an entire assembly |
|[Bind ThingWorx Data to a 3D Widget](http://support.ptc.com/help/vuforia/studio/en/#page/Studio_Help_Center%2FBeginnerBindTWXData.html%23)|A short tutorial that shows how to add ThingWorx data to an Experience and bind it to a widget.|
|[How to grant users publish permissions within Vuforia Studio](https://www.ptc.com/en/support/article/CS268110)|This article contains instructions on how to manage common user permissions tasks in Vuforia Studio.|
|[Configuring Vuforia Studio & ThingWorx For Academic Use Cases](https://apps.ptc.com/schools/curriculum/DX/VuforiaStudio-AcademicConfiguration.pdf)|This guide outlines the requirements and best practices for leveraging ThingWorx Composer for academic IoT and AR education using ThingWorx and Vuforia Studio.|
|[How to Create a Model Hierarchy in Vuforia Studio](https://apps.ptc.com/schools/curriculum/DX/Vuforia-Studio-Model-Hierarchy.pdf)|Used to create kinematic constrained asseblies in Vuforia Studio (for example, a 6-axis robot)|

## Vuforia Engine (SDK)
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Vuforia (SDK) Developer Portal](https://developer.vuforia.com) | Resources for learning how to leverage Vuforia Engine (SDK). |
|[Vuforia Quick Installation Guide - Windows](https://apps.ptc.com/schools/curriculum/DX/Install_Vuforia.pdf)|How to install the Vuforia Engine/SDK in Unity.|
|[Vuforia Quick Installation Guide - MacOS](https://apps.ptc.com/schools/curriculum/DX/Install_Vuforia_MacOS.pdf)|How to install the Vuforia Engine/SDK in Unity.|
|[Add an Image Target to Your Experience ](https://apps.ptc.com/schools/curriculum/DX/Add%20an%20Image%20Target%20and%20CAD%20File.pdf)|This guide will show you how to Add an Image Target to Your Experience and Import Pre-Existing CAD Files |
|[From PTC Creo 3.0 to Vuforia 5.5](https://apps.ptc.com/schools/curriculum/DX/Creo_to_Vuforia.pdf)|In this guide you will learn how to Augment your PTC Creo 3.0 models with PTC Vuforia|

## Vuforia Spatial Toolbox
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Vuforia Spatial Toolbox](https://spatialtoolbox.vuforia.com) | The Vuforia Spatial Toolbox and Vuforia Spatial Edge Server make up a shared research platform for exploring spatial computing. |
|[Video tutorials](https://www.youtube.com/playlist?list=PLhL0fv9JyKMaWhaHmm21J6mgpp841zYYw)|Vuforia Spatial Toolbox Tutorials from the Tufts Center for Engineering Education and Outreach (CEEO)|

## Vuforia Expert Capture
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Transform Work Instruction with Vuforia Expert Capture](https://www.ptc.com/en/products/vuforia/vuforia-expert-capture) | Learn more about expert capture here, or reach out to PTC for a demo. |

## Vuforia Chalk
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Remote Assistance Powered by Augmented Reality](https://www.ptc.com/en/products/vuforia/vuforia-chalk) | Learn more about expert capture here, or reach out to PTC for information.  |
|[Vuforia Chalk - Introduction Series](https://www.youtube.com/playlist?list=PLrCBNJga3kdFt0-Ss_O_D1hlh2-Sms02S)|An introduction video series to get started with Vuforia Chalk.|
|[Installing Vuforia Chalk Guide](https://apps.ptc.com/schools/curriculum/DX/Chalk_guide.pdf)|A written guide that walks a user through intalling Vuforia Chalk.|


# Digital Thread (PDM &amp; PLM)
## Onshape PDM
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Onshape Learning Center - Data Management](https://learn.onshape.com/learn/learning-path/onshape-fundamentals-data-management) | In Onshape, PDM is built into the product. |
| [PTC Resource Center](https://www.ptc.com/en/Resource-center)| Search for the keyword 'twin' to find relevant publications. |

# Digital Transformation Curriculum Case Studies and Resources
## IoT Course
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Tufts University's Chris Rogers Webinar](https://players.brightcove.net/1532789042001/SJl3bQaEz_default/index.html?videoId=6131639163001) | Mechanical Engineering professor talks about teaching IoT to first year engineering students |

## Smart Manufacturing
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [BYU's Yuri Hovanski Webinar](https://players.brightcove.net/1532789042001/HknUe20R_default/index.html?videoId=6146274139001) | Mechanical Engineering professor talks about teaching IoT to first year engineering students |
| [Smart Manufacturing Supporting Documents](https://github.com/PTC-Academic/DX-Resources/tree/master/Curriculum%20Resources/Smart%20Manufacturing%20Supporting%20Documents) | A collection of articles on the theories motivating the push for smart manufacturing, from digitizing and connecting machines to visualizing information in augmented reality |

## Design Education
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Resource&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description | 
|---|---|
| [Purdue University's Karthik Ramani Webinar](https://players.brightcove.net/1532789042001/default_default/index.html?videoId=6155014476001) | Mechanical Engineering professor talks about teaching engineering design to university students by having them build toys|
