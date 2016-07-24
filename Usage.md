`usage: runserver.py [-h] [-se] [-a AUTH_SERVICE] [-u USERNAME] [-p PASSWORD]
                    [-l LOCATION] [-st STEP_LIMIT] [-sd SCAN_DELAY] [-dc]
                    [-H HOST] [-P PORT] [-L LOCALE] [-c] [-d] [-m] [-ns] [-fl]
                    [-k GMAPS_KEY] [-C] [-D DB] [-t NUM_THREADS] [-np] [-ng]
                    [-nk]`

`-h` - shows help message.  
`-se` - Settings, loads config.ini.  
`-a AUTH_SERVICE` - Auth Service (ptc or google).  
`-u USERNAME` - Username (Email if using google).  
`-p PASSWORD` - Password.  
`-l LOCATION` - Location, can be an address or coordinates.  
`-st STEP_LIMIT` - Steps, the amount of 'steps' the scan will make.  
`-sd SCAN_DELAY` - Time delay before beginning new scan.  
`-dc` - Display Found Pokemon in Console.  
`-H HOST` - Set web server listening host.  
`-P PORT` - Set web server listening port.  
`-L LOCALE` - Locale for Pokemon names: default en, checklocale folder for more options.  
`-c` - Coordinates transformer for China.  
`-d` - Debug Mode.  
`-m` - Mock mode. Starts the web server but not the background thread.  
`-ns` - No-Server Mode. Starts the searcher but not the Webserver.  
`-fl` - Toggles the search bar, uses a 'fixed' location.  
`-k` GMAPS_KEY - Google Maps Javascript API Key.  
`-C` - Enable CORS on web server.  
`-D DB`  - Change the name of the database file, default is `pogom.db`.  
`-t` - Number of threads, default is set to 1.  
`-np` - Disables Pokemon from the map (including parsing them into local db).  
`-ng` - Disables Gyms from the map (including parsing them into local db).  
`-nk` - Disables PokeStops from the map (including parsing them into local db).  