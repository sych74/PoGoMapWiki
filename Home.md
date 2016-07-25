# Welcome to the Pokemon Go Map wiki

Pokemon Go Map is aiming to bring a live visualization map of nearby Pokémon, Pokéstops and gyms in a form of a web-app as well as native phone applications.

Video Setup: 
[Video Walkthrough](https://www.youtube.com/watch?v=RJKAulPCkRI)  
[German Amazon EC2 Tutorial](https://www.youtube.com/watch?v=FxcVGrszl3I)
## Prerequisites

Installation will require Python 2.7 and Pip. If you already have these you can skip to [installation](#install-dependencies). Python 3 is not supported at all.

### Ubuntu or Debian

You can install Python and Pip on Ubuntu by running the following command:

```
sudo apt-get install python python-pip
```

### Windows

Download Python [here](https://www.python.org/ftp/python/2.7.12/python-2.7.12.amd64.msi) and install. Then download [pip](https://bootstrap.pypa.io/get-pip.py) (right click that link and choose "Save Link As"), and double click the file you downloaded, assuming you installed Python correctly.

There is a one-click setup for Windows. After you've installed Python, go into the `Easy Setup` folder and run `setup.bat`. This should install `pip` and the dependencies for you, and put your Google API key into the right place.

## Credentials and Downloading

Create a Pokemon Club account [on their official website] to be used by the program to search for Pokemon. This generally shouldn't be the same as your main Trainer account you personally use. As of 7/21/2016 this page is unavailable most of the time, refresh the page every 5-10 minutes and it should allow signups eventually.
You can also use a Google account. For both services, you can login without ever connecting to the actual game. 

Then, download one of the following branches below:

- [Download master](https://github.com/AHAAAAAAA/PokemonGo-Map/archive/master.zip) (Stable builds)
- [Download dev branch](https://github.com/AHAAAAAAA/PokemonGo-Map/archive/develop.zip) (Active development)

The dev branch will have latest features from the development team, however it may be unstable at some times.

Extract this zip file to any location.

## Install Dependencies

Now, open a Terminal/Command Line (`Win`+`R` and `cmd` on Windows) and `cd` to the folder you extracted the zip file to.

```
cd some/directory/
```

In Windows you can also right click within the folder and select "Open Command Window Here."

Then enter the following:

```
pip install -r requirements.txt
```
## Google Maps API key

You will need to generate your own Google Maps API key and place it in your program directory to use this program. Here's a [wiki entry](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Google-Maps-API:-a-brief-guide-to-your-own-key) on how to do this part.

## Running

To start the server, run the following command:

```
python runserver.py -u [USERNAME] -p [PASSWORD] -st 10 -k [Google Maps API key] -l "[LOCATION]"
```

or for Google account:

```
python runserver.py -a google -u [USERNAME] -p [PASSWORD] -st 10 -k [Google Maps API key] -l "[LOCATION]" 
```

Replacing [USERNAME] and [PASSWORD] with the Pokemon Club credentials you created previously, and [LOCATION] with any location, for example `Washington, D.C` or latitude and longitude coordinates, such as `38.9072 77.0369`.

Additionally, you can change the `10` after `-st` to any number. This number indicates the number of steps away from your location it should look, higher numbers being farther.

## Accessing

Open your browser to [`http://localhost:5000`](http://localhost:5000) and keep refreshing as it loads more Pokemon (auto refresh is not implemented yet).

## Project refactor
As of 2016-07-20, support for the first implementation 'example.py' was dropped.<br/>
Please use the refactored version present in the branch `develop`. <br/>
Periodic tagged releases will be made
