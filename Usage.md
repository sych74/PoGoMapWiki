
# Usage
`python example.py -a authService -u myUsername -p myPassword -l "Boulder, CO" -st 5`

| Flag                       | Description                                            | Required |
|----------------------------|--------------------------------------------------------|----------|
| `-a` `--auth-service`      | Auth service (PTC or google)                           |          |
| `-u` `--username`          | Username                                               | ✓        |
| `-p` `--password`          | Password                                               | ✓        |
| `-l` `--location`          | Any location Google Maps can understand                | ✓        |
| `-st` `--step-limit`       | Steps to take                                          | ✓        |
| `-i` `--ignore`            | Comma-separated list of Pokémon names or IDs to ignore |          |
| `-o` `--only`              | Comma-separated list of Pokémon names or IDs to search |          |
| `-ar` `--auto-refresh`     | Number of seconds on which to autorefresh              |          |
| `-dp` `--display-pokestop` | Display pokéstops                                      |          |
| `-dg` `--display-gym`      | Display gyms                                           |          |
| `-H` `--host`              | Set web server listening host                          |          |
| `-P` `--port`              | Set web server listening port                          |          |
| `-L` `--locale`            | Locale for Pokemon names: default en, check locale folder for more options |          |
| `-c` `--china`             | Coordinates transformer for China                      |          |
| `-d` `--debug`             | Debug mode                                             |          |
| `-ol` `--onlylure`         | Display only lured pokéstop                            |          |

_Note:
5 steps is approximately a 1.2km radius. More than 10 is redundant (you usually can't walk that far before despawn anyway)_

## Working examples
### ignore Pokémon
`python example.py -a PTC -u myUsername -p myPassword -l "Central Park, New York, NY" -st 5 -i Pidgey,Weedle,Zubat`

### make server externally visible
#### IPv4
`python example.py -a PTC -u myUsername -p myPassword -l "Central Park, New York, NY" -st 5 -H 0.0.0.0 -P 5000`
#### IPv6
`python example.py -a PTC -u myUsername -p myPassword -l "Central Park, New York, NY" -st 5 -H :: -P 5000`
