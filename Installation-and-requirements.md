In order to run the project, you will need Python, pip and the project dependencies.
Version 2.7 is what we usually test against. You can use 3.x but no support will be given. 

https://github.com/Langoor2/PokemonGo-Map-FAQ/blob/master/FAQ/Enviroment_Variables_not_correct.md

### Ubuntu or Debian

You can install Python and Pip on Ubuntu by running the following command:

```
sudo apt-get install python python-pip
```

### Windows

Download Python [here](https://www.python.org/ftp/python/2.7.12/python-2.7.12.amd64.msi) and install. Then download [pip](https://bootstrap.pypa.io/get-pip.py) (right click that link and choose "Save Link As"), and double click the file you downloaded, assuming you installed Python correctly.

## Credentials and Downloading

Create a Pokemon Club account [on their official website] to be used by the program to search for Pokemon. This generally shouldn't be the same as your main Trainer account you personally use. As of 7/21/2016 this page is unavailable most of the time, refresh the page every 5-10 minutes and it should allow signups eventually.

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

## Running

To start the server, run the following command:

```
python example.py -a ptc -u [USERNAME] -p [PASSWORD] -l "[LOCATION]" -st 10
```

Replaing [USERNAME] and [PASSWORD] with the Pokemon Club credentials you created previously, and [LOCATION] with any location, for example `Washington, D.C` or latitude and longitude coordinates, such as `38.9072 77.0369`.

Additionally, you can change the `10` after `-st` to any number. This number indicates the number of steps away from your location it should look, higher numbers being farther.

## Accessing

Open your browser to [`http://localhost:5000`](http://localhost:5000) and keep refreshing as it loads more Pokemon (auto refresh is not implemented yet).