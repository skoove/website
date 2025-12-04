+++
title = "resisting the social media restriction"
date = 2025-12-04
+++

On the 10th of December, many services will be required to restrict access to Australians under 16 years of age, or face punishments. This is a huge breach of anonymity, privacy, and security, as we are being asked to trust corporations with our personal documents to verify that we are over the age of 16, providing them information that can be easily sold, or used to target us with advertisements. Luckily, zero thought has been put into the implementation (if you could not tell by the privacy issues), and it will be incredibly easy to circumvent.

Everyone will be affected by this, this is not just for under 16s wanting to access restricted sites, this is for *anyone* who does not want server their personal data on a platter to a corporation, which I would hope is most people!

## some terminology
I will use some terms that could be unfamiliar to you, I will quickly explain what you need to know, and link extra resources for them.

An **IP address** is the identifier for machines on the internet, they take the form of `xxx.xxx.xxx.xxx` for IPv4 and `0123:4567:89:abcd:efgh:ijkl` for IPv6

<https://en.wikipedia.org/wiki/IP_address>

A **DNS Server** is a server that tells your computer what IP address to go to when you put in the domain name of a service, for example, `example.com` may evaluate to `23.215.0.136`.

<https://en.wikipedia.org/wiki/Domain_Name_System>

## what services will be effected
[According to the ABC](https://en.wikipedia.org/wiki/Domain_Name_System), the following services will either need to put restrictions in place, or be blocked:
- Facebook
- Instagram
- Snapchat
- Threads
- TikTok
- X (Formerly Twitter)
- YouTube
- Kick
- Reddit
- Twitch

This list will almost certainly expand.

The following services **will not** be effected

- Discord
- GitHub
- Google Classroom
- LEGO Play
- Messenger
- Pinterest
- Roblox[^roblox]
- Steam and Steam Chat
- WhatsApp
- YouTube Kids
- Linkedin

[^roblox]: what the hell???? why restrict everything else but not notorious pedo haven roblox??

## how will it be implemented
Services need to take steps to verify identities, in practice this means sending things like licences, face scans, or other info to them. If a service *does not* want to do those things, they may just block access to Australians, and if they don't want to do that, the government may take action against them, such as legal challenge, or just trying to block them using means they control.

We actually have a good example, the government already blocks lots of sites! they even made us a nice list:

<https://www.teqsa.gov.au/blocked-illegal-cheating-websites>

If you go to those sites, you may be redirected to that page. This is implemented using **DNS blocking** and is very very easily circumvented.

## DNS blocking
Normally, when you ask a DNS server to resolve and IP for you, it sends you the correct one, however if the government asked your ISP to block a site, it sends you to a access blocked page (for example on my phone where I have not bothered fixing this, I cant go to piracy websites).

Fortunately, this is super easy to get around, just do not use your ISP's DNS server, I use `1.1.1.1` (dont put that in your browser it redirects to an ad for Cloudflares VPN, which we will get to later). Look up the instructions for your operating system, it is generally super simple.

## geoblocking
Since it is on services to implement the restrictions, unless they simply don't (again, stellar planning from the government), almost all the restrictions will be done like this. Geoblocking works by trying to determine the location of your device.

The first method is simply by your devices IP address, each country is assigned a range of IP addresses, so a service can just check the address, then block it, or restrict it if it is from Australia.

Another method is using the ping (the time taken for a connection to reach the server from your device), ping is very predictable, so can be used to estimate the location of a device, I don't think this is use too much, but I cant be sure, you could definitely figure out if it is an Australian connected as we are so big and separated from other countries, especially if you have servers all over the world. You may have used this method yourself if you play online multiplayer games! For example if I see someone with a ping of around 70ms I know they are probably in Singapore.

The least likely method is just using your devices GPS, just don't give things location permissions :P, though this could become a problem when more countries start implementing restrictions, but not yet.

### circumventing
Both the IP based blocking, and ping based can be circumvented by a VPN or a proxy. However both do put your information in the hands of potentially untrustworthy people.

#### VPN
A VPN creates a virtual network between you and some other network, in this case the wider internet, A VPN passes your traffic though their server, then to the internet, meaning both your ping and IP have changed! However some services opt to simply block VPN servers from accessing their service. As for which one to pick, just pick Mullvad, not nord, not proton, not cloudflares, just use Mullvad

**ABSOLUTELY DO NOT USE A FREE VPN**

You are passing *all* of your traffic to them, a free VPN service is almost definitely selling your data.

<https://mullvad.net/en>

#### proxies
Proxies are similar to VPNs with 2 major differences

1. You ask the proxy to make the request for you, rather than it just passing it on to the destination.

2. You can probably trust proxy providers a bit less

If VPN services end up required to block Australia, we are left with just proxies to freely access the internet, lets hope we never get to that point

My friend Alisa has a great post on setting up proxies!

<https://axlefublr.github.io/proxies/>



If I made a mistake, or there is some other reason you would like to contact me, please email me!

<zie@skoove.dev>

---

