JellyObject
-------------------------------------
[Asset Store Link](http://u3d.as/Mm0)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

Contact  
-------------------------------------
Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.net/contact](http://justingarza.net/contact/)
  
Description/Features
-------------------------------------
Make 2D Jelly Objects!* Shrink & Grow!
* Connect Child Objects
* Pull-Drag-Shoot
* Sticky!
* Plus Awesome Shader!
Terms of Use
-------------------------------------
You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

Table of Contents 
-------------------------------------
1. Full Discolsure
2. JellyObject.cs 
3. JellyObjectCollision.cs
4. JellyObjectSticky.cs
5. JellyObjectPuller.cs
6. Other Scripts
	* Controls.cs
	* SwitchScenes.cs
	* Demo0.cs
	* Demo1.cs
7. distortion.shader

  
Full Discolsure
-------------------------------------
This asset is based on a free tutorial that can be viewed on 
[youtube.com](https://www.youtube.com/watch?v=mCGVxMqHYUk&feature=youtu.be) and downloaded from [GitHub](https://github.com/calleerlandsson/SoftBodyDemo).

JellyObject.cs 
-------------------------------------
Makes an object appear as if it was made out of jelly.

**Shape Type**  
Used to determine how to arrange the ReferencePoints
(Circle or Rectangle)  
![Imgur](http://i.imgur.com/GvHDhvUs.png)  ![Imgur](http://i.imgur.com/WURW0xEs.png)  

**Reference Points Count**  
The reference points count.

**Reference Point Distance From Center**  
The reference point distance from center.  
(this should be adjusted to less than 1 if your texture does not go all the way to the edge.)
this is shown as "spacing" for rectangles

**Reference Point Radius**  
This is how large each Reference Point will be.

**Width**  
The width of the mesh that will be made

**Height**  
The height of the mesh that will be made

**Spring Damping Ratio**  
The spring damping ratio...or how fast will it settle

**Spring Frequency**  
The spring frequency...or Stiffness

**PhysMaterial**  
The physical material.

**childObjects**  
An Array of objects that will follow this object.

**Show Gizmos**  
The show gizmos.

**print Collisions**  
The print collisions in the console.

![Imgur](http://i.imgur.com/A1U9yFl.png)  
![Imgur](http://i.imgur.com/hat7kww.png)


**_The JellyObject.cs also contains some functions you might want to use._**

**AddChildObject()**  
used to add a child object (like eyes).

**ChangeSize()**  
Used to change the size of this object.

**ChangeSize_Delta()**  
used to increase or decrease the size of this Object.

**ReBuild()**  
call rebuild if you want to recreate all the reference points, Springs, etc.
(if you change a variable you might want to call this so the change will take effect).

JellyObjectCollision.cs
-------------------------------------
This is an Extension script for the JellyObject.cs.  
This script can be modified to controll what should happen during collision events. (i.e. take damage, increase in size, descrease in size, etc etc etc)

*Note: in it's current form this script only detects if the JellyObject is on the ground, or not.*

**printCollisions**  
print collisions in console

**isOnGround**  
this Bool determines if the JellyObject is on the ground

**GroundTags**  
Tags that will determine if an object is "ground".

![Imgur](http://i.imgur.com/O4uDOkA.png)

JellyObjectSticky.cs
-------------------------------------
This is an Extension script for the JellyObject.cs.
This script controlls weather the JellyObject is sticky or not

**stickToTags**  
Tags that will determine of the object sticks

**stuckToObj**  
the object this JellyObject is stuck to (used for Referencing in other scripts)

**unStick()**  
used to unstick this jellyObject (Method)

![Imgur](http://i.imgur.com/w5wk8WE.png)

JellyObjectPuller.cs
-------------------------------------
This is an Extension script for the JellyObject.cs.
This Script is a StateMachine that adds pull-drag-shoot functionality of the JellyObject.

**PrevState**  
The Previous State.

**State**  
The Current State 

**PullerLinePrefab**  
The puller line prefab. (this is just an Object with a LineRederer on it)
please see prefab in prefab folder for more info.

**ForceMultiplier**  
The force multiplier.

**maxPullDistance**  
The max pull distance.

**pullingTimeScale**  
The time scale while the object is in the PULLING State

**mustTouchOn**  
Weather or not the touch must occur on the object itself.

**AllowOnlyOnGroundOrStuck**  
The allow pull-drag-shoot functionality only on ground or stuck.

![Imgur](http://i.imgur.com/xPgSCk1.png)

Other Scripts
-------------------------------------
**Controls.cs:**  
Basic arrow controls to move the JellyObject

**SwitchScenes.cs:**  
Used to change the scene. 

**Demo0.cs:**  
Basic script to control the Size, Color, and more in the Demo0. 

**Demo1.cs:**  
Basic script to control the Force, StickToggle, and more in Demo1.

 
distortion.shader 
-------------------------------------
This is the shader i am using for the Jelly Objects in the demo.  

**_MainTex**  
Is the main texture.

**_Color**  
Is the color tint.

**_Distortion**  
How much the background will be distorted.

**_NormalMap**  
How the background will be distorted.

**_NormalMapMask**  
maps out where the normal map should distort and not distort.

**_Transparency**  
Fades between the color and the background.

**_Lightness**  
How much the colors should be lightned up.

![Imgur](http://i.imgur.com/fT0VqTb.png)  
![Imgur](http://i.imgur.com/QGwcb44.png)

