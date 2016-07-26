###First off, you will need to obtain https://github.com/AHAAAAAAA/PokemonGo-Map/pull/2153  

If you dont know how to do that, sorry.. i forgot how myself (SOmeone tell them how! ((unless its merged by that point)) )  

Alright, now that you have the Beehive, destroy everything except Location_Generator.py. Put this file into its own little folder, i named myne Beehive.  

Next, Open a Terminal by Shift + Right Clicking inside the folder you just put the location.py into. Once the terminal opens, type in the following command:   

python location_generator.py -st stepsize -lp ringsize -lat yourstartinglathere -lon yourstartinglonghere  


An example will look like this -  

python location_generator.py -st 5 -lp 4 -lat 39.949157 -lon -75.165297  

the terminal will output a list of coordinates. Right click the terminal, and select Mark. copy the entire list of coordinates, and then head over to your saved copy of this page: https://docs.google.com/spreadsheets/d/1Uh4VITpCciSy8pRh9I7OZuNiM-LizyBJcU7WR8oi7yY/edit#gid=263691484  

We are going to paste all of the coords you just copied, into the first section of colored spaces, starting with the Top Pink one (ctrl v will do it automagically!)  

##Next, setting up your .Bat, to be able to use the formatting from that page:  
  
  
  
:: Set PythonPath to where your Python is installed, Typically C:\Python27\Python.exe  
:: Set BranchPath to where you have the Pokemon Live Map folder  

SET PythonPath=  
SET BranchPath=  
SET Executable=runserver.py  

::GAPI is your google map api key
::auth is the authentication service you are using. PTC or Google
::Self explanatory, username of the chosen auth service
::again.. do i need to explain? password of chosen auth
::Threads default is 1, if you want more, change it here.. 1 is recommended until multithreading is fixed in windows.
::locale is the language output in your terminal, default is EN (english)


SET GAPI=  
SET auth=  
SET username=  
SET password=  
SET thread=-t 1  
SET locale=EN  


::kill all python processes  
taskkill /IM python.exe /F
echo Starting worker processes....


::title of this command window  
title Pokemon Go Map

::paste the second column of colors here, down to the last space of the color you wanted. Pink = 1 Leap, Purple - 2 Leaps, Blue = 3 Leaps, Green = 4 Leaps, and Yellow = 5 Leaps. The amount of workers required gets silly after 5 Leaps :P)  



::this part is the time it will pause till going back to the start again to restart the servers (edit the 1801 to change the delay in seconds)  

echo Waiting 30 minutes to restart all processes  
ping 127.0.0.1 -n 1801 > nul  

goto start  
pause  

Copy and paste all of ^ into a .txt document, rename it to Dickbutt.bat




Now that we have our .bat created, we are going to copy and paste the last column of the spreadsheet, based on colors, into the space above designated for the commands. File>Save, then double click the .bat to start the workers, in order.. Simple ^_^