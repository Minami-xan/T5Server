
![alt text](https://img.shields.io/badge/Debian-10-red?logo=Debian)
![alt text](https://img.shields.io/badge/Plutonium-T5-blue)

<img src="https://imgur.com/bBrx8Hf.png" alt="drawing" width="350"/> <img src="https://i.imgur.com/TdpsBgH.png" alt="drawing" width="200"/>

# T5Server
Simple installation and configuration of a T5 server on linux.

## Required
+ Last Version of Debian 10 (Probably work on Debian 11)
+ Storage more than 30Gb
+ Sudoer permission

## Installation
1. Download files : 
```shell 
git clone https://github.com/Minami-xan/T5Server.git
```
2. Move to `T5Server` Folder.
```shell
cd ~/T5Server/
```
3. Run the Installation Script `install.sh` .
```shell
sudo env "HOME=$HOME" bash install.sh
```
4. Download Game File
```shell
sudo transmission-cli pluto_t5_full_game.torrent -w $HOME/T5Server
```
5. After the download organize and sort the file
```shell
sudo rm $HOME/T5Server/pluto_t5_full_game.torrent
sudo mv $HOME/T5Server/pluto_t5_full_game $HOME/T5Server/Server
sudo rm -r $HOME/T5Server/Server/redist
sudo rm $HOME/T5Server/README.md
```
<center> <b>Installation Complete</b> </center>

## Configuration
1. Move to `Plutonium` Folder.
```shell
cd ~/T5Server/Plutonium/
```
2. Edit `T5_**_server.sh` with your information.
```shell
nano T5_mp_server.sh
#OR
nano T5_zm_server.sh
```
3. Allow server port.
```shell
sudo bash ~/T5Server/Scripts/allow_port.sh
```
<center> <b>Configuration Complete</b> </center>

## Launch Server
1. Move to `Plutonium` Folder.
```shell
cd ~/T5Server/Plutonium
```
2. Launch Server. 
```shell
./T5_mp_server.sh
#OR
./T5_zm_server.sh
```
   I advise you to use `tmux` or `screen` to open and manage multiple servers.

## Source
• **Plutonium:** https://plutonium.pw <br>
• **My Topic** https://forum.plutonium.pw/topic/23683/guide-debian-t5-server-on-linux-vps-dedicated-server <br>
• **Plutonium-Updater by mxbe:** https://github.com/mxve/plutonium-updater.rs <br>