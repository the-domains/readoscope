---
inFeed: true
hasPage: true
inNav: false
inLanguage: null
starred: false
keywords: []
description: ''
datePublished: '2016-02-08T06:28:12.824Z'
dateModified: '2016-02-08T06:28:03.858Z'
title: 'Thresholds in computing: Part 1 – What is a threshold?'
author: []
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
sourcePath: _posts/2016-02-08-thresholds-in-computing-part-1-what-is-a-threshold.md
published: true
url: thresholds-in-computing-part-1-what-is-a-threshold/index.html
_type: Article

---
_(Part 1 in [a series of posts][0] on small-form-factor computing)_

The word threshold gets used a lot, especially in computing and technology. It doesn't always mean the same thing. Let's examine, non-academically, what it means in some contexts, and particularly how it applies to mainstream computing.

## Threshold voltage

For computer engineers, the threshold voltage is the voltage at which a significant current flowing through a semiconductor is formed. This threshold voltage is important because the voltage across the connection needs to be significantly higher for the circuit to operate reliably---it would not be desirable if pressing Enter does not reliably tell your PC to create a line break, for instance. At the same time, we only want to use just as much voltage as is needed, so that we can save on power consumption. This is a big field of study: [Near-threshold computing promises an energy reduction][1] of 100× or more.

## Bandwidth/latency thresholds

In software, programmers who work at a sufficiently low level (e.g. optimising programs by tweaking memory/cache use) will also be familiar with thresholds. A computer has varying levels of storage, arranged here in order of increasing distance from the brains of the PC---the CPU:

L1 and L2 data caches, which have capacities up to 256KB typically, latencies on the order of 1 ns, and theoretical bandwidth in tens of GB/s.

L3 caches of about 8MB, with latencies close to 10 ns, and theoretical bandwidth about a third or less of L1 cache.

Main memory, which can be 2--16GB or more in size, with response time on the order of 100 ns, theoretical bandwidth up to 25 GB/s.

Solid state storage (SSDs), with capacities in hundreds of GB, latency on the order of 1 ms or lower, and bandwidth between 0.1--1 GB/s.

Hard disk storage, with capacities up to 4TB per disk, latency on the order of 10 ms, bandwidth around 0.1 GB/s.

The numbers above are ballpark figures based on technology readily available to consumers.

The general trend as we go from near storage to far storage is a decrease in latency, an increase in bandwidth, and an increase in capacity. Dark\_Shikari \[describes in his x264 development blog\](http://x264dev.multimedia.cx/archives/201 "The other hidden cycle-eating demon: code cache misses") how he compressed a function binary so that it fits in L2 cache, avoiding a cache miss that would force the CPU to go to main memory instead. The result is a 10% speedup in the relevant function, shaving milliseconds off its runtime. This does not sound like a lot, but for low-level functions that get called many tens of thousands of times in the encoding of a video, it quickly adds up.

## Thresholds in user interfaces

In interface design and user experience (commonly abbreviated [UX][2], thresholds are less obvious. A well-known example would be multi-touch capacitive touchscreens, and the interfaces they have enabled. Touchscreens are not a new technology; they have been around since the '60s. But they did not cross a threshold until the iPhone and other early smartphones were released with multi-touch capacitive touchscreens. Prior to that, touchscreen interfaces were still very much button-based, since swipe gestures were difficult to recognise, and often not very reliable.

## What is a threshold?

The experience of freezing water is one that science students would be familiar with. As the temperature of water under normal conditions approaches 0°C, water begins to freeze, and ice begins to melt. Once past this temperature point, water does not behave very differently; water at 1°C behaves very similarly to water at 5°C or 10°C, and likewise with ice at --1°C, --5°C or --10°C.

Here, 0°C is the freezing threshold of water. The word "threshold" [derives from the Old English _þrescold_, describing a "doorsill, point of entering"][3]. A threshold is a point at which **the behaviour (of a system or device) enters a markedly different mode**.

## Thresholds in small-form-factor computing

We are familiar with the idea of the thin-tablet/thick-laptop threshold: tablets are always thin, and laptops are always significantly thicker. The key differentiator here lies in the thermal dissipation rate of the chip, the rate at which the chip produces and dissipates heat. For tablets to remain thin, the chip must be capable of dissipating all its produced heat without any assistance (or at most assisted by a metal chassis), without growing alarmingly hot. If it is unable to do this, the device will require a cooling heatsink and fan, which adds significantly to the device's thickness---even the thinnest fan-assisted heatsinks are at least a few millimetres thick.

Device manufacturers know this. They design their products and integrate these chips without exceeding a certain thermal dissipation rate. This number is known in geek parlance as [TDP][4]---The _Thermal Design Power_, sometimes called _thermal design point_, is the maximum amount of heat generated by the CPU that the cooling system in a computer is required to dissipate in typical operation. For tablets, the TDP threshold is about 8W. It is why a 10W adapter is sufficient for just about any passively cooled tablet.

What about in desktops? This is the Dell Inspiron 518, in 2008\. It's the oldest image that Google Images turns up, but desktops still looked much the same in 2003:

\[!\[Dell Inspiron 518 (2008), CNET\](http://writoscope.me/wp-content/uploads/2013/12/dell-2008.jpg)\](http://writoscope.me/wp-content/uploads/2013/12/dell-2008.jpg)
\_Dell Inspiron 518 (2008), CNET\_

And this is the Dell Inspiron 660s, in 2013:

\[!\[Dell Inspiron 660s (2013), Amazon\](http://writoscope.me/wp-content/uploads/2013/12/81KXQP7EfeL.\_SL1500\_-1024x905.jpg)\](http://writoscope.me/wp-content/uploads/2013/12/81KXQP7EfeL.\_SL1500\_.jpg) \_Dell Inspiron 660s (2013), Amazon\_

It is striking to note _how little_ has changed. In the past 10 years, the chips have changed a lot; performance has increased 10×. But the desktop still looks much the same, inside and outside.

Why?

Let's [look at our][5][fish][6] again. What else is similar between those two pictures?

Space. Empty space. Lots and lots of it.

Empty space alone is not bad; [it is a critical element][7] of graphic design, after all. But here, in the desktop, do we really need it, and if we do, how much do we really need?

Let's play with thresholds. Let's toy with various factors in desktops **that we can control**, and see what happens. Let's see if we cross any thresholds. 

\_On to [Thresholds in computing: Part 2 -- Does it need to take up so much space?][8]

[0]: http://writoscope.me/tag/threshold/
[1]: http://www.michigancmes.org/papers/sylvester_blaauw8.pdf
[2]: http://en.wikipedia.org/wiki/User_experience
[3]: http://www.etymonline.com/index.php?term=threshold
[4]: http://en.wikipedia.org/wiki/Thermal_design_power
[5]: http://grammar.about.com/od/classicessays/a/Look-At-Your-Fish-By-Samuel-H-Scudder.htm
[6]: https://readtapestry.com/s/YuyuuzQO8/?p=109
[7]: http://boagworld.com/design/why-whitespace-matters/
[8]: http://writoscope.me/2013/12/20/thresholds-in-computing-part-2-does-it-need-to-take-up-so-much-space/