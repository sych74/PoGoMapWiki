# How to start using a MySQL server
**This is a guide for windows only currently.**

## I. Prerequisites 
1. Have already ran/operated the PokemonGo-Map using the default database setup. 
2. Have the "develop" build of PokemonGo-Map. [Available here.](https://github.com/AHAAAAAAA/PokemonGo-Map/archive/develop.zip)
3. Downloaded [MariaDB](https://downloads.mariadb.org/)

## II. Installing MariaDB
1. Run the install file, for me this was: mariadb-10.1.16-winx64.msi
2. Click next
3. Check "I accept the terms in the License Agreement" and click next
4. If you wish to change the installation location do that. If not click next.
5. Decide whether or not you want a password on your root account, if you don't put a password on it this database cannot be accessed from remote machines, which isn't necessary for what were doing. But if you do want a password go to 5a, if not go to 5b.
  - **5a.** Input the password you want into "new root password", and again into the "confirm" textbox. 
  - **5b.** Uncheck "modify password for database user 'root'.
6. Click next
7. All the default options are acceptable here. Hit next.
8. This screen wants to know if you can submit anonymous usage data, feel free to hit next or if you'd like to contribute data go ahead and check "enable the Feedback plugin and submit anonymous usage information" and then click next.
9. Click install. Administrator privileges required. 
10. Congratulations you've installed MariaDB and it's all downhill from here. 

## Setting up your database & editing Utils.py
1. Go to your windows start menu and locate MariaDB.
2. Open "MySQL Client"
3. If you created a password in step 5a above enter it now and hit enter. If you didn't create a password simply hit enter.
4. One this command prompt screen you'll want to enter: 
 <p>`CREATE DATABASE pokemongomapdb;`</p>
    You can change pokemongomapdb to whatever you want the name of the database to be.
5. If the database creation was successful it will tell you "Query OK, 1 row affected". If it doesn't echo that back at you then you either received an error message, or it just created a blank line. I've detailed how to fix common errors, and the blank line below.
    - **Blank line:** - 
***
You simply missed the ";" in the CREATE DATABASE command. Essentially you didn't close of the line, so the program thinks you still have more information to input. Simply insert a ; onto the blank line and hit enter and it should echo "Query OK" at you. 
    - **Error: "ERROR 1064 (42000): You have an error in your SQL syntax"** - Double check that you put in the CREATE DATABASE command exactly as it's typed above. If you had the blank line error, and then retyped the CREATE DATABASE line it will spit this at you because you actually typed "CREATE DATABASE pokemongomapdb CREATE DATABASE pokemongomapdb;". Simply retry the "CREATE DATABASE pokemongomapdb;" and don't forget your ";".
    - **Error: "ERROR 1007 (HY000): Can't create database 'pokemongomapdb'; database exists"** - The pokemongomapdb database already exists. 
If you're trying to start a fresh database you'll need to execute `DROP DATABASE pokemongomapdb`, and then run `CREATE DATABASE pokemongomapdb`. If you want to keep the pokemongomapdb but start a new one, change the name. 
6. Congratulations, your database is now setup and ready to be used. 

## III. Setting up the Config.ini file
### Config.ini
1. Open file explorer to where you've extracted your develop branch of PokemonGo-Map
2. Navigate to the "config" folder.
3. Right-click and open config.ini in your text editor of choice. I used Notepad++.
4. You're looking to fill in all the values in this file. If you've already ran and used the PokemonGo-Map like was required in step 1 of the prerequisites you should be familiar with most of this information, but I've broken it all down below.
    - **[Authentication]** - Service is either ptc, or google. Username and Password are your respective credentials for the service you chose above.
    - **[Database]** - This is the important section you will want to modify. 
        - Change the "Type" to "mysql" 
        - Change "Database_Name" to "pokemongomapdb"
        - Change "Database_User:" to "root", Change "Database_Pass:" to the password you chose in step 5a in section II, or leave it blank if you followed step 5b in section II.
        - Change "Database_Host" to "127.0.0.1"
    - **[Search_Settings]** - You will need to fill this out only if you plan to run only one worker to search for Pokemon. I personally run multiple workers to look for Pokemon so I left all of these at their defaults. If you plan to only run one instance however this needs to be filled out. Steps is how far out you want the scanner to look, Location is the coordinates of where you want to search, "Scan_delay" is how many seconds you want between scans, and if you so wish you may also disable pokemon, pokestops, or gyms by setting the respective value to true. I personally just do it on my actual map. If you plan to run more then one worker, make sure you follow the "editing utils.py" part below once you've setup the config.ini 
    - **[Misc]** - "Google_Maps_API_Key" is your own personal google maps API key. If you don't have one, or don't know what that is please see [this](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Google-Maps-API:-a-brief-guide-to-your-own-key) wiki page for the PokemonGo-Map project. "Host" is the host you are using, "Port" is whatever port you are running the map through, both of which would have been needed for you to run the map in prerequisite 1. 
5. Go to File->Save as... and make sure you save this file into the same directory as the "config.ini.example", but obviously save it as "config.ini". Make sure it's saved as a .ini file type, and not anything else or it won't work. 
6. You're now done configuring your config.ini file, 

### Editing Utils.py
**You only need to do this if you want to run multiple workers/scanners for pokemon with the mysql database**
<p>The reason you only need to do this with the mysql database is because in order to use the mysql database you must use the config.ini file. So when you call the config.ini with `-se` in runserver.py it ignores all other paramaters. We are simply going to comment out where it asks for location, and steps. However if you have a need to pass additonal paramters when you call runserver.py feel free to comment other blocks. </p>
1. Navigate to your branch directory
2. Go to the "pogom" folder
3. Locate utils.py and open it in your text editor of choice. 
4. The lines your looking for are under `def parse_config(args):` 
5. Simply add `#` to the front of every line you no longer want as a parameter. In our case: <p></p>
```
    args.location = Config.get('Search_Settings', 'Location')
    args.step_limit = int(Config.get('Search_Settings', 'Steps'))
```
<p>becomes </p>
```
    #args.location = Config.get('Search_Settings', 'Location')
    #args.step_limit = int(Config.get('Search_Settings', 'Steps'))
```

## Run it!
<p>Now that we have our server setup and our config.ini filled out it's time to actually run the workers to make sure everything is in check. Remember from above if you commented out any parameters in the util.py file that all of those parameters need to be met and filled out when you run the runserver.py script. In our case we commented out location, and steps so we could individual choose where each worker scanned, and the size of the scan. I've put two code snippets below, one would be used if you didn't comment out anything and instead filled out the **[Search_Settings]** in section III step 4 above. The other code snippet is what you would run if you commented out the same lines as I did in our running example.</p>
**Filled out Search_Settings & Commented out nothing in utils.py**<p></p>
`python runserver.py -se `
<p> </p>
**Left Search_Settings at default & Commented out location, and steps in utils.py**
<p> </p>
`python runserver.py -se -st 10 -l "[LOCATION]"`
<p>You should now be up and running. If you've encountered any errors it's most likely due to missing a parameter you commented out when you call runserver.py or you mis-typed something in your `config.ini`. However, if it's neither of those issues and something not covered in this guide hop into the PokemonGoDev discord server, and go to the help channel. People there are great, and gladly assist people with troubleshooting issues.</p>

## Final Notes & Credits
### Final Notes
<p>As just some quick closing notes, if you've encountered any problems or issues with this guide or find it needs to be updated please don't hesitate to let me know. I am normally always in the PokemonGoDev discord channels, or you can contact me by other means. I really hope this guide goes a long way in helping others, because I know I was confused when I tried to get the mysql servers setup and without the help I received I would have never got this setup, or this guide written.</p>
### Credits
<p>I'd just like to credit the PokemonGoDev channel on discord and the many people who have helped me in the past few days. I've learned a lot, and while I used to hobby program I just haven't been able to dig deep into this project. So without the help of the guys in Discord this guide wouldn't have been possible. So shout out to all of them, because well frankly tons of people helped me at various points along my way. </p>
<p>I'd also like to specifically credit Snuffy on discord for their great assistance, definitely one of the main contributors to helping me set this all up.</p>
