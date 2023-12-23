
# Overview

This document explains the process of installing Zynthian in a [reTerminal](https://www.seeedstudio.com/ReTerminal-with-CM4-p-4904.html). The reTerminal is an embedded device which have a Raspberry Pi CM4, an LCD display, a multi-touch screen panel, some buttons and a very nice case. My model is the CM4 4032, so I have **4 GiB of RAM and 32 GiB of eMMC** storage.

![Image: SeeedStudio reTerminal (c)](reterminal.jpg)

## Some considerations

One important thing to note with this device is that it **does NOT have any sound interface** (at least, not exposed directly). Talking about installing Zynthian, this is a big issue. You can, nevertheless, use the exposed 40 pin header to add a RPi sound module, or, as in my case, use an external USB audio interface. It works without any problem.

On the other hand, as you will see in a moment, this device does not use the SD card to boot up the system. This means that the **installation procedure is a bit more complex** than with a normal Raspberry Pi. But not much more :) .

Let's begin!


# Zynthian installation

Of course, and first of all, you need to **download the Zynthian OS image** from the official web page. It's around 8 GiB (12/2023), so it may take a while to download (but you won't sit and wait, there is work to do!).

* [Zynthian OS last stable image](https://os.zynthian.org/zynthianos-last-stable.zip)
* [Zynthian.org Software](https://zynthian.org/#software)

Now, in order to flash the operating system into the eMMC, you need to boot it in a special mode. To do so, you need to remove the back cover and the heatsink, and flip down the boot switch inside. Then, after installing the drivers in your PC/Mac, connect the reTerminal to your host using the USB-C cable. If everything is ok, your host will see it like an USB drive. The whole process is very well explained in the official Wiki, here:

* [Flash Raspberry Pi OS/ 64-bit Ubuntu OS or Other OS to eMMC](https://wiki.seeedstudio.com/reTerminal/#flash-raspberry-pi-os-64-bit-ubuntu-os-or-other-os-to-emmc)

> NOTE: The back cover has two tabs around the middle screw holes. Once the four corner screws are removed, these tabs keep the cover from being released. You may need to insert something from both sides to pry them (with care) and be able to quit the cover. I did remove these tabs for easy future access.

Once the reTerminal is in *flash mode*, and you unzipped de Zynthian image, you can use the [Raspberry Pi Imager](https://www.raspberrypi.com/software/) to flash it. Select "Choose OS > Use Custom" to use the provided Zynthian `.img` file, and also select the eMMC device as destination. Press write and wait. In my case, it took around 15-20 minutes, so it's time for a coffe break :) .

## Entering 'flash mode'

## Writing the Zynthian image

# reTerminal drivers

# References

* [Zynthian](https://zynthian.org/)

* [Seeed Studio shop: reTerminal](https://www.seeedstudio.com/ReTerminal-with-CM4-p-4904.html)
* [reTerminal Wiki](https://wiki.seeedstudio.com/reTerminal/)
* [reTerminal: installing an OS to the eMMC](https://wiki.seeedstudio.com/reTerminal/#flash-raspberry-pi-os-64-bit-ubuntu-os-or-other-os-to-emmc)
