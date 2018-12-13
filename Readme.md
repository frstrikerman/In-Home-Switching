# In-Home-Switching

This is a homebrew that enables streaming of PC games to the Nintendo Switch.

Have you ever been told by your parents that spending hours sitting in front of a PC was bad for you (like I was)? Well, now you can play your games portably anywhere in your house!

You can find the corresponding repo for the PC app [here]( MISSING LINK ).

This project is fairly new, so please do not consider it totally stable. If you encounter serious issues, feel free to submit them.

## Features:
  * Stream PC screen to a Nintendo Switch in your local network
    * 720p (full Switch display resolution)
    * 40-60 FPS (if not see Troubleshooting)
    * Low delay (again, see Troubleshooting)
  * Capture Input on Switch
    * Emulate an Xbox controller on the PC
  * PC app offers picture quality adjustments

## How to Use
If you do not want to build by yourself, have a look at the [Releases page](https://github.com/jakibaki/In-Home-Switching/releases). You also need the companion app on your PC (Win 8 or later) which you can grab [here]( MISSING LINK ).
Just start the App with your Switch CFW. You are then told an IP that you have to type in the PC app for connecting. Link start!

## Screenshots

MISSING

## Current Limitations
  * Only works with Windows 8 and newer
  * No audio support atm
  * No support for Switch CFW other than [Atmosphère](https://github.com/Atmosphere-NX/Atmosphere)

## Scheduled for Future Releases
  * Stream PC audio to Switch
  * Multi-controller support
  * More efficient threading

## Build instructions

MISSING

## Troubleshooting

### *Nice videos, but sadly that delay makes it unplayable*

If you are experiencing delays greater than 0.1 seconds, either your PC is just to slow for your chosen quality options (try GPU encoding, worse image quality) or your local network is bad. Basically we need instant transfer in the network (this has nothing to do with troughput, just latency)

### *These framedrops hurt my eyes!*

Your PC is probably to slow for encoding with the games/applications on. Try other applications, lower image quality, set your PC screen resolution to 1280x720p (saves scaling) and try changing the GPU usage setting.

### *No drops, but my framerate is just very low*

Well, in our tests we had 60 FPS on Windows 10 with lower image quality... I guess you can try the same strategies as for fixing framedrops, I hope that helps.

## License

This code is licensed GPLv3 and this has a reason: We do not want to see (or read about) any parts of this project in non-open-source software (everything that is not GPLv3 licensed). Please share the notion of free code for everyone.

## Credits to

* [ffmpeg](https://www.ffmpeg.org/) for being such a powerful media tool that we use on PC and Switch.
* [SwitchBrew](https://switchbrew.org/) for libNX and its ffmpeg inclusion
* [Atmosphère](https://github.com/Atmosphere-NX/Atmosphere) for being a great Switch CFW
* [Captura](https://github.com/MathewSachin/Captura) for showing us how to capture frame input with Windows Duplication API