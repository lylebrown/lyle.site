---
templateKey: blog-post
title: Utilizing the 10G SFP+ ports on an Aruba S2500 switch
date: 2019-05-23T01:00:10.000Z
description: Unlike some other Arubas, these ports are vendor-locked.
featuredpost: false
featuredimage: /img/switch-3297900_1920.jpg
tags:
  - networking
  - switch
---
![network switch](/img/switch-3297900_1920.jpg)

The Aruba S2500 series make for great homelab switches, if only for the fact that they're so plentiful on eBay for around $100 (depending on number of ports and PoE support). I'm planning to add PoE cameras to the house, along with adding a few wired drops soon, so I upgraded my previous switch to an Aruba S2500-48P. The other huge perk? I'm able to play with 10G networking. And it's not too difficult either, as long as you go into it knowing about compatibility beforehand. We're going to cover three topics that I think everyone should know immediately after buying one of these: SFP+ transceiver support, disabling the uplink ports, and limiting firmware updates if you wish to keep SSH support.

Yes, the S2500 series is vendor-locked. Despite what some posts a search will bring you to suggest, the command to allow unsupported transceivers does not exist on this model, regardless of how far you update the firmware. That means you have to know beforehand which SFP+ transceivers are compatible, which is incredibly difficult to find online. Hopefully this post provides another source of information. After wasting time and money confirming that Cisco transceivers don't work, I found a buried reddit thread that mentioned Molex transceivers work. With that in mind, I bought a few MOLEX 74752-2501, and sure enough, they worked without issue.