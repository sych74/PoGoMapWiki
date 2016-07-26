##How to make your map externally visible
A lot of people ask how you can make your map externally visible, so other people can view it, or so you can visit it from another location.

**THIS GUIDE IS NOT UNIVERSAL.** Some steps in this guide depend on your router, but most routers have a lot in common, so you should be fine.

##Lets start!
We are not responsible for any damage that might occur. You should take security measures yourself.

1. First, we are going to find some basic information. Open the Command Prompt by hitting Windows + R and typing "cmd"
<p align="center">
<img src="https://i.imgur.com/5WeUnTy.png">
</p>
2. Enter "ipconfig" in the command prompt. Now you will see a lot of information appearing, this information WILL PROBABLY BE DIFFERENT IN YOUR CASE!!!
<p align="center">
<img src="https://i.imgur.com/O9LHEQv.png">
</p>
3. Now, search the internet adapter that you are currently using to connect to the network, and note these values.
<p align="center">
<img src="https://i.imgur.com/lzumhC2.png">
</p>
4. In your browser, go to the IP Address of your router that you found in the previous step, and log in. If you don't know them already, the login information is usually on the bottom of your router, unless they've already been changed.
<p>
<img src="https://i.imgur.com/zVyGzu0.png">
</p>
5. Find the Port Forwarding category in your router's control panel, and navigate here. (For me, "Application" -> "Port forwarding")
<p>
<img src="https://i.imgur.com/dsr3D5c.png">
</p>
6. Your router may directly allow you to enter port here, mine doesn't so I am going to click on "Click here to add an application."
<p>
<img src="https://i.imgur.com/klEmgN4.png">
</p>
7. Now we are on another screen, here we are going to enter the details. Pick a name which you can remember, and set the protocol to TCP, because PoGoMap only uses the TCP protocol.
<p>
<img src="https://i.imgur.com/CDlY4hX.png">
</p>
8. The port selection is divided in 2 parts, mapping and normal. To make it simple, we are going to enter the same values here. the start and end mark which ports are being forwarded. If you enter 420 in start, and 423 in end, port 420, 421, 422 and 423 will be forwarded.
The ports you want to use don't matter. I would recommend using between 5000 and 6000. (but this doesn't matter!) I am using these for demonstrating.
<p>
<img src="https://i.imgur.com/5zz30vv.png">
</p>
9. Again, make sure that the mapping start and end port are the same. I will now hit "Add". My router now shows me an little table of my changes, I can remove or edit them if I made an mistake.
<p>
<img src="https://i.imgur.com/esQHvdr.png">
</p>
10. Now, I will go back to the previous screen and select the application I just created.
<p>
<img src="https://i.imgur.com/S2AKuW7.png">
</p>
11. In the "LAN Host IP Address" box I will enter the IP address of my computer, that we found in a previous step, and click "Add". Now you I see the application appear in the table, and is my port forwarded application!
<p>
<img src="https://i.imgur.com/ligxZWc.png">
</p>
12. Your port is now forwarded to the map! do not forget to start the server with `-P *the port you forwarded* -H 0.0.0.0`. In my case:
<p>
<img src="https://i.imgur.com/en77ozU.png">
</p>

Credit: Langoor2

