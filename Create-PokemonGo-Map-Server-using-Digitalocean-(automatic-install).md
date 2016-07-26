# What is DigitalOcean
> DigitalOcean is a cloud infrastructure provider focused on simplifying web infrastructure for software developers.

> Each Droplet is billed per hour up to its monthly cap. You can choose to fund your account via PayPal or you can pay your monthly bill via credit card.
(for 10$ bonus credits see "Create an Account".

For more information see: https://www.digitalocean.com/help/

# Why using DigitalOcean?
I'm using it because it's a cheap way to fire up temporary servers.
If you destroy your droplet (server) after use, you will not be billed anymore. If you need your servers for two hours for exmaple, only 0.02$ will be billed.

# Create an Account
If you don't have an account, you can create one by using the following ref link:
[Create an Account at digitalocean.com](https://m.do.co/c/2d1757c3cb42)
Since the account is created, you will get 10$ in credits as reward. 

# Create a Server
* "Select an Image": Select "Ubuntu 16.04.1 x64" (first item in list) as distribution
* "Choose a size": Use the 5$ plan (512 MB, 1 vCPU, 20GB SSD)
* "Choose a datacenter region": Select any region you want to use
* "User Data": To use the ready to use configuration for your server, enable "User Data" checkbox and insert the following code into the textarea:

## Use master-Branch
```
#cloud-config
packages:
  - python
  - python-pip
runcmd:
  - cd /opt
  - git clone https://github.com/AHAAAAAAA/PokemonGo-Map.git
  - cd PokemonGo-Map
  - locale-gen en_GB.UTF-8
  - pip install -r requirements.txt
  - nohup python runserver.py -a <AUTHMETHOD> -u <USERNAME> -p <PASSWORD> -l <LOCATION> -st 20 -H 0.0.0.0 -P 80 -k <GMAPKEY> &
```

## Use develop-Branch
```
#cloud-config
packages:
  - python
  - python-pip
  - unzip
runcmd:
  - cd /opt
  - wget https://github.com/AHAAAAAAA/PokemonGo-Map/archive/develop.zip
  - unzip develop.zip
  - cd PokemonGo-Map-develop
  - locale-gen en_GB.UTF-8
  - pip install -r requirements.txt
  - nohup python runserver.py -a <AUTHMETHOD> -u <USERNAME> -p <PASSWORD> -l <LOCATION> -st 20 -H 0.0.0.0 -P 80 -k <GMAPKEY> &
```


For more information about cloud-config see: [How to Use Cloud-Config for your initial Server Setup](https://www.digitalocean.com/community/tutorials/how-to-use-cloud-config-for-your-initial-server-setup)

Note: Change the ```<VARIABLES>``` with your data.

After the server is created, you'll get an email with login information (ip address, root password).
Type in the ip address in your browser to show up the PokemonGo-Map.

Note: The process will take a few minutes after you get the mail to setup the application (PokemonGo-Map).

# Destroy Server
* Select your server from your list
* Click "Destroy" in the left menue.
* Click "Destroy" (red button)
* Confirm process by clicking "Confirm"