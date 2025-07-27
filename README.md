# HexaLED
Hexagon ceiling lights

## Summary
I saw many of these "hexagon LED" ceiling lights but none that would fit my needs:
- 24 V
- dimmable warm white / cold white
- low profile
- able to be controlled locally via Home Assistant
- freely extendable / modular

## How it started / bill of materials
1. Controller: I first wanted to build a multi-channel N-FET driver board that would be able to control 10 output channels (for 5 CW/WW strips). Then I found out about these fancy thingies: [QuinLED An-Penta-Deca](https://quinled.info/quinled-an-penta-deca/) and [QuinLED An-Penta-Plus](https://quinled.info/quinled-an-penta-plus/). Well the first step was easy: add to cart 😂
2. LED strips: I decided on these: [AliExpress - FCOB CCT LED Light Strip 608 LEDs High Density Flexible FOB COB 10mm Led Lights RA90 2700K to 6000K Linear Dimmable DC24V](https://www.aliexpress.com/item/1005007162915201.html) - not an affiliate link. I went with 24 V type, I ordered 5 m long strips that I then cut into segments.
3. Cables: I wanted silicone cables so they are easier to bend. I ordered a bunch of these 3-pin ones: [10Pcs JST XH 2s Battery Balancing Charge Plug Silicone Wire JST XH Female Cable 200mm 22AWG for RC Parts](https://www.aliexpress.com/item/1005008182460220.html) - not an affiliate link either. I went with these: 2S 3pin 200mm -10Pcs.
4. I now needed some connectors where the cables will connect to. I ordered a bunch of S3B-XH-A-1 (LF)(SN) connectors from TME.eu: [TME.eu - S3B-XH-A-1 (LF)(SN)JST](https://www.tme.eu/si/en/details/s3b-xh-a-1/raster-signal-connectors-2-50mm/jst/s3b-xh-a-1-lf-sn/).
5. Oh right, I need something to mount LED strips to! Luckily my local hardware store has these 2 m long anodized aluminium profiles that are meant for LED strips, with diffusers. Neat! The thing is, I don't have a link where to buy them or any article numbers. I'll post photos with measurements down below.
6. How will I mount all this? Well the connectors need a PCB, so I made 2 simple designs and had it made by JLCPCB. The PCBs are 1 mm thick but are made from 4 layers. Top and bottom are 10 oz and both inside ones are 5 oz each so I connected both inner layers together. I only needed 3 layers anyway.
7. 3D printed parts hold everything fixed up on the ceiling. I used white PETG, nothing special.
8. I also had a big issue of how am I going to align everything up on the ceiling correctly? I had my neighbor CNC cut a 3 mm thick aluminium jig that I used to mark all the holes with. I did need help of my sister for this - thanks sis :)
9. Other material that I used: M3x10 mm screws 

## Then it began
After about 5 days worth of walking up and down my ladder, a lot of cutting and stripping wires, even more soldering and eventually figuring out I messed up the lengths again... I somehow made it!
I won't go in too many details why I made some decisions because that would take too long but trust me, be precise when cutting wires and mounting everything. This project is made so (poorly?) that it only has up to 2 mm tolerance on a segment before you're forced to make some wires longer or shorter or it just won't fit.

## Measurements
Here's a list of what measurements are important:
1. LED profiles need to be cut to 665 mm pieces
2. LED strips need to be 616 mm long (cut at cut marks, they are spot-on)
3. you need 2 length of cables: one that has straight wires needs to be XX mm long and the other that has crossed wires needs to be XX mm long.
4. LED profile cover/diffuser needs to be 640 mm long




## License
This project is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).  
You are free to use and remix it for **non-commercial purposes**, with attribution.  
⚠️ Provided as-is. No liability accepted.
