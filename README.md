# HexaLED
Modular hexagon ceiling lights using 24 V CCT COB LED strips

*(yes, I need to hide power wires, I know 😅)*

![Almost done](Photos/Project/Final_product.jpg)

## Summary
I saw many of these "Hexagon LED" ceiling lights but none that would fit my needs:
- 24 V DC powered
- dimmable warm white / cold white (CCT)
- COB LEDs
- low profile
- able to be controlled locally via Home Assistant
- freely extendable / modular

## How it started / bill of materials
1. Controller: I first wanted to build a multi-channel N-FET driver board that would be able to control 10 output channels (for 5 CCT strips). Then I found out about these fancy thingies: [QuinLED An-Penta-Deca](https://quinled.info/quinled-an-penta-deca/) and [QuinLED An-Penta-Plus](https://quinled.info/quinled-an-penta-plus/). Well the first step was easy: add to cart 😂
2. Power supply: [ERPF-400-24 from MEAN WELL](https://www.tme.eu/si/en/details/erpf-400-24/led-power-supplies/mean-well/) looked ok for me with some extra power leftover.
3. LED strips: I decided on these: [AliExpress - FCOB CCT LED Light Strip 608 LEDs High Density Flexible FOB COB 10mm Led Lights RA90 2700K to 6000K Linear Dimmable DC24V](https://www.aliexpress.com/item/1005007162915201.html) - not an affiliate link. I went with 24 V type, I ordered 5 m long strips that I then cut into segments.
4. Cables: I wanted silicone cables so they are easier to bend. I ordered a bunch of these 3-pin ones: [10Pcs JST XH 2s Battery Balancing Charge Plug Silicone Wire JST XH Female Cable 200mm 22AWG for RC Parts](https://www.aliexpress.com/item/1005008182460220.html) - not an affiliate link either. I went with these: 2S 3pin 200mm -10Pcs.
5. I now needed some connectors where the cables will connect to. I ordered a bunch of S3B-XH-A-1 (LF)(SN) connectors from TME.eu: [TME.eu - S3B-XH-A-1 (LF)(SN)JST](https://www.tme.eu/si/en/details/s3b-xh-a-1/raster-signal-connectors-2-50mm/jst/s3b-xh-a-1-lf-sn/).
6. Oh right, I need something to mount LED strips to! Luckily my local hardware store has these 2 m long anodized aluminium profiles that are meant for LED strips, with diffusers. Neat! The thing is, I don't have a link where to buy them or any article numbers. I'll post photos with measurements down below.
7. How will I mount all this? Well the connectors need a PCB, so I made 2 simple designs and had it made by JLCPCB. The PCBs are 1 mm thick but are made from 4 layers. Top and bottom are 10 oz and both inside ones are 5 oz each so I connected both inner layers together. I only needed 3 layers anyway.
8. 3D printed parts hold everything fixed up on the ceiling. I used white PETG, nothing special. I did use up over 1 kg of it thouggh. Some parts were scrap (bad design) but I do want the lights to stay up for a long time :)
9. I also had a big issue of how am I going to align everything up on the ceiling correctly? I had my neighbor CNC cut a 3 mm thick aluminium jig that I used to mark all the holes with. I did need help of my sister for this - thanks sis :)
10. Other material that I used:
- M3x10 mm screws (DIN 912, 3 per cover),
- 2.9X4.5 DIN7981 screws for mounting LED profile to 3D printed base (2 per profile),
- [fischer Metal cavity fixing HM 5 x 37 S B polybag](https://www.fischer-international.com/en/products/cavity-fixings/board-fixing/metal-cavity-fixing-hm/48041-hm-5-x-37-s-b) drywall "anchors" (1 per base),
- 4 mm² wires for long runs and 0,75 mm wires for last 20 cm between distribution boards and long run cables,
- wire ferrules,
- WAGO inline splicing connectors with levers, 221 series (for connecting 4 mm² cables to 0,75 mm² cables - 3 per LED group).
- heatshrink tube (size doesn't really matter, as long as you can fit it over the wires)

## Long story short
After about 5 days worth of walking up and down my ladder, a lot of cutting and stripping wires, even more soldering and eventually figuring out I messed up the lengths again... I somehow made it!

I won't go in too many details why I made some decisions because that would take too long but trust me, be precise when cutting wires and mounting everything. This project is made so (poorly?) that it only has up to 2 mm tolerance on a segment before you're forced to make some wires longer or shorter or it just won't fit.

I decided to make 5 groups of 7 LED strips so the current is evenly distributed. I'm running them all in 2 groups right now, I'm waiting to get An-Penta-Deca delivered, then I'll be splitting them :)

## Important stuff
Here's a list of what measurements are important:
1. LED profiles need to be cut to 665 mm pieces
2. LED strips need to be 616 mm long (cut at cut marks, they are spot-on)
3. You need 2 length of cables: one that has straight wires needs to be XX mm long and the other that has crossed wires needs to be XX mm long.
4. LED profile covers/diffusers need to be 640 mm long
5. When soldering JST connectors to PCB, make sure to cut the legs before soldering so you get as low profile PCB as possible! I tried cutting/grinding them later but that takes waay more time.

## Build process
I hope I can explain in enough detail how to make this :)

### LED profiles
You need to cut the profiles to 665 mm pieces. Why 665? Well I got the profiles in 2 m lengths and it was the least amount of waste doing it this way.

![Measuring and marking cuts](Photos/Project/Measuring_LED_profiles.jpg)

I then went to work with angle grinders. First I cut the profiles then I used the 2nd grinder to round the edges a bit.

![Cutting profiles](Photos/Project/Angle_grinder_party.jpg)

Manual file was used to reach inside parts of profile. I wanted to make all corners smooth, silicone wires are easily damaged!

![Manual filing](Photos/Project/Filing_edges.jpg)

I used a simple 3D printed jig to drill 3 mm holes in correct spot for all the profiles. Just make sure to clear out the debree every so often. I should've made the jig open from the bottom but.. Too late now :)

![Drilling holes](Photos/Project/Drilling_jig.jpg)

I made sure to have all edges nice and clean with no sharp edges.

![Deburringg holes](Photos/Project/Deburring_holes.jpg)

Last step is to mark where the strips need to be placed. Don't hurry or it will bite you later. Ask me how I know. Mark a line 25 mm from edge.

![Mark 25 mm from edge](Photos/Project/Marking_for_strips.jpg)


### PCB soldering

The PCBs are really easy to solder, just keep in mind that you cut the connectors before soldering them!

![Trimming connector leads](Photos/Project/Cutting_PCB_JST_connectors.jpg)

Make sure all the solder joints are as flush as possible, there isn't a lot of free space that we're working with :)

![Flush soldering](Photos/Project/Flush_soldering_job.jpg)

You can use the jig that I also provided.

![PCB soldering jig](Photos/Project/Soldering_jig.jpg)

Power injection "nodes" are a bit of a pain in the butt to make, I admit. Note to self: don't ever order PCBs at 1 AM. Sleep it over and order the next morning. I later replaced the wires with longer (and slightly thicker) ones so I could hide them better.

![Power cables](Photos/Project/Power_injection.jpg)

### LED strips

Cut the strips at cut marks, my strips had them at about 616 mm.

![Strip length](Photos/Project/LED_strip_length.jpg)

Now remove backing foil from the strips and start gluing them to profiles. I found this way to be easier: gluing *then* soldering cables. I'll explain later why. Make sure to be as precise as possible. I know I will sound like a parrot until the end of this guide.

![Place strip at mark](Photos/Project/Yes,_25_mm.jpg)

### Cables

For cutting the cables I found it easiest to just prepare 2 heatshrink tubes that you put over the cables before you cut them. I prepared 1 tube for "shorter" cables (on top of photo) and 1 tube with a notch for the longer cables (bottom 2 cables, one has crossed wires but they are of same length). The short is XX mm long and the long one is XX mm long. For the longer cables, make sure to **shorten the middle wire by about 2 mm!**

![2 cable lengths](Photos/Project/Cable_lengths.jpg)

It helps to move the wires to the side before soldering them. Make sure all the connectors are facing wrong-side-up. I did it this way to avoid shorting pads on PCB with any kind of screw that would be underneath it. This is the reason the PCBs are also "mounted" wrong side up. Well technically they are mounted the right side up but we're looking at them from bottom :P

![Soldering crossed wires](Photos/Project/Soldering_crossed_wires.jpg)

Don't hurry and make sure to check for potential shorts. Luckily I caught this one before I turned everything on. Pro tip: use a multimeter to check for shorts before powering it all on! I know I've stripped the wires too much, I had to move them a bit because I couldn't connect them. Oops :)

![Oopsie](Photos/Project/Short.jpg)

At first it seems like it's taking ages to make it but somehow it was easier the more I made. I didn't even solder all the cables on both ends either, no need to.

![First few segments ready](Photos/Project/This_is_taking_ages.jpg)

#### Grouping

It makes sense to make a plan of how you want to connect the LEDs. I made 5 groups of 7 segments each. This way you can also figure out how many cables you even need to solder and how many V and Y PCBs you need.

![LED groups](Photos/Project/LED_groups.png)

### Mounting

You first need to make some evenly-spaced holes. This was my plan how I wanted it to look like.

![Mounting plan](Photos/Project/Mounting_plan.png)

My neighbor has a laser CNC cutter and made me a jig that helped *immensely* when I was marking holes. I also couldn't do this without my sister. I needed someone to hold it in place while I marked the holes. The first 6 holes were the most critical, if I messed them up, it would skew the whole project. I actually bought a line laser level for this purpose.

![Hole marking jiggy](Photos/Project/Mounting_holes_marking_jig.jpg)

My ceiling is made from drywall so I used the anchors that have normal M5 screws. I didn't dare to go with cheaper ones as that would prevent me from being unable to ever remove or replace anything. Not the cheapest solution, iKnow :/

When mounting the base parts, don't screw them tightly yet, you'll need to turn them to correct orientation first!

![Base part](Photos/Project/Base_part.png)

I don't really have photos of whole mounting process but it's pretty straightforward. Space the profiles evenly, use 2 screws for each profile and that's about it.

After connecting the Y and V PCBs and tucking in the cables, use the covers/diffusers and covers to hide everything.

![Diffusers](Photos/Project/Finishing_touches.jpg)

This is why dimensions matter so much. There are a few mm you can cut from diffusers but if you cut more than 3-4 mm, the gap will show.

![Y board with power](Photos/Project/Y_board_with_power_injection.jpg)

![V board](Photos/Project/V-board.jpg)

I prepared 3 different cover types: for normal 3-way junctions, for 2-way junctions (outside corners) and for junctions with power connections.

![Different covers](Photos/Project/Covers.png)

If you use the correct bit for your drill, you can actually hang it from the ceiling 😂

![Hanging drill](Photos/Project/Use_correct_bit.jpg)

### Connecting to controller

Nothing special, just connect positive wire to positive output and negative CW/WW wires to respective outputs and that's it :)

### YAML file for ESPHome

Included in folder. It's just the example config really, nothing special.

## Random tips and bits and bobs

### Orientation

I oriented all PCB the same way - positive rail on "top". This made it much easier to manipulate. Yes, you can keep tossing and turning them around but it did save me some time in the long run.

I also made sure to have all segments that only had cables run from one side, to not use crossed wires. Try to avoid crossed wires as much as possible, they do show through diffuser. I could probably use hot glue or something to fix them but.. Nah :)

### FLIR images
My thermal camera showed no abnormalities when the strips were running at 100% after a few hours of "testing".

LED controller

![LED controller](Photos/FLIR/LED_controller.jpg)

Power supply after 1 hour

![Power supply](Photos/FLIR/Power_supply_at_full_load_after_1_hour.jpg)

Power cables before/after closing them up

![Power cables](Photos/FLIR/Power_injection_before_closing_covers.jpg)

![Enclosed power cables](Photos/FLIR/Power_injection_cables.jpg)

LED strips

![LED strips 1](Photos/FLIR/Led_strips_1.jpg)
![LED strips 2](Photos/FLIR/Led_strips_2.jpg)
![LED strips 3](Photos/FLIR/Led_strips_3.jpg)
![LED strips 4](Photos/FLIR/Led_strips_4.jpg)
![LED strips 5](Photos/FLIR/Led_strips_5.jpg)

### Measure 3 times, still cut twice

Make sure to not look at things cross-eyed as I apparently have. I triple-checked the length and still managed to cut the strips too short. At least I found out after cutting 6 of them, not *all* of them. Whew!

![Another oopsie](Photos/Project/Measure_twice,_cut_twice.jpg)


## Summary
I totally overengineered this but.. Oh man it looks nice 😅 Not to mention how much it eliminates shadows! Crazy. Would I do it again? Now that it's done, maybe. If you asked me 2 days before coming to this stage: not a chance!

Interesting info: at output of LED controller, I get 24,04 V and at end of strip that is farthest away, my voltemeter read 23,51 V. That is 0,53 V voltage drop and I think that's pretty good. Maybe I did go a bit overboard with using such thick wire for long runs but.. It is what it is. I'm not changing it now.

Anyway, feel free to download the files and make your own hexagon ceiling lights. Let me know if I forgot to add any details or if you have any questions. This is one of the first projects that I started with when moving to a new apartment.

The lights are set up in my "mancave": I call it "Brlog" - that translates to "den" or "lair" 😅

Hope you enjoyed reading this, it sure was an interesting project for me. Not to mention, this was the first time I had custom 4-layer PCBs made for me 😂

## License
This project is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).  
You are free to use and remix it for **non-commercial purposes**, with attribution.  
⚠️ Provided as-is. No liability accepted.
