# Lighttpd on iOS 4 
***


This was a really fun side project I had. I owned an ancient iPod Touch, running iOS 4, or maybe even 3. At the time, I did no own any other devices - no laptop, desktop, server, anything. However, I needed to host web content, and as my iPod had 32gb of space, this was the perfect solution. I jailbroke it, installed a hotspot app, and started figuring out how to host a web site. I realized that I needed to actually run a web server on this tiny thing. 

So, I found an ARM binary of lighttpd, either from Cydia or from the web, I don't rememeber. Now, I needed a simple way to launch and kill the server. I installed SBSettings, but there was no toggle to easily do this. This is my solution.

There is no screenshot available unfortunately, as the device is long dead. However, it worked great!

**Note**: This is here purely for entertainment and historic reasons. Apple has tightened security on their products, and I've switched to Android years ago, where this is much simpler. I leave the steps and description here purely for fun.


### Installation Steps:

1. put startserv and stopserv in /usr/sbin, chmod to 755

2. In /var/mobile/Library/SBSettings/Commands
	replace defaults com.sbsettingslighttpd.*, located in this folder
	
3. Replace /System.Library/LaunchDaemons/net.limneos.lighttpd.plist

	
4. When the toggle is clicked, it loads the framework, which starts the server. When it is tapped again, the framework is unloaded and the server is killed.

*Note* As a bonus, I've included a screenshot of how my desktop looked at the time of this work. (lighttpd_work.png)

### Usage

If you happen to have a jailbroken iPhone or iPod touch running iOS 4 with SBSettings, feel free to give this a spin.



#### Contributors

Ivan Smirnov
