---
layout: post
title: ESP8266 And Platform IO
---

I am writing this little introduction because I found some great tools, that I think that every IoT or home automation enthusiasts should know and experience.

Firstly i want to introduce you a neat little thing..

**The ESP8266**

![ESP8266](/images/2016/03/esp8266.jpg)

ESP8266 is a System-On-a-Chip(SoC). The module by itself, is a fantastic platform and tool, but for new comers of electrical and software engineering, it might not seem so accessible. Fortunately there are some really cheap development boards out there, most of them is based on the ESP-12 chip. To be more specific the improved ESP-12E's and ESP-12F's([module family](http://www.esp8266.com/wiki/doku.php?id=esp8266-module-family)). The development boards has integrated USB to TTL debug interfaces, so theres is no need for external hardware and wiring just to program them, which may be quite a hurdle to some.

I recommend modules like these:

- [Witty cloud](http://www.aliexpress.com/af/witty-cloud.html)
- [NodeMCU v3](http://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20160403065815&SearchText=NodeMCU+v3).

To ease the process of developing with this module, i will also encourage you to try out [this](https://github.com/cnHeider/pio) little project, that I also made a little [write up](http://cnheider.net/2016/04/03/ProbeIO.html) on. The project was build using..

**The PlatformIO**

![PlatformIO](/images/2016/03/platformio.png)

PlatformIO is an ecosystem for IoT development, it comes with integration for IDE such as: Arduino, Atom, CLion, Eclipse, Emacs, Energia, Qt Creator, Sublime Text, Vim, Visual Studio. The suite can be utilised with great pleasure, for a large variety of other embedded systems, other than ESP8266 module.

The most noticeable feature of the PlatformIO ecosystem for me, is the so well implemented PlatformIO IDE, an integration for Atom environment. The integration include a serial monitor with the atom environment, automation of all kinds of tasks such a deployment of new builds and fetches of missing dependencies.

I myself has been hesitant towards atom and still is.. Due to my very slow i3 processor, my whole linux setup is lightweight. See my post on [my setup](http://cnheider.net/2016/03/06/dotConfig.html). The [Atom](http://atom.io) editor since back when I spun it up the first time has been slow and in need of some real changes towards speed and responsiveness. I arrived this conclusion times multiple times, and ended up discarding it every time. This time I might just stay for good, largely affected by the PlatformIO plug-in suite.

A another neat little feature is that the command ```platformio run``` supports Over-The-Air(OTA) updates, the build flag ```--upload-port``` allows upload ports to be other than some file descriptors of your system, it allows upload ports to ip-addresses and domains of your network.

Example:

```bash
platformio run --target upload --upload-port IP_ADDRESS_HERE or mDNS_NAME.local
```

Some ressources, where you get additional information:

- [ESP8266 SDK](https://github.com/pfalcon/esp-open-sdk)
- [Arduino like syntax for ESP8266](https://github.com/esp8266/Arduino)
- [ESP8266 Community](http://esp8266.net/)
- [Community site](http://www.esp8266.com/)
- [PlatformIO](https://github.com/platformio)
