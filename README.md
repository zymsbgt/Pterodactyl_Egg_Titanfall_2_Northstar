## Docker image for the egg
`docker.io/zymsbgt/northstar:latest` <br/>
So this works, the old repo didn't work though (their Docker image was too outdated and this repo uses Northstar 1.9.2 as of 9 August 2022). You'll need to use the Mounts Feature in Pterodactyl and mount the full Titanfall 2 game at `/mnt/titanfall` on the container.
Also dont forget to enable the mount in the wings conifg on the wings server that will be hosting the files.

## What about the Dockerfile?
Included in this repository.

All Joey did was make sure the user that was created was the Container user.
Turns out no entrypoint script was needed and the Enviroment variables handle all the server config anyways.

## Egg Vars

I've only included Server_Name and Server Descriptionas Egg Vars. Feel free to modify the egg to add others if you wish!


| Environment variable      | Description |
| ---                       | --- |
| NS_SERVER_NAME            | **Required.** The server name to show in the server browser. |
| NS_SERVER_DESC            | The server description to show in the server browser. |
| NS_SERVER_PASSWORD        | The password for the server. If empty, the server is public. |
| NS_PORT                   | The UDP game port. Must match with the forwarded port and be accessible from the default external IP. |
| NS_PORT_AUTH              | The TCP player authentication port. Must match with the forwarded port and be accessible from the default external IP. |
| NS_MASTERSERVER_URL       | The base URL of the master server. |
| NS_MASTERSERVER_REGISTER  | True/false for whether the server should register with the master server. If false, you will probably want to set NS_INSECURE to true. |
| NS_INSECURE               | Whether to allow unauthenticated direct connections to the server. |

## Want something simple to setup or a server to run this on?
I run GeyserHost, where I set up game servers like Minecraft and Northstar for gamers to run. If you'd like to leave setting up the server to me or wanna support my work, do join the [GeyserHost discord!](https://discord.gg/gwtQqFjDYp)

### Credits
I made this repo because I wanted to be able to host Titalfall 2 servers on Pterodactyl Panel. Found a repo (https://github.com/joeyjoey1234/Pterodactyl_Egg_Titanfall_2_Northstar) but it didn't work as it was too outdated, so I thought I might as well spend some time fixing it. 
Big thanks to Gecko#7945 and BulletMemes#0072 on the Northstar discord server for helping me with debugging!
