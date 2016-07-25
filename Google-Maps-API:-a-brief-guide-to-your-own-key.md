##How to get your own Google Maps key and use it for this project
This project uses Google Maps. There's one map coupled with the project, but as it gets more popular we'll definitely hit the rate-limit making the map unusable.
### Often this error is encounterd
<p>
<img src="https://i.imgur.com/QsMfL8D.png">
</p>
### How to fix this
Step 1] Go to [this](https://console.developers.google.com/flows/enableapi?apiid=maps_backend,geocoding_backend,directions_backend,distance_matrix_backend,elevation_backend,places_backend&keyType=CLIENT_SIDE&reusekey=true) webpage, you may have to sign in with your Google account.

Step 2] Select "Create new project" and click "continue". This may take a while, be patient and do not close the webpage.
<p>
<img src="https://i.imgur.com/WoGBZjH.png">
</p>
Step 3] Now enter an fancy name, and click create.
<p>
<img src="https://i.imgur.com/Oc10qJ9.png">
</p>
Step 4] Get your key and enable the Javascript API! An pop-up box will appear with you new API-Key! Save this Key ID. It is required for later in the Heroku configuration. One last step in the Google API dialogue before you leave, you need to enable the Google Maps JavaScript API to make available your newly generated key to outside services. This is accomplished by searching for Google Maps Javascript API in the search dialogue on the dev network homepage. Then enable it. This will prevent browser console errors in the future that say "ApiNotActivatedMapError." Now close the Google dev window.
<p>
<img src="https://i.imgur.com/D1K26f8.png">
</p>
Step 5] Navigate to your pokemon map directory, and inside the config folder you will find credentials.json.
<p>
<img src="https://i.imgur.com/sv4wNtd.png">
</p>
Step 6] add your previously created Google API key in this file, save it, and re-run the server! it should be working now! If you see an error, make sure you actually enabled the Javascript API in Step 4.
<p>
<img src="https://i.imgur.com/10uqA47.png">
</p>
