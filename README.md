# homelab

This is ikeacluster, my take on using an IKEA HELMER filing cabinet and
turning it into a nearly silent, low power rig for a home compute lab.  It supports
up to 10x mini-ITX motherboards, a mixture of 20x 2.5" or 3.5" hard drives
and/or SSDs, all running off a large ATX power supply.  Best of all, it has 
wheels and fits under a desk!

The HELMER form factor is sorely unappreciated for stacking up systems so I've posted my photos
and designs to hopefully inspire other people.

![HELMER](./img/7271891250_ea68a6c65b_n.jpg) ![ikeacluster](./img/7862072998_a28363d610_z.jpg)

I first built this in 2012 and various bits have changed and expanded over
time, nevertheless it's been running nonstop 24/7 for over ten years now!

### What I use this for
This wasn't built for fake internet points, I actually use this. This runs some of my own 24/7
self-hosted services but also as a playground for rapidly testing short-lived proof-of-concepts
for work, learning what the new hotness is, taking a sledge hammer to it, and learning to fix it.

Some of the many projects and software I've ran on this:

- Acts as datacenter rack with top-of-rack switch in a layer 3/BGP topology with other "racks"
- Bare-metal PXE installations of CentOS 6/7/8/9 Stream/10 Stream, Ubuntu 18/24, even OpenIndiana
- Proving out new IPv6-only PXE kickstarts, testing enhanced logging patches to installers
- Anycast VIP injection via BGP
- L3 DSR load balancing, multi-link ECMP load balancing
- BIOS/UEFI firmware, BMC updates and tooling
- Chef servers
- OpenTSDB metric collection and HBase storage
- Facebook Scribe, Loki, Grafana, Prometheus backends
- Kubernetes, k3s cluster testing
- Using Varnish for RPM and Apt package mirrors and caching
- Container and artifact distribution
- Private TLS/SSL CA, SSH certificate CA, Hashicorp Vault
- Netbox
- Docker containers

Generally this is an IPv6-only environment with the exception of HBase which stubbornly still
needs IPv4. Hardware comes and goes as motherboards and drives fail, or I need to focus on new
technologies, or I get some sweet eBay deals.

### Build your own

Over time I hope to put together a bill of materials and halfway decent
construction doc here so people can build their own if they want. IMHO this is way
more practical than all the IKEA LACK "racks" people seem to be fond of. This is published
on Github to try this as a medium and because all of the pages don't fit into my blog
website well.

There's room for quite a bit of improvisation and loose workmanship in
building this. Even if I built another one, it probably wouldn't be exactly
like this one.  Over on the flickrs I have a bunch of photos as this was
being built and some of the design iterations I went through.

**Lasers!**
Cutting and drilling the acrylic "blades" for motherboards+drives is a time
consuming process.  I did the originals by hand and they all had jagged edges,
but perfectly usable.  I recently got my hands on a laser cutter, so I
designed a file using Lightburn to cut out the blades perfectly.
See the Files section below or go browse through the `laser/` directory.

### Build table of contents
* [FAQ](FAQ.md)
* [HELMER cabinet assembly](HELMER.md)
* [Motherboard blades](blade.md)
* [Doors](door.md)
* [Networking](network.md)
* [Power distribution](power.md)

### Files
* [Board - 2x 3.5" / 3x 2.5" drives (SVG)](laser/ikeacluster-board4-23x22x32.svg)
* [Board - 2x 3.5" / 3x 2.5" drives (Lightburn)](laser/ikeacluster-board4-23x22x32.lbrn)

### Links
* [flickr - Initial and ongoing build photos](https://www.flickr.com/photos/binaryfury/albums/72157629900950858)
* [flickr - PSU, distribution, and fan upgrade](https://www.flickr.com/photos/binaryfury/albums/72157631186725716)
* [Blog build commentary](https://binaryfury.wann.net/ikeacluster/)
* [My website!](https://binaryfury.wann.net/)

### Fully populated and running
![](./img/24378251929_89eb8c93ee_z.jpg)

![](./img/46784165712_11b6b6ab40_z.jpg)
