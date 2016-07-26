##How to make your map externally visible
A lot of people ask how you can make your map externally visible, so other people can view it, or so you can visit it from another location ngrok

###THIS GUIDE IS NOT UNIVERSAL
Some steps in this guide depend on your router, altough, most routers have a lot in common, so you should be fine

##Lets start!
We are not responsible for any damage that might occur.. You should take security mesures yourself

Step 1] First, we are going to find some basic information.. open the commmandprompt by hitting WindowsKey + R and typing "cmd"
<p align="center">
<img src="https://i.imgur.com/5WeUnTy.png">
</p>
Step 2] Enter "ipconfig" in the commandprompt. Now you will see an lot of appearing, this information WILL PROBARLY BE DIFFRENT IN YOUR CASE!!!
<p align="center">
<img src="https://i.imgur.com/O9LHEQv.png">
</p>
Step 3] Now, search the internet adapter that you are currencly using to connect to the network, and note these values.
<p align="center">
<img src="https://i.imgur.com/lzumhC2.png">
</p>
Step 4] In your browser, go to the IP-adress of your router that you found in the previous step, and log in
<p>
<img src="https://i.imgur.com/zVyGzu0.png">
</p>
Step 5] Find the portforwarding catagory in your router's control panel, and navigate here. (For me, "Application" -> "Port forwarding")
<p>
<img src="https://i.imgur.com/dsr3D5c.png">
</p>
Step 6] Your router may directly allow you to enter port here, mine doesn't so i am going to click on "Click here to add an application."
<p>
<img src="https://i.imgur.com/klEmgN4.png">
</p>
Step 7] Now we are on another screen, here we are going to enter the details. Pic an name wich you can remember, and set the protocol to TCP, because the application only uses the TCP protocol, there is no need to forward UDP.
<p>
<img src="https://i.imgur.com/CDlY4hX.png">
</p>
Step 8] The port selection is devided in 2 parts, mapping and normal. To make it simpel, we are going to enter the same values here. the start and end mark wich ports are being forwarded. If you enter 420 in start, and 423 in end, port 420, 421, 422 and 423 will be forwarded.
The ports you want to use don't matter.. i would recommend using between 5000 and 6000. (but this doesn't matter!) i am using these for demonstrating.
<p>
<img src="https://i.imgur.com/5zz30vv.png">
</p>
Step 9] Again, make sure that the mapping start and end port are the same. I will now hit "Add". My router now shows me an little table of my changes, i can remove or edit them if i made an mistake
<p>
<img src="https://i.imgur.com/esQHvdr.png">
</p>
Step 10] Now, I will go back to the previous screen and select the application i just created.
<p>
<img src="https://i.imgur.com/S2AKuW7.png">
</p>
Step 11] In the "LAN Host IP Address" box i will enter the IP adress of my computer, that we found in an previous step, and click "Add". Now you I see the application appear in the table, and is my port forwarded!
<p>
<img src="https://i.imgur.com/ligxZWc.png">
</p>
Step 12] Your port is now forwared! do not forget to start up the server with -P *the port you forwarded* -H 0.0.0.0. In my case:
<p>
<img src="https://i.imgur.com/en77ozU.png">
</p>

Credit: Langoor2

