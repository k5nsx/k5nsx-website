---
title:  "K5NSX High Altitude Balloon - July 2026"
date:   2026-06-21 22:30:00 -0500
author: ae5au
categories: Balloons
tags: balloons hab
---
K5NSX will be coordinating a high-altitude balloon launch. The date is Saturday, July 11th.

EDIT: We will meet in Carlisle, AR at 9:00 AM CDT. Launch shortly afterward.

Talk-in / chase simplex on 146.55 MHz FM

The payloads for this launch will be:
* Primary tracker
  * K5NSX - Horus Binary v3 - 432.5 MHz
  * K5NSX-11 - APRS - 445.975 MHz ~ every minute
* Secondary tracker - Horus Binary v3 on 70cm
  * AE5AU - Horus Binary v3 - 432.6 MHz
* Raspberry Pi camera - storing images to microSD while also sending preview images via 915MHz LoRa


We need two main types of assistance...either (or both) would be greatly appreciated.
1) Tracking from a home/fixed station.
1) Chasing from a mobile station during the balloon flight.

[Horus Binary](https://github.com/projecthorus/horusdemodlib/wiki/) is a protocol specifically designed for tracking balloon payloads. To receive it requires something capable of receiving upper sideband on 70cm. This can be as simple as an RTL-SDR or it could be any ham rig or receiver and a way to get audio into a computer (internal USB or an audio interface). A few current options that you might already have:
* Quansheng UV-K5 with alternate firmware and AIOC interface
* Kenwood TH-D74A / TH-D75A
* Icom IC-705
* Yaesu FTX-1
* Yaesu FT-991(A)
* Icom IC-7100
* Icom IC-9700

There are 3 options for software to decode Horus Binary
* [webhorus](https://horus.sondehub.org/) - browser-based decoder that can accept sound card input or directly control an RTL-SDR. This is the simplest, but also the most finnicky, option.
* [Horus-GUI](https://github.com/projecthorus/horus-gui) - Graphical application. Probably the best option if you have a home station already setup for digital modes.
* [horusdemodlib](https://github.com/projecthorus/horusdemodlib/) - Python library for headless decoding and also running multiple decoders on a single SDR receiver. Also can integrate with [Chasemapper](https://github.com/projecthorus/chasemapper/) for mapping during the chase. I'll share some options for how to easily configure this setup on a Pi or similar machine in the next week or so.

All of these decoding options feed data to [SondeHub Amateur](https://amateur.sondehub.org/) which is where we will be tracking and coordinating the recovery efforts.

Please reach out via email or the [NSX Discord](https://discord.gg/YHz6zyBE4j) if you are interested in participating in any way. I hope this will be the first of many launches like this.

73, Luke - AE5AU
