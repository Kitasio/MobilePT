## Android studio & Traffic interception
----
### Android Studio

Studio for making android applications, it has all the tool to create an
app, uses two main languages Java and Kotlin.

Every app contains 4 components

<ul>
	<li>broadcast reciver</li>
	<li>Services</li>
	<li>Activities</li>
	<li>Intent listener</li>
</ul>

### App components (development)
----
1. AndroidManifest.xml - /app/manifests/AndroidManifest.xml
2. MainActivity.java (the source code of the app) - /java/com.../MainActivity.java

### Traffic interseption
----
Catching data comes in 2 ways
1. local
2. external

Externally we can do it with Burp

1. First configure proxy on the phone --> settings --> wifi --> modify network --> advanced options, and here you find
the proxy to set for burp

2. Second configure the proxy on Burp --> in edit of the proxy listener set 'All interfases'

Certificate

Note that phone has to be rooted
Go to apkpure.com and download certificate manager 

In the phone browser go to http://burp/

Then go to the certificate app and import the burp certificate

Locally it's possible with a tool named PacketCapture (like wireshark for mobile)

### Activity events

1. onCreate - what happens when activity is created for the first time
2. onStart - when activity is started after an onStop event
3. onResume - what happens when avtivity is started after an onPause
4. onRestart - when activity restarts after being stopped
5. onPause - what happens when another activity pops and this goes to background
6. onStop - 
7. onDestroy - 

### Creating a simple user interface

After creating project you can configure the .xml file in layouts graphically or with code.

Creating activity, right click on com.exmple.myapp, new, activity, empty activity or whatever 

To make a connectin between two activitie - you need to use Intent object 

### Android reversing

Reverse engineering is the process of taking a product and revealing its design,
 architecture and operations.

There is a con in reversing which is the need to understand how processes work


### APKTOOL

this tool makes reverse for apk apps

in cmd: apktool.jar d myapp.apk

this will disasemble the application

in cmd: apktool.jar b myapp (the folder)

will build the app


### Smali operatio codes

if-eqz v0, :cond_0 --> jump to a location in the code named cond_0 if v0 equals 0.

const/16 v2, 0x3d --> defines a constant named v2, with a size 16bits, and the value 0x3d

move v0, v1 --> moves the content of v1 to v2

add-int v1, v2, 0x1 --> adds value 0x1 to the variable v2, and stores the value in v1

.method public [piblic] --> definition of a function block

return v0 --> returns the v0 to the function that called it


With reversing you can change the logic of the application

1. value changing
2. changing conditions
3. delete code
4. manipulate code