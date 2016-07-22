If you happen to have 2-step verification enabled for your Google account you will need to supply an [app password](https://support.google.com/accounts/answer/185833?hl=en) for your password instead of your normal login password.

Q: Can I sign in with Google?<br/>
A: Yes you can! Pass the flag `-a google` to use Google authentication

Q: ... expected one argument
A: The -dp, -dg -dl, -i, -o and -ar parameters are no longer needed. Remove them from your query

Q: Port forwarding Tutorial?
A: https://github.com/Langoor2/PokemonGo-Map-FAQ/blob/master/FAQ/Portforwarding.md

Q: `python is not recognized as an internal or external command`<br/>
A: https://github.com/Langoor2/PokemonGo-Map-FAQ/blob/master/FAQ/Enviroment_Variables_not_correct.md

Q: `pip or python is not recognized as an internal or external command`<br/>
pip needs to be installed to retrieve all the dependencies, [see how](https://github.com/AHAAAAAAA/PokemonGo-Map/wiki/Installation-and-requirements)

Q: `Exception, e <- Invalid syntax.`<br/>
A: This error is caused by Python 3. The project officially supports 2.7

Q: `error: command 'gcc' failed with exit status 1` or `[...]failed with error code 1 in /tmp/pip-build-k3oWzv/pycryptodomex/`  
A: Your OS is missing the `gcc` compiler library. Run `apt-get install build-essentials`