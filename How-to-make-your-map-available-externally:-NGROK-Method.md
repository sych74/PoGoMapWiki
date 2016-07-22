# How to make your map available externally using ngrok

Before following this guide you need to have everything working correctly at localhost, this simply forwards that to an
external address.

Start by adding -H 0.0.0.0 to the end of your command, for example

    python runserver.py -a ptc -u example -p dummy -l "Central park" -st 10 -H 0.0.0.0

Now download ngrok from [here](https://ngrok.com/download).

Extract it to the main folder, usually called "PokemonGo-Map-Develop", and run the .exe.

Now type "ngrok.exe http 5000" and hit enter. 
The "5000" can be replaced with whatever number you want, it's the port you're 
gonna use. I do however heavily recommend using 5000.

Now you're gonna see a window like this:
<p>
<img src="https://i.gyazo.com/b602507c0e5c6cc1b502f4ffa7cf62b3.png">
</p>

The highlighted address is the webadress for your map, so if you enter the link you will see something like this:
<p>
<img src="https://cdn.discordapp.com/attachments/204338767920758785/206017476662788096/unknown.png">
</p>
It will obviously differ depending on your location and the theme you are currently using.

Keep in mind that the ngrok website changes every time you write the command.

Now you're done!