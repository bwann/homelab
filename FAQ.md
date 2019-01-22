# FAQ

### Why? Why not a bunch of Raspberry Pis? Why not just use virtual machines
(VMs?)

Mainly I felt like building something one day.  I live in a tiny apartment,
I have no room for a rack of servers nor the associated noise.  And I had a
stack of random leftover hard drives I didn't have a use for.

In my day jobs I frequently deal with bare metal systems in datacenters, so
I want to replicate that in my homelab for better or for worse. This
includes IPMI OOB connectivity, PXE booting, BIOS/UEFI stuff, hard drives
and SSDs, writing tooling for all that stuff, and whatnot.

I don't need raw compute power nor storage, I just need lots of diverse
systems.  And since it's likely to be idle a lot of the time, it should be
low power too.

A while back in 2012 I did take a HELMER drawer leftover from this project,
filled it full of 8x Raspberry Pis (1st gen), and created `tinycluster`.
(https://binaryfury.wann.net/tinycluster/)

### What did this cost?

I'm not really sure.  I wasn't keeping track of component cost when I
originally built it, and I've replaced and expanded things over the years.
I'm hoping by writing docs I can jog my memory and pin down material cost.

I think I estimated around $300 for the HELMER cabinet, all the extra metal,
acyrlic, switch, router, cabling, screws and hardware.  Then what each
individual system cost, in terms of motherboard + RAM + drives cost.

### How much power does it draw?

Last time I checked when it had 9 motherboards was around 260-280 watts
continuously.  It varies based upon how many hard drives vs SSDs are installed,
and types of motherboards.  In summer it can heat up the room so sometimes
I'll turn off blades I'm not actively using.

### How quiet is it?

Pretty quiet, I never notice it.  The hard drives seeking around are about the
only noise that come from it.  Ironically the original goal for this was to 
get as quiet as possible because this is in my bedroom, now I have a
circulation fan and HEPA air filter running all the time which are
considerably louder.

### What kind of motherboards do you use?

There's an assortment, altho usually almost all are embedded Intel Atom
motherboards, either older D2500s or a couple of newer Avoton D2550s. There's
a couple of old spare Pentium E6500 that I bought from surplus that are
hot power hogs.
