# Pokemon Online Startup Scripts (2.0.0)
Startup scripts for the Pokemon Online software - uses the "screen" command to manage session. This also restarts the Pokemon Online server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/PokemonOnlineStartup) - [Official Forum](https://pokemon.gameplayer.club/index.php/forum/pokemon-online-server-support)  - [Official Download Area](https://pokemon.gameplayer.club/index.php/downloads/category/6-pokemon-online-server-scripts)
![Pokemon Sample Screen](https://pokemon.gameplayer.club/Pokemon512Icon.png) 

---
These start up the Pokemon Online server at boot time with a "screen" process.

1. Copy **pokemononline** into **/etc/init.d** - make sure it is executable
2. Copy **startpokemononline** into **/root/pokemon-online** - make sure it is executable
4. Run "**systemctl enable pokemononline**" (only needed once, will stick)
5. Run "**systemctl start pokemononline**" - starts Pokemon Online without restarting the server

When you want to view the Pokemon Online console, just enter "**screen -r**" in your shell.

To disconnect from the Pokemon Online console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/pokemon-online/nostart**". To reenable it type "**rm /root/pokemon-online/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
