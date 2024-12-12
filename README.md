# homelab
Self-documentation repo for my own sake along the journey of setting up a nice homelab.

First of all I have to say that I am not expert in networking, containers, storage, linux... so please be aware of that everything that you see here does not come from me, but from many sources including youtube videos, forums, knowledgeable friendships and general willingness to get things working.

This repo is a way for me to documentate the set up of my new homelab after having a working set up for a couple of months, but not the most reliable in the way it is set up and what and how the services that I have are running.

My current set up is a single machine running TrueNAS as storage and supervising roles, with a single 1TB HDD stripe VDEV hosting all my data while having some docker containers installed through the ix-systems app center and other ones had been set up directly on top of the shell of TrueNAS using docker compose. Obviously this is not a desirable set up but it was the way for me to get into it and see exactly what I wanted and how everything really works (as i said before my knowledge in this is basic).

And so we begin: After a lot of research and experimentation thanks to a kind of performant minipc that i got my plas is to totally rebuild the TrueNAS machine with a 2x 2TB HDD's mirror and use it explicitly for storage only as my tank for all my data and pass this through to a Proxmox VE installed in my minipc which will run all my apps and services.

What services will I be running, well I think is more or less obvious but of course we will have an Arr Stack running through a gluetun VPN service using PIA, jellyfin and jellyseer to make use of what the stack is going to provide :$, pihole stance, of course portainer to make the managing of all of this super easy, photo backup software like immich or photoprism and a dashboard like homepage to manage everything easily. Also I need to add that all of this without remote connection intentions, i want this to be, as my current set up is, only accesible inside my house, i dont have the need to share this services with anybody and let alone access them when im not there.


