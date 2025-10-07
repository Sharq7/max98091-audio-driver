# max98091-audio-driver
a driver for audio codec max98091.
In the mainline Linux kernel, there is a driver with the filename max98090.c. This supports
max98090 completely but does not support max98091. Although both the codecs have a lot of
similarity, but max98091 has support for TDM and therefore extra microphone channels.

The driver in mainline linux kernel, has a compatibility flag and of_device_id both indicating
support for max98090 and max98091, BUT it is not so. max98091 is not supported, as the routes
and widgets are not coded in the max98090.c code.

An attempt would be made to mainline this code. But for the moment it is present here. To
test it or run it, just copy paste this file to max98090.c in the linux kernel and build the
module.
