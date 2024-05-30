+++
title = 'De-googling, so far'
date = 2024-05-29T21:22:20-07:00
draft = false
+++

Over the past few years, I have tried to gradually reduce or eliminate my use of
Google products and services. It has been difficult to ditch Google's products
in some categories, and in some others, it has been nigh impossible. Here, I
list the services I have tried to find alternatives for, discuss the ease (or
lack thereof) of finding a satisfactory alternative, and rant about my
experience so far.

Before we begin, I feel like I should put a few important caveats out of the
way. First, these are notes from personal experience, and are not a
comprehensive review of alternatives to Google's offerings. If you are looking
for comparisons of alternatives, they are not here. Second, using some of the
alternatives I mention requires having a self-hosted server setup of some sort,
which for many people will be entirely out of the question.

## Search
I have used DuckDuckGo as my primary search engine for the past six or seven
years, and although it has its flaws, it has been adequate. The problem with
DuckDuckGo is that in many cases, it doesn't seem to show a good understanding
of the search query, for lack of a better way to put it. It takes my search
terms too literally. It's saving grace, though, is the 'bang' feature: if you
decide that the results are not what you hoped for and you wish to go to Google
instead, just add a `!g` in your search. This works not just for Google but for
a long list of websites, and I find this feature incredibly handy when I know
beforehand that I want to search a particular website, like Wikipedia, YouTube
or Amazon. 

