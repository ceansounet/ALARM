---
title: "ALARM"
author: "Gwendal B"
description: "An alarm clock that uses analog buttons and hands, with the added accuracy of GPS based time"
created_at: "2026-03-20"
---

# August 18th: Started planning the BOM and making the repo

Spent about 2 hours researching about different coaxial stepper motors, microcontrollers, and gps modules. Searched for the best deals on aliexpress, I am still unsure about the power situation, as the esp32 is 3.3v, and basically all of the other components are 5v,
and I am also planning on adding 2 18650 Li-on batteries to get it running even in case of power cuts, I will do more research on this today (after I sleep, it's 2am rn). 

<img width="784" height="920" alt="image" src="https://github.com/user-attachments/assets/eafb391b-1b28-4df1-b7d9-2c126ab7d1dd" />
<img width="790" height="940" alt="image" src="https://github.com/user-attachments/assets/95d0585f-1cb3-434d-95f4-3205dec3906b" />

I then proceeded to not go to sleep, and to finish the BOM xD, so I spent another hour researching power paths, speakers, microcontrollers (again), and so I chose to use an esp32 S3-N16R8, because it has a lot of headroom for saving music, and a lot of available pins.
I also added a 40mm speaker, but I don't know how well it will sound, I searched a lot for better options but at that size, nothing seemed very good (also IDK anything about speakers, and half of them didn't have info in the description).
I added a MAX98357A driver for the speaker, it seemed to be made for it because it has all the right specs.
For the power I will use 2 18650 batteries (that I already own) in 1S2P, with a boost converter, on an fully integrated UPS board, that does charging and interrupted power, in case of emmergency.
And finally I added an acrylic round pannel, to make the clock nicer, idk if I will actually use it tho, if it looks good.
To round things up I sent my whole BOM to claude to try and identify any incompatibilities or oversights, and it found that A4988 wouldn't work with 5v (only 8.2-45v) so I will probably switch to DRV8836, because I already have those on hand. but it might make firmware a bit harder.

**Total time spent: 3 hours**
