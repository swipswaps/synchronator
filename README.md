# Synchronator

Synchronator brings bit perfect volume control to Hi-Fi systems with Linux as source. 

This enables controll of your Hi-Fi amplifier volume level from within any Airplay, DLNA, OpenHome, or MPD application a.o.


## Technical background

Contrary to many other operating systems in Linux it is not uncommon that audio applications, such as MPD and Shairport, allow audio data and mixer/volume data to be send to different (audio) devices. By sending mixer data to a dummy/virtual soundcard, volume control can be enabled without touching the audio data. Synchronator in turn can synchronise that volume level with any Hi-Fi system/amplifier that can be externally controlled (RS232/I2C/TCP). In addition, changes in volume level at the amplifier side are synced back.


## Requirements for audio applications

The only requirement for audio applications is that a different device can be set for audio and mixer data.

### Known supported applications
- Music Player Daemon (MPD)
- UPMPD (DLNA/OpenHome)
- Shairport and derivatives (Airplay)
- XBMC (requires small change in sourcecode)


## Requirements for Hi-Fi amplifiers

Obviously, for a computer to control an amplifier that amplifier needs to be controllable. Many amplifiers are controllable via a serial connection (e.g. RS232, TTL, etc). 

Currently only the serial interface is fully supported (thus RS232, TTL, etc). Support for I2C is under development and currently being tested. Support for TCP/IP support is planned in the near future.

### Supported amplifiers/brands
- Cambridge Audio
- Carry Audio Design
- Classe<sup>*</sup>
- Leema Acoustics
- Lyngdorf
- NAD
- Parasound

*) volume changes at the amplifier side are not synced back for this amplifier at this moment


## Features summary

- Synchronisation of volume level changes between Linux and Hi-Fi amplifier
- Http/PHP interface for controlling miscellaneous amplifier options (power, input, etc)

## Untested alternative uses

Synchronator is designed to synchronise the volume level between Linux and Hi-Fi. However, other applications can be thought of also. By running multiple instances of Synchronator, commands between incompatible devices can be translated. A few examples follow:

- With the NAD M50 Bluesound player one can control the volume level of other NAD equipment (Dac or amplifier). While this is nice if you have that NAD equipment, it is less useful if you have an amplifier of another brand. Synchonator can translate commands between these two incompatible devices.

- Once the TCP/IP interface is ready, it should be possible to control your amplifier from within Denon Heos and by extension Spotify Connect. With Denon Heos it is possible to control Denon and Marantz amplifiers via TCP/IP. Since Synchronator will be able to translate these commands, Synchronator can enable this functionality for other brands as well.

## Installation and configuration

For installation check the installation manual or the extended installation manual

For setting the appropriate configuration settings check the configuration manual

## Downloads

Download the latest version from here:
http://muffins.diskstation.me/synchronator-latest.tar.gz

Download the current beta version from here:
http://muffins.diskstation.me/synchronator-beta.tar.gz

Download the configuration library from here:
http://www.hyperrealm.com/libconfig/