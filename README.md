# Pokemon Online Startup Scripts (2.0.0)
Startup scripts for the Pokemon Online software - uses the "screen" command to manage session. This also restarts the Pokemon Online server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/MinetestStartup) - [Official Forum](https://minecity.online/index.php/forum/startup-scripts)  - [Official Download Area](https://minecity.online/index.php/downloads/category/5-server-tools)
![Minetest Sample Screen](https://MineCity.online/minetest_demo.png) 

---
These start up the Minetest server at boot time with a "screen" process.

1. Copy **minetest** into **/etc/init.d** - make sure it is executable
2. Copy **startminetest** into **/usr/local/minetest** - make sure it is executable
4. Run "**systemctl enable minetest**" (only needed once, will stick)
5. Run "**systemctl start minetest**" - starts Minetest without restarting the server

When you want to view the Minetest console, just enter "**screen -r**" in your shell.

To disconnect from the Minetest console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /usr/local/minetest/nostart**". To reenable it type "**rm /usr/local/minetest/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
