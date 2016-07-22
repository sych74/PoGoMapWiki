`usage: runserver.py [-h] [-a AUTH_SERVICE] -u USERNAME [-p PASSWORD] -l`
                    `LOCATION -st STEP_LIMIT [-i IGNORE | -o ONLY]`
                    `[-ar AUTO_REFRESH] [-ol Display only lured Pokestops] [-H HOST] [-P PORT]`
                    `[-L LOCALE] [-c] [-d] [-m] [-k GMAPS_KEY]`

-h, -        shows help message  
-a AUTH_SERVICE  - Auth Service  
-u USERNAME      - Username  
  -p PASSWORD    - Password  
  -l LOCATION    - Location, can be an address or coordinates  
  -st STEP_LIMIT - Steps  
  -sd SCAN_DELAY - Time delay before beginning new scan  
  -dc            - Display Found Pokemon in Console  
  -H HOST        - Set web server listening host  
  -P PORT        - Set web server listening port  
  -L LOCALE      - Locale for Pokemon names: default en, checklocale folder for more options  
  -c             - Coordinates transformer for China  
  -d             - Debug Mode  
  -m             - Mock mode. Starts the web server but not the background thread.  
  -ns            - No-Server Mode. Starts the searcher but not the Webserver.  
  -k GMAPS_KEY   - Google Maps Javascript API Key  
  -C             - Enable CORS on web server  
