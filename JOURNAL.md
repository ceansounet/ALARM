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

# August 18th: Continuing the BOM - bad surprises

Due to the recent (and crazy) import tax increases in Europe, I had the bad surprise at checkout to see that I had for 75€ of products, about the same in import taxes, so I decided to reduce the scope of the project a bit, and limit myself to a 60$ all included budget.
But not to worry, I won't sacrifice anything important ! My changes are mostly using components I already own, so first, I removed the acrylic circle, I also removed the buttons, to use keyswitches instead, I'm going to use 2 encoders instead of 3, to harvest them from
my hackpad, and I will also be harvesting the oled screen from there. I am switching to a raspberry pi pico 2 that I got at HC Outpost, it has 26 open gpio pins, and I plan on using all of them (surely this isn't a bad idea, surely this isn't foreshadowing...)
Now all that I'm left with is this :

<img width="1184" height="788" alt="image" src="https://github.com/user-attachments/assets/1c770f9f-9eac-4463-bc06-90de68493133" />

Which are the motors, power board, amplifier, speaker, ring backlight, hall effect sensor, and GPS module.

**Total time spent: 1.5 hour**

# August 18th: Started CAD

It's 10pm and I should go eat, I started the cad by fetching every part from grabcad, and making them myself when I couldn't find them, then I organized them in the way I envisioned, and put constraints to make it feel more secure, next step are :

1- make at least a sketch of the design of the main case, I am looking for mid century vibes

2- research and design the enclosure for the speaker, as I have learnt it can have a big impact on sound quality and power

3- make all of the brackets and holders for the different parts

4- integrate all of the parts into the case nicely, making sure assembly stays simple

5- make the front plate and clock face, and if I have the motivation, I'd like to use a technique called thermoforming, to make a round grill around the front, like this inspiration from Zion Brock.

<img width="740" height="416" alt="image" src="https://github.com/user-attachments/assets/ee13edc6-9b5a-4f1b-a3a4-3e7f3b36de35" />


<img width="976" height="548" alt="image" src="https://github.com/user-attachments/assets/0b1a3edb-2d64-4a22-a587-7b393ba2d772" />

**Total time spent: 2 hours**

# August 19th: Really good progress in cad

I see it, the vision, it's coming to life! I made the whole case body for the ALARM, as well as groves for assembly and alignment, might add one on top if needed. I also added the push buttons on top, looking really nice, the design is a bit challenging with all of the different angles and parts, but it's coming together nicely. I think the front plate will be made in 2 parts, one is attached to what I call the sled, which houses all of the parts, and the sled screw into the frame, 2 screws at the top, one on the bottom, and then the thermoformed grill comes in with magnets that attach to the screws underneath, which makes it swappable, different colors for different moods.

Next step is researching accoustics, and then cadding the sled with the speaker housing as needed.

<img width="1034" height="610" alt="image" src="https://github.com/user-attachments/assets/3f857e62-400a-4160-af92-7e1fa7218d95" />

**Total time spent: 2.5 hours**

# August 20th: Continuing CAD + acoustic research

I spent an hour researching how to make the speaker sound good, and translated that into CAD with a chamber that goes behind it

<img width="768" height="1024" alt="image" src="https://github.com/user-attachments/assets/e35246b3-156b-44fc-8485-12b94e086969" />


**Total time spent: 1 hour**