After reading constant praise for it on HackerNews, I tried
[Kagi](https://kagi.com/) for couple of months last year. Kagi has a lot of
strengths. Just out of the box, it's results are markedly better than DuckDuckGo
and perhaps even Google. Their feature to up-rank or down-rank websites of your
choosing is an absolute lifesaver. Not having to wade through SEO'd junk to find
what I need prevents a lot of frustration. That said, I had two major issues
with Kagi. First, their cheapest subscription tier has a limit of 300 searches
monthly, and I would find myself running against the limit halfway into the
billing period. I would have gladly paid for the unlimited tier, if not for my
second issue with Kagi: privacy-wise, I simply don't believe that a service that
requires login and thus naturally associates all your activity with your
identity is better than a service which can be used without a login. So I'm
sticking to DuckDuckGo for the time being.

## E-Mail
Unlike Search and many other categories in this list, it is not difficult to
find a capable alternative e-mail service. I personally use
[ProtonMail](https://proton.me/mail) and [Fastmail](https://fastmail.com).
Proton positions itself as the privacy-focused option, and claim to have
end-to-end encryption. They bundle e-mail with storage, calendar, VPN and a
password manager at a very reasonable rate. I will continue using ProtonMail as
one of my email accounts, but I don't like the fact it is difficult to use
third-party email clients with their service. Yes, that is due to how they do
end-to-end encryption, and I don't have a reason to doubt their honesty, but is
it *really* end-to-end encryption if you don't have sole ownership and full
control of your keys? 

Besides moving away from Google, I also decided I want to own the whole of my
email address, including the domain name. So, a year and a half ago I started
using Fastmail with a custom domain. A feature of Fastmail I like and use all
the time is masked email, but in fairness a lot of services provide this feature
these days. Unlike Proton, FastMail makes no claims of extreme privacy, but I
lke it because it has a nice and clean web UI and it works with my favorite FOSS
e-mail client on Android.

## Photos
Back in the days when Google Photos had free unlimited photo storage, it was
pretty much unbeatable. Yes, the resolution was capped to 16 megapixels, but
during the time I relied on Google Photos, I didn't have a phone with a camera
capable of much higher resolution. After Google axed the unlimited storage,
other photo storage services seem pretty competitive with Google Photos. At a
glance, Microsoft OneDrive, iCloud, Amazon Photos and DropBox all seem like
options I would at least consider. But I have not tried any of those services
and have no plans to do so, because I self-host a personal instance of
[Immich](https://immich.app/) to store all my photos. In just a couple of years,
Immich has gone from zero to having a very rich feature-set, and although it
doesn't have a stable release yet, it is stable enough for me. Using the
[immich-go](https://github.com/simulot/immich-go) CLI tool, it is a breeze to
import media from your Google Takeout export to Immich as well.

## Drive
Cloud storage of files is an easy switch: there are many, many file storage
providers available with very competitive pricing. For myself, I initially used
a [Nextcloud](https://nextcloud.com/) instance I self-host. I still have some of
my files in Nextcloud, but I found it to be slow when syncing a large amount of
files, so I opted for a simpler solution. All my important files are now in a
directory in my home server, and when I need access to them I just mount the
directory in my laptop with `sshfs`. In case I need a web interface, I have a
[FileBrowser](https://filebrowser.org/) instance running. Side note: I love how
simple FileBrowser is. It does the things I need and not a thing more.

I realize switching to a different storage provider will be more difficult for
people who use Google Drive for collaboration and need to share files often with
other people. Fortunately, in my case what I needed was just to not lose my
files if my laptop goes belly up, and to be able to occasionally access
important files from my phone.

## Calendar and Contacts
Using most calendar and contacts clients with different providers, and switching
between them, is more or less straightforward thanks to the
[CalDAV](https://en.wikipedia.org/wiki/CalDAV) and
[CardDAV](https://en.wikipedia.org/wiki/CardDAV) open protocols. I use my
NextCloud instance as the server for both, and it works flawlessly. On the
client side, I use [Fossify](https://github.com/FossifyOrg) Calendar and
GrapheneOS's default contacts app along with [DavX5](https://www.davx5.com/) to
facilitate the synchronization. I recently discovered that the Calendar and
Contacts apps that come with the Gnome Desktop Environment support CalDAV and
CardDAV as well, so that's neat! I can now view or update my calendar and
contact list from my phone, laptop or the browser!

For people who can't or don't want to self-host a Nextcloud instance, there are
plenty of 'cloud productivity suite' providers that provide file storage,
calendar, contact and email services with a single account. Microsoft Outlook
and Apple iCloud are the most popular ones, but privacy-focused alternatives
like Proton are growing.

## Phone
Let me begin by saying that I am extremely grateful that
[GrapheneOS](https://grapheneos.org/) exists. It is Android but with privacy and
security features that severely limit the capacity of big tech to spy on you.
This includes Google itself, as GrapheneOS by default comes without all the apps
and services that Google includes on a regular Android phone. Optionally, you
can install Google Play Services, but as a regular, 'sandboxed' app: which means
Google has the same privilege as any other app in your phone, and you can decide
what permissions to allow it. But the catch is... well, there are several.
Whether or not you'll find them acceptable depends on where your preference lies
in the privacy-convenience trade-off scale. Because unfortunately, you must
sacrifice one to get more of the other. The first issue is that it only runs on
Google Pixel devices. This is because the GrapheneOS project has a [sizable list
of security and support requirements](https://grapheneos.org/faq#future-devices)
that a device will need to fulfill to be supported, and apparently only Google
Pixel devices do at the moment. If you already have a Pixel phone (like I did
when I first decided to try GrapheneOS), this is not an issue. If you don't
already have one though, you'll have to make a decision about whether you want
to support Google's business by buying a device they produce, even though you're
doing that so you can give Google less control of your digital life. To me, that
feels like an acceptable trade-off.

The other issue is that many apps will either not work, or will be partially
broken. I have used GrapheneOS for a total of 16 months in two stints, 8 months
each in two devices; first a Pixel 3a and now a Pixel 7. Until about 2 months
ago, I used it without the (sandboxed) Google Play Services. In this
configuration, there is a whole category of applications you cannot use: most
prominently, banking and finance apps will just refuse to work. Many apps that
work will have some features broken: notifications in particular will be missing
for a lot of apps. Some apps will keep complaining that your phone does not have
Google Play Services and thus is not supported, but still continue to mostly
work (looking at you, Snapchat). But I found I could still manage. Apps like
Telegram, Signal and Whatsapp use their own notification delivery mechanism, so
they aren't impacted as long as you turn off battery optimization for them. All
the banks I have accounts with have mobile websites that work reasonably well. I
was even able to take trips through Uber's mobile website, which was a pleasant
surprise. The location functionality did not work, but I believe that was due
more to the browser than to Uber itself. I tried to get as many apps as possible
from F-droid, the app store for open-source Android apps. For proprietary apps,
I used Aurora store, which is an alternative open-source client for the Google
Play Store. Not ideal, but better than manually downloading APKs from websites
like APKPure and APKMirror.

About two months ago, in a moment of frustration, I decided to install the
sandboxed Google Play Services and Google Play Store to see if that would
improve my experience. Some things are noticeably better: for instance,
notifications work for all apps, installing new apps is way easier, and I can
install and use some financial apps without issues. It is still far from the
regular Android experience; for instance, apps don't auto-update, you have to
manually go into Google Play Store and update them. This is unfortunate, but you
necessarily lose some functionality when you limit the god-like permissions
Google has on a regular Android device.

Slight tangent: one of my big gripes here is with Android Auto. Contrary to what
the name might suggest, Android Auto is not part of the [Android Open Source
Project (AOSP)](https://source.android.com/). Instead [it is a proprietary
standard](https://en.wikipedia.org/wiki/Android_Auto), and the Android Auto app
on your phone is a proprietary app that has privileged access to your system. If
I want turn-by-turn navigation in my car's head unit out of an open-source maps
app on my phone, that is simply not possible without a privileged, proprietary
app in between to mediate. Before January 2024, it was not even possible to use
Android Auto in GrapheneOS, but now it is at least supported, although it does
depend on the sandboxed Google Play being installed as well.

Every time I am frustrated with the state of things with GrapheneOS, I think
about getting an iPhone, using it without any Google apps, and enjoying the
'just works' nature of Apple products. But then I would be handing over control
of a large part of my digital life to another big tech company, so I haven't
bought an iPhone yet. Apple does like to make a big deal of at least pretending
to care more about your privacy than the rest of Big Tech, but I would rather
not rely on promises if I can, and where possible, use open-source software
stacks I can trust. So I'm sticking with GrapheneOS on my Pixel, at least for
the near future.

## Maps
[OpenStreetMap](https://www.openstreetmap.org) is a fantastic dataset and in
many cases, is better than Google Maps in terms of map accuracy. I use it a lot.
But Google Maps is much more than just the map data: it has client apps across
different platforms with a consistent interface, routing and turn-by-turn
navigation, public transport information, live traffic data, and most
importantly for me, business reviews and opening hours. For the last one,
Google's sheer size means that the network effects are on their side, and I'm
not aware of any effort to create an open dataset of business reviews. All this
means that it is difficult to quit Google Maps entirely. OpenStreetMap-based
apps like [Organic Maps](https://organicmaps.app/) are great and I frequently
use them, but I find myself using the Google Maps website a lot, for tasks like
searching for restaurants to getting an estimate of how long my commute is going
to take.

## Video
The sad reality here is that YouTube essentially has no alternative. Yes, it is
technologically difficult to deliver video to the internet in a way that is
cost-effective, but the problem that is orders of magnitude more difficult is
that of building a critical mass of creators and viewers that the network effect
takes over. All the creators are on YouTube, so everyone goes there for content.
All the viewers are on YouTube, so creators put their videos there. There are
platforms that are trying to provide an alternative, but they are mostly unknown
to the general populace. I have never given serious thought to
[PeerTube](https://en.wikipedia.org/wiki/PeerTube) because I don't know of any
creators I watch that upload their videos to a PeerTube instance. I think
[Nebula.tv](https://nebula.tv) is promising, and a bunch of creators I like
upload their videos on it. I do have a Nebula account but rarely end up using
it, since most videos get uploaded to YouTube as well, and when I open Nebula, I
find myself having already watched all the interesting videos on YouTube.

## Conclusion
At this point in time, it is exceedingly difficult to fully avoid using Google
products and services, and you'll need to sacrifice a lot of convenience in your
attempts to use alternatives. Nevertheless, capable and privacy-friendly
alternatives exist for many product segments in which Google dominates, and I
think it is worthwhile to reduce your dependence on Google where you can. If you
are so inclined, self-hosting can provide even more freedom and privacy. 

