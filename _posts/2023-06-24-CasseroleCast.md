---
layout: post
title: "How I made my own Android TV and why you should buy a Google Chromecast"
date: '2023-06-24 04:23:56 +0300'
---

How I made my own Android TV and why you should buy a Google Chromecast
=========================================================

For over a span of two weeks, I had been contemplating the idea of creating a smart TV experience without the annoying advertisements that typically come bundled with Samsung or LG TVs, among others. The concept seemed feasible, especially since I had a Raspberry Pi 3 B+ lying around, and I already had prior knowledge and experience with Kodi, XBMC, and OSMC. Thus, I began by installing OSMC, which had proven to be a stable and reliable media center in the past---after all, the name itself implies "smartness."

However, upon installation, I encountered an issue with the Wi-Fi not being recognized. Undeterred, I embarked on a debugging mission, trying various solutions available. Unfortunately, none of the options I attempted seemed to address my specific problem. Connmanctl, the service responsible for managing Wi-Fi connections on OSMC, appeared to be malfunctioning without providing any helpful logs or error messages. After investing approximately 6 to 7 hours in troubleshooting, I reluctantly gave up and shifted my focus elsewhere. I started researching alternative options and stumbled upon LibreELEC, which seemed like a suitable choice.

Subsequently, I proceeded to install Kodi, Netflix, and HBO Max on LibreELEC. However, when attempting to watch content in 720p resolution, I encountered issues such as audio-video synchronization problems, buffering, and limited bandwidth due to hardware constraints. These were typical bugs resulting from the hardware's limited resources, which were tolerable to some extent. Nevertheless, there was one crucial feature that LibreELEC lacked, and I couldn't imagine living without it---the cast button offered by Google. After much effort, I managed to find a cast add-on specifically for YouTube (not to mention the struggles of obtaining a YouTube API key for Kodi usage). Thus, my quest for the perfect solution continued.

Over the course of a few days, I scoured the internet in search of an add-on that could provide me with the coveted casting experience. I familiarized myself with Google's casting protocol, the Chromecast framework, and even explored "modern programming" techniques with ChatGPT. Eventually, I developed my own add-on. However, I encountered a setback---it lacked certain functions, such as Python-pip, which proved essential on LibreELEC. While I did find an add-on that claimed to provide similar functionality, it did not fully meet my requirements. At this point, I found myself once again pondering my next move.

Driven by determination, I decided to install Android 10 on the Raspberry Pi, which offered a nearly perfect experience. I stumbled upon a repository that provided LineageOS without Google Apps (GApps) and sideloaded GApps separately to avoid performance issues. Without GApps, everything ran smoothly, albeit limited to a resolution of 720x420, which was somewhat acceptable. However, despite this progress, I found myself still yearning for the casting feature and the presence of Android TV apps.

Having heard about Aptoide TV for quite some time, I decided to give it a try. I began filling it with various apps, but some of them failed to function properly without Google Mobile Services (GMS) or GApps. Nevertheless, I believed I had finally achieved the status of a smart TV. But alas, I was mistaken. The lack of app support, absence of Google services, and an overall unsatisfactory TV experience led me to regret my decision.

Curiosity got the better of me, and I began exploring what Google had to offer in the realm of Android TV. To my surprise, I discovered a new model priced at only $50, featuring Google TV---a seemingly perfect solution that encompassed everything I had desired. Could it be true that all my requirements were attainable for just $50? However, I knew I had to come to terms with reality and prove to myself that I could create such an experience.

During my search, I came across a laptop with a faulty keyboard---a Myria laptop (Chuwi Herobook Air)---which was priced at 600 RON or $130. It was a Chinese laptop rebranded with a local brand, but unfortunately, no documentation was available for repairing the keyboard. In light of this, I resolved to transform it into an Android TV setup, determined to prove a point to myself.

Therefore, I began my search for Android x86 options and discovered new and improved solutions designed specifically for laptops. One of them caught my attention: Bliss OS. Bliss OS aimed to provide the Android 12 experience on older laptops, breathing new life into them. Filled with hope, I decided to give it a try.

After installing Bliss OS, I resumed my quest for Aptoide TV. To my surprise and delight, I found apps that offered casting functionality. Finally, I had achieved the smart TV experience I had been longing for. The apps worked flawlessly, including games and IPTV applications. However, the format of a laptop with a broken keyboard wasn't particularly appealing. As a result, I embarked on a dismantling process and ingeniously repurposed a casserole to house the entire motherboard. As a bonus, I even installed a fan to ensure optimal cooling.

![353404331_1005842713926287_1578590621122536440_n](https://github.com/null-p4n/null-p4n.github.io/assets/60641238/147104d6-f3a3-4fe8-83a6-a671f5023607)

![325033751_1005659383937367_2180209348370325790_n](https://github.com/null-p4n/null-p4n.github.io/assets/60641238/02e87472-e159-4dd7-918b-efdd0e67f0ab)

![353590622_287519977071722_9184906694739302040_n](https://github.com/null-p4n/null-p4n.github.io/assets/60641238/c28ae9a2-353c-4096-b62f-9fdd0d43b3be)

Without any hesitation, I proudly introduce to you: CasseroleCast, the smart TV of prehistoric times. However, in all honesty, the overall conclusion I've reached is this: purchasing a Google Chromecast is a reliable and efficient option. It delivers on its promises, offering speed and the features you desire. Alternatively, you can follow my steps and embark on the DIY journey. Cheers!
