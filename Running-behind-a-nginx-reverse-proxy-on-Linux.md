If you do not want to expose pokemongo-map to the web directly or you want to place it under a prefix, follow this guide:

Assuming the following:

* You are running pokemongo-map on the default port 5000
* You've already made your machine available externally (such as with [ngrok](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/How-to-make-your-map-available-externally:-NGROK-Method))

1. Install nginx (I'm not walking you through that, google will assist)
2. In /etc/nginx/nginx.conf add the following before the last `}`

```
include conf.d/pokemongo-map.conf;
```

3. Create a file /etc/nginx/conf.d/pokemongo-map.conf and place the following in it:

```
        location /go/ {
           proxy_pass http://127.0.0.1:5000/;
        }
```

You can now access it by http://yourip/go

