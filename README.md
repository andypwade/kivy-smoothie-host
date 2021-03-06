# kivy-smoothie-host
A Smoothie host, written in Kivy for running on rpi with touch screen.

This is a work in progress

This uses python >= 3.4.3

## Goal
The goal here is to have a small touch screen host that can run a smoothie and is better than an LCD Panel, and almost as good as a host PC running pronterface.
It is not meant to be a replacement for say Octoprint whose goals are different.

An RPI with 7" touch screen is about the same price as the better LCD panels, and makes a great standalone controller for a 3D printer.

I have had a 10" linux tablet called a pengpod running my delta printer for years as the only Host, it runs a hacked version of Pronterface to make it more tolerable to use on a touch screen. However Pengpods are no longer available and there are no other linux tablets I can find. A raspberry PI with touch screen is pretty close.

I'm was running with the very first RPI model A, but it runs pretty slowly.
I upgraded to an RPI-3 Model B and it runs much better, so I recommend them they are only about $10 more expensive.
I suspect an RPI-2 Model B will also run pretty well.


## Install on RPI

I use kivypi from here  http://kivypie.mitako.eu/ and the official 7" touch screen, pretty much runs out-of-the-box.
Recommended to do a sudo apt-get update and sudo apt-get upgrade.

You need the latest python serial and pyserial-asyncio from here https://github.com/pyserial/pyserial-asyncio.git
(git install).

(make sure pip is installed.. sudo apt-get python3-pip)

- sudo python3 -m pip install --upgrade pyserial
- python3 -m pip install --user aiofiles

Install the asyncio stuff:-
(May first need to do sudo apt-get python3-setuptools)
- git clone https://github.com/pyserial/pyserial-asyncio.git
- cd pyserial-asyncio/
- python3 setup.py install --user

Run with...

> kivy main.py

### On linux Desktop (and maybe windows/macos)

Install kivy for python3 from your distro:-

https://kivy.org/docs/installation/installation.html

1. sudo add-apt-repository ppa:kivy-team/kivy
2. sudo apt-get update
3. sudo apt-get install python3-kivy

Install pyserial which you probably alrady have:-
(make sure pip is installed.. sudo apt-get python3-pip)

4. sudo python3 -m pip install --upgrade pyserial

Install the asyncio stuff:-
(May first need to do sudo apt-get python3-setuptools)
5. git clone https://github.com/pyserial/pyserial-asyncio.git
6. cd pyserial-asyncio/
7. python3 setup.py install --user

Install the aio file stuff
8. python3 -m pip install --user aiofiles

Run as
> cd kivy-smoothie-host
> python3 main.py


# Screen shots
![Extruder Screen](screen1.png)
![Command Screen](screen2.png)
![Jog Screen](screen3.png)

