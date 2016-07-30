# Deploy PokemonGo Map within Jelastic Cloud

[![Deploy](https://raw.githubusercontent.com/sych74/PokemonGo-Map-in-Cloud/master/images/deploy-to-jelastic.png)](https://jelastic.com/install-application/?manifest=https://raw.githubusercontent.com/sych74/PokemonGo-Map-in-Cloud/master/manifest.jps)

Click on the button above to quickly deploy **PokemonGo Map** into Jelastic Cloud and evolve your personage much more faster! Do not waste your time blindly wandering across the streets and searching for a random pokemon - with this applet you can instantly observe all of them being drawn right over Google Maps in the desired location and easily catch the rare creature you want the most!

**P.S. No credit card is required.**

## Deployment Guide

1. After clicking the Deploy to Jelastic button, you’ll be shown a separate page with the following installation widget:
 
***image 1***

Here, the next data should be specified:
- **Name** - just your name
- **Email** - an email address your Jelastic account will be bound to
- **Company** - your company name
- **Service provider** - choose the desired hosting service provider (you can also use [Jelastic Cloud Union](https://jelastic.cloud/) for a simple comparison of the presented here vendors)

 > **Tip:** If you are already registered at any of the listed Jelastic Platforms, you can specify email of your existing account and proceed directly to the ***4th*** step of this instruction.

Click the **Install** button below when ready.

2. Then move to the specified email address inbox, open the newly received letter from Jelastic (usually titled as *Confirmation of application deploy*) and follow the link inside to confirm your account creation and complete PokemonGo Map installation.

***image 2***

> **Tip:** In case you’ve also got an additional letter with automatically generated account credentials, just skip the next guide step and proceed to the ***5th*** one.

3. Depending on the settings of the chosen service provider, you may be required to verify your account with either [captcha](https://docs.jelastic.com/account#captcha) or [mobile number](https://docs.jelastic.com/account#sms).

***image 3***

4. After you are redirected and automatically logged in the dashboard, you’ll see the ***PokemonGo Map*** installation frame:

***image 4***

First of all, you need to select the desired **account type**:
- ***Google Account*** - to connect to your Google account, enter the corresponding *User email* and *Password*:

***image 5***

- ***Pokemon Club Account*** - also you can launch directly to your Pokemon Club account with the corresponding credentials (whilst considering that *Pkmn Club User* is your nickname in the game **but not your email address**)

**Note:** If you’ve decided to create a [new Pokemon Club account](https://club.pokemon.com/us/pokemon-trainer-club/sign-up/), please be aware that their site can be occasionally unavailable due to high load, so just wait for a couple of minutes and try to reload the page.

***image 6***

> **Tip:** Neither *Google* not *Pkmn Club* account you define here shouldn’t be obligatory the one you actually use for the game - any existing account is suitable ( i.e. even if it has never been connected to the PokemonGo app).
Generally, it’s recommended to use a separate account for the Map applet.

5. Then, fill in the rest of the fields:

- **Your Location** - either address or latitude/longitude coordinates of your current location (can be determined with [Google Maps](https://www.google.com.ua/maps)), e.g. *Washington, D.C* or *38.9072 77.0369*
- **Steps Away** - defines the distance from your current location for the map to show the PokemonGo objects (the higher this number is, the greater radius you’ll explore)
- **Google Map API Key** - specify your [API key for Google map](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Google-Maps-API:-a-brief-guide-to-your-own-key/f0f622f6f1da28eddb57609bf47aa468cf56dedf) (or just use the default automatically populated one)
- **Environment** - the desired name for your environment (subsequently it will be used as a part of URL to access the map)
- **Display Name** - [environment alias](https://docs.jelastic.com/environment-aliases) (optional, i.e. can be left empty)
- **Region** - choose the preferable [environment region](https://docs.jelastic.com/environment-regions) from the automatically fetched list (in case this option present)

Finish with the **Install** button.

6. Wait a while for the installation to be completed and **Open** your map in **browser**.

***image 6***

7. That’s all! Map is already working and showing all the nearby pokemons, gyms and pokestops. Clicking on a particular pokemon will show the time it is going to disappear.

***image 7***

If needed, you can adjust some **Options**, available with the same-named button in the top left corner - e.g. change your location, select items to be displayed, enable/disable notifications about particular pokemons appearance, etc.

Just that easy! Now it’s time to catch ’em all!
