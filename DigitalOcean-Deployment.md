## Prerequisites

- [A DigitalOcean account](https://m.do.co/c/fb6730f5bb99)
- [A Google Maps API key](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Google-Maps-API:-a-brief-guide-to-your-own-key)
- [A new Pokemon Club account](https://club.pokemon.com/us/pokemon-trainer-club/sign-up/)

## Installation

Create a Droplet in your DigitalOcean control panel with Ubuntu 16.04, any Droplet size will work.

Check the "User Data" box lower on the page and enter the following:

```
#!/bin/bash

apt-get -y update
apt-get -y install python python-pip nodejs npm git
git clone https://github.com/AHAAAAAAA/PokemonGo-Map.git /root/PoGoMap
cd /root/PoGoMap
pip install -r requirements.txt
npm install
python runserver.py -u [USERNAME] -p [PASSWORD] -st 10 -k [Google Maps API key] -l "[LOCATION]" -H 0.0.0.0 -P 80
```

**Important:** Be sure to replace `[USERNAME]`, `[PASSWORD]`, [API Key]`, and `[LOCATION]` with your Pokemon Trainers Club Username and Password, your Google Maps API Key, and your location (Latitude and Longitude), respectively. You will be able to change locations later on the site.

Once you have that, create your Droplet. Setup will take a few minutes initially, but once it's done your map will be accessible at `http://[YOURDROPLET]/`, replacing that of course with your Droplet's IP address.

Credit: [JonahAragon](https://github.com/JonahAragon)