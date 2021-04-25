# How to Add a World Object #

#### What is a World Object?
* World Objects are another method of creating an image target. They allow the user to not hover over an image during their AR experience. Rather, you can scan an image once, and place your experience to a desired location. 

<center><img src="resources/gif1.gif" style="width:75%; border:2px solid #000"></img></center>

###Step 1: 
To begin, git clone our master branch to your Desktop. Once it is finished downloading, ppen terminal and `cd` into the downloaded folder. After you are in the folder, in terminal do `git checkout SpatialToolbox-Mac-Emun` then do `git pull origin SpatialToolbox-Mac-Emun`. This should update the folder so that you have the proper branch. 

###Step 2:
Open the SpatialToolbox-Mac-Interns folder on your Desktop and move the `spatialToolbox` folder to your Documents. You will notice that it is empty; this is ok because when the server runs, it should download necessary folders for you. 

###Step 3:
In terminal within the downloaded folder, do `cd vuforia-spatial-edge-server`. Then run `node server` in the terminal. Go onto your localhost and select **Add World Object**. Give it a name, and select add target. 

You can drag in your image target directly from your desktop (it should be a .jpg). In the image bellow, my world object is called "EmunWorld" and my image target is a generic Thingmark. 

<center><img src="resources/img1.png" style="width:75%; border:2px solid #000"></img></center>

###Step 4:
Next, you should stop your server on the terminal and then run it again. When you go back onto your localhost, you will notice the SPIKE interface is already there. This is because this is automatically added. 

The key here is that where it says "Edit Target". Notice how it has an achor icon. This is because it is anchored to your World Object. If you open the app on your phone, you will see the AR visualization on it! 

<center><img src="resources/img2.png" style="width:75%; border:2px solid #000"></img></center>

###Notes: 
* You can move the targets ontop of your World Object by click it and looking somewhere else, and then clicking again to place it down. 







