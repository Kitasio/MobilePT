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