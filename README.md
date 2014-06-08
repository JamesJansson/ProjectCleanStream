ProjectCleanStream
==================

The purpose of this project is to make it possible to ensure IP requests made by your computer or mobile are legitimate requests. This is used to prevent malicious programs from 'dialing home' and to identify threats at an early stage.

The idea of this project is to direct traffic through a cheap, open source device such as a RaspberryPi, which records traffic, and slowly learns what is legitmate and what is malicious or unknown. 

1) The RaspberryPi is connected to a home router using an ethernet connnector.

2) Attached to the RPi is a wireless USB dongle, which will allow the RPi to share the internet connection and hence act as a wireless router. 

3) The RPi directs traffic, while keeping a record of the IP addresses and a summary of key information sent in the packet to unknown IP addresses (packet sniffing).

4) The RPi preiodically generates a webpage that displays a summary of IPs accessed, the number of times accessed, any available information about that IP (such as country of orgin or other known information about that address), and ultimately the ability to add that address to either a whitelist or a blacklist. A user can access this webpage by entering a domain such as http://rhost, which updates automatically every few seconds.

5) The RPi can optionally and anonymously report IPs to a central repository that will identify IPs that are continously accessed, allowing them to be reported to the authorities as being suspicious, allowing identity theft software like keyloggers to be shutdown to prevent unnecessary loss. 

This system should allow you to monitor undisclosed processes that are making calls to IP addresses that are not requested by the user. It will not be able to identify threats that are installed on white listed IPs or domains. If a malicious call is being made through an organisation that you trust, it is unlikely that it will be able to identify those threats without complicated software to investigate every request. 

How to:

This video shows how to use a RPi as an internet passthrough device

https://www.youtube.com/watch?v=ZaHu0PratLU

Using the RPi for man in the middle interception

http://jeffq.com/blog/setting-up-a-man-in-the-middle-device-with-raspberry-pi-part-1/

Alternative for Android devices:

Note that the following application only saves the IPs visited. A method needs to be established to make the phone a HTTP server to allow the computer connnected to phone and match sites visited with data sent and received over the connection.
https://play.google.com/store/apps/details?id=jp.co.taosoftware.android.packetcapture


