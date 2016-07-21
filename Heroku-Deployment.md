This adds minimal Heroku support. Documentation should go into the wiki once this is in master.

### Documentation

- Create an app on Heroku.
- Clone PokemonGo-Map on your PC:
```sh
$ git clone https://github.com/AHAAAAAAA/PokemonGo-Map
$ cd PokemonGo-Map
$ git checkout develop
```
- Copy `credentials.example.json` to `credentials.json` and edit its contents.
- Commit `credentials.json`
```sh
$ git add -f credentials.json
$ git commit -m "added credentials.json"
```
- Push PokemonGo-Map to Heroku:
```sh
$ git push https://git.heroku.com/yourapp.git develop:master
```
- On Heroku add the following environment variables: `USERNAME`, `PASSWORD`, `LOCATION` and `STEP_COUNT`.
- On Heroku start and open the app.

Optionally you can add your own parameters using the `EXTRA_ARGS` environment variable. For example you can use `-dp -dg -ar 60` for `EXTRA_ARGS` to get pokestops, gyms and auto-refresh.