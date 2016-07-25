**Can I sign in with Google?**<br/>
Yes you can! Pass the flag `-a google` to use Google authentication. 

If you happen to have 2-step verification enabled for your Google account you will need to supply an [app password](https://support.google.com/accounts/answer/185833?hl=en) for your password instead of your normal login password.


**... expected one argument.**<br>
The -dp, -dg -dl, -i, -o and -ar parameters are no longer needed. Remove them from your query

**How do I setup port forwarding?**<br>
[See this helpful guide](https://github.com/Langoor2/PokemonGo-Map-FAQ/blob/master/FAQ/Portforwarding.md)

**["It's acting like the location flag is missing."](http://imgur.com/a/tM3BN)**<br>
-1, never forget

**I'm getting this error..**

| Error  |  Cause |
|---|---|
| `python is not recognized as an internal or external command`  | [Python has not been added to the environment](https://github.com/Langoor2/PokemonGo-Map-FAQ/blob/master/FAQ/Enviroment_Variables_not_correct.md)  |
| `pip or python is not recognized as an internal or external command`  | [pip needs to be installed to retrieve all the dependencies](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Installation-and-requirements)  |
| `Exception, e <- Invalid syntax.`  | This error is caused by Python 3. The project requires python 2.7  |
| `error: command 'gcc' failed with exit status 1`  | Your OS is missing the `gcc` compiler library. For Debian, run `apt-get install build-essentials`, For Red Had, run `yum groupinstall 'Development Tools'` |
| `[...]failed with error code 1 in /tmp/pip-build-k3oWzv/pycryptodomex/`   | Your OS is missing the `gcc` compiler library. For Debian, run `apt-get install build-essentials` For Red Had, run `yum groupinstall 'Development Tools'`  |
|   |   |
|   |   |



