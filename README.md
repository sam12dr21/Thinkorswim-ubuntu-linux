# Thinkorswim-ubuntu-linux
Thinkorswim in WINE in ubuntu linux

1.) install wine

```
sudo dpkg --add-architecture i386sudo dpkg --add-architecture i386

sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/noble/winehq-noble.sources

sudo apt update

sudo apt install --install-recommends winehq-stable wine64 winetricks
```

2.) launch winetricks  -> select default wine -> install windows components

> I IGNORED the following error - You are using a 64-bit WINEPREFIX. Note that many verbs only install 32-bit versions of packages. If you encounter problems, please retest in a clean 32-bit WINEPREFIX before reporting a bug.

3.) install dotnet 4.6.2 and visual c++ 2015-2022.

4.) this will take a few steps of clicking through installers

5.) then exit winetricks. open terminal and cd to directory of setup file. type `wine setup.exe`and hit enter.

6.) installation took about 15min and then after it shows installed, I had to press ctrl+c to end the terminal output.

7.) there will be no shortcut however, go to the location of the installation of TOS in wine -> /home/sam/.wine/drive_c/Program Files/thinkorswim/thinkorswim.exe

8.) double click to launch it and test if it works. then close it

9.) in notepad paste the following

```
[Desktop Entry]
Name=YourAppName
Exec=wine "/home/USERNAME/.wine/drive_c/Program Files/thinkorswim/thinkorswim.exe"
Type=Application
Terminal=false
```

replace USERNAME with yours. 

save it as *.desktop file

10.) launch and enjoy

if it does not launch then chmod +x the shortcut file and thinkorswim.exe if needed.
