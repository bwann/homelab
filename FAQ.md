# FAQ

### Why? Why not a bunch of Raspberry Pis? Why not just use virtual machines (VMs)?

Mainly I felt like building something one day.  I live in a tiny apartment,
I have no room for a rack of servers nor the associated noise.  And I had a
stack of random leftover hard drives I didn't have a use for.

In my day jobs I frequently deal with bare metal systems in datacenters, so
I want to replicate that in my homelab for better or for worse. This
includes IPMI BMC/OOB connectivity, PXE booting, BIOS/UEFI stuff, hard drives
and SSDs, real network routers and switches, writing tooling for all that
stuff, and whatnot.

I don't need raw compute power nor storage, I just need lots of diverse
systems.  And since it's likely to be idle a lot of the time, it should be
low power too.

A while back in 2012 I did take a HELMER drawer leftover from this project,
filled it full of 8x Raspberry Pis (1st gen), and created `tinycluster`.
(https://binaryfury.wann.net/tinycluster/)

Plus the form factor of the HELMER makes it fun to come up with ideas to fit
things into a compact space.

### How big is it?

The HELMER cabinet is about 11" wide, 27" tall, and 17" deep.  It fits
perfectly under an IKEA desk if you have one.  Other than the power and
Ethernet cables coming out the back, it's pretty self contained and stays
within this footprint.

### What did this cost?

I'm not really sure.  I wasn't keeping track of components and hardware when I
originally built it, and I've replaced and expanded things over the years.
I'm hoping by writing docs I can jog my memory and pin down material cost.

I think I estimated around $300 for the HELMER cabinet, all the extra metal,
acyrlic, cabling, screws, hardware, and including the 16-port switch and
router.  Then whatever the individual system cost, in terms of motherboard +
RAM + drives.

Aside from the electronics, I think the several feet of aluminum angle stock
was the most expensive part.

### How long did it take to build?

I did the entire initial cabinet modification and a couple of working blades
in a Sunday afternoon + evening.  The power wiring is what takes the longest
time, but you only have to do it once.

### How much power does it draw?

Last time I checked when it had 9 motherboards was around 260-280 watts
continuously.  It varies based upon how many hard drives vs SSDs are installed,
and types of motherboards.  In summer it can heat up the room so sometimes
I'll turn off blades I'm not actively using.

An individual Avoton C2558 blade + SSD draws about 12.5 watts, and an older
Atom 2550 + 3.5" HDD + 2.5" SSD draws about 28 watts.

### How quiet is it?

Pretty quiet, I never notice it.  The hard drives seeking around are about the
only noise that come from it.  Ironically the original goal for this was to 
get as quiet as possible because this is in my bedroom, now I have a
circulation fan and HEPA air filter running all the time which are
considerably louder.

### What kind of motherboards do you use?

The main thing is using mini-ITX form factor, as they're the only thing that
fits with room for the drives.  There's an assortment, altho usually almost
all are embedded Intel Atom motherboards, either older D2500s or a couple of
newer Avoton D2550s from Supermicro. There's a couple of old Pentium E6500s
in there too that I bought from surplus.

Some motherboards have built-in 12 VDC inputs which could save using a PicoPSU.
I considered them, but then I wouldn't be able to power dual hard drives.
