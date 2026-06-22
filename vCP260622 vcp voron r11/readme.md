r11 is a plastic nozzle version without hotend to heat up the nozzle but very friendly for starter to build. low cost and easy manufacture/assembly.

documentation in coming!

if anything doesn't seem right, my apologies. please let me know. Thanks!



-----------------------------------------

# 1 toolhead, vcp voron, r11

just a second for the naming of vcp voron: vcp is short for vibration cementitious print, vcp voron is like E3D Revo Voron, means vcp *for* VORON since it's based on VORON2.4 motion system. previously there were vcp on a CR10 but that's not reliable since the bed of i3 motion system is not good for the fresh slurry print to keep its shape. so basically vcp is just for VORON (or delta, but still DORON Velta would be nice). 

## 1.1 toolhead intro

i hope this intro shows you how this toolhead works. parts were put into folders.

### 1.1.1 x carriage

based on the x extrusion and MGN12 linear rail of VORON2.4r2.

<img width="702" height="413" alt="image" src="https://github.com/user-attachments/assets/adbaefc0-a400-445d-b39e-a6edb0ade6e5" />

### 1.1.2 positioner

to make the major functional part in position, as well as connect to PG13.5 umbilical cable mount. 

<img width="650" height="421" alt="image" src="https://github.com/user-attachments/assets/d9629da9-85c2-40a5-a7b2-7f225727b061" />

### 1.1.3 integrated hopper-nozzle

cementitious slurry goes in from the top and comes out from the bottom. 

<img width="687" height="419" alt="image" src="https://github.com/user-attachments/assets/8535bc72-6fc8-41e7-8e8b-8556f33aa9ba" />

### 1.1.4 hypocenter

this group generates pulse vibration by forcing step loss of the stepper. no worry about the counter-EMF (counter-electromotive force), the 608 bearing limits it and i tested it.

<img width="670" height="417" alt="image" src="https://github.com/user-attachments/assets/4f3eb2af-9e1d-49e4-9fd2-d82422cb5160" />

the hypocenter has been working very stably through many versions in the prototyping. the hitter is an M3x50 screw with many shims to thicken it a bit.


### 1.1.5 (optional) upper drive

actually became optional. the major function of this part is to keep stirring the slurry so that it won't settle in the flow path. you can do the stir-up manually without this part. 

<img width="670" height="424" alt="image" src="https://github.com/user-attachments/assets/3f2a2ae1-4033-484f-999d-6360ec2d398c" />

for nozzle diameter smaller than 1.5 mm, it's NOT recommended to install this part (and yes stir up the slurry manually would be an better option, i will explain why later (maybe...)).


### 1.1.6 (optional) LED light bar

have a better view. 

<img width="661" height="419" alt="image" src="https://github.com/user-attachments/assets/4ad3329b-1d8c-4293-b19b-7e5553b17ea9" />

### 1.1.7 (optional) resin coating jig stand

if you want to finish up the surface with epoxy resin, you may use this jig. 

<img width="538" height="421" alt="image" src="https://github.com/user-attachments/assets/d0d56922-f193-492b-b5d5-7defcf7436e8" />






# 2 hopper-nozzle body

slurry feed hopper with integrated nozzle printed in one part, brings you a continuous and seamless flow path with smoothness. 

### 2.1 FDM print of hopper-nozzle body

recommend ASA or at least ABS print of the **hopper-nozzle body** because cementitious material is alkaline (pH 12-13 for fresh slurry) therefore PETG or PLA won't survive too long. 

0.2 mm layer height is good. recommend 0.5 mm line width for both inner and outer walls with 7 walls at least, because it's gonna stand against frequent impact pulse vibration during the print. 

after print out, directly screw in one M3x20 SHCS (socket head cap screw) near the nozzle as a reinforcing bar, like this: 

<img width="861" height="665" alt="image" src="https://github.com/user-attachments/assets/a7f412ee-58ab-4460-a526-2e19bfa389b0" />

(do not over-fasten this screw, it's plastic anyway. over-fastening may cause interlayer cracks in the print part)


### 2.2 (IMPORTANT) internal flow path finishing procedure

the flow path needs to be smoothed by drill bits, 60° chamfer drill bit, files. the roughness of the flow path will cause flow rate inconsistency and/or material buildup and/or clog. 

tools need: 

<img width="482" height="391" alt="image" src="https://github.com/user-attachments/assets/fce4d54e-5537-40fe-86bb-bf3717304581" />

- hand-held electric drill (better have 2 sets)
- 20.5 mm 60° 3-flute chamfer drill bit  (*filleted, extended*) - M3 or M4 tapping tools are needed to extend the length of this bit (see photos below)
- (optional) 20.5 mm drill bit
- hex shank screwdriver bit extension
- hex shank socket wrench 
- round file
- nozzle-diametered drill bit (e.g., 1.0 mm drill bit if you want 1.0 mm nozzle diameter)
- (optional) carbide rotary file (pointer)
- 4-flute taper reamer with hex shank socket (*tip sharpened*)

(optional but highly recommended) you may use an angle grinder and sandpaper to do a fillet on the sharp edge of the 60° chamfer bit. this can give you a smooth transition of flow path. 

<img width="753" height="356" alt="image" src="https://github.com/user-attachments/assets/dbed72d0-d138-4bc8-9aee-1795ef8fbeb1" />



a light torch is recommended if you wanna have a look of the flow path:

<img width="500" height="332" alt="image" src="https://github.com/user-attachments/assets/e9aefa16-4c5f-4b99-817b-f7068c79d74e" />








#### 2.2.1 section one - barrel

you can consider using a 20.5 mm diameter drill bit, but personally i only use the 20.5 mm 60° chamfer drill bit. 

(optional) 20.5 mm drill bit: 

<img width="445" height="330" alt="image" src="https://github.com/user-attachments/assets/dff6ab27-a53f-4df2-a4c0-1199592933ac" />

(must) 20.5 mm 60° chamfer drill bit:

<img width="558" height="190" alt="image" src="https://github.com/user-attachments/assets/847ad1e0-d7c0-4e3f-bb68-5914801ba83f" />

i recommend doing this section dry.

if you ever have the other way to drill it down to the throat of the flow path, you don't need to do the extension of the 60° chemfer bit. if not, my plan is tapping the hold of chamfer bit and use an M3 or M4 SHCS and hex shank extension to reach the throat. 

hold the print part and drill in the chamfer **slowly**. 

**PLEASE BE SLOW**. or you may hurt yourself or waste the print part.  

<img width="539" height="373" alt="image" src="https://github.com/user-attachments/assets/e38aa2e9-58f9-443e-8836-6253393c9730" />

don't do it to the throat in one go. drill in 10 or 20 mm and retreat once. repeat  till you see something like below, you've reached the throat: 

<img width="496" height="361" alt="image" src="https://github.com/user-attachments/assets/b429947e-c39c-45ed-9868-da57f64f295a" />



#### 2.2.2 section two - throat

these three are for the throat:

- 4-flute taper reamer
- round file
- (optional) carbide rotary file

<img width="711" height="462" alt="image" src="https://github.com/user-attachments/assets/c5b8f9da-854e-4391-a3ce-97a253cc85af" />

if you have the carbide rotary file, you may not need to sharpen the tip of taper reamer like i did. if you don't have the rotary file, you may need to shape the blades on the tip of the reamer. 

let me know if you have better tools for this job! 

for this part, sorry that there is no good photo to take since it's deep inside. 

for me, i use the round file as a probe to grope 

<img width="491" height="340" alt="image" src="https://github.com/user-attachments/assets/b09c208f-75b4-4f95-baa2-0daa830f75ab" />

there should be NO STAIR(S) on any transitional part of the flow path. any stairs are meant to make some material buildup during slurry printing. 


#### 2.2.3 section three - nozzle

slowly, drill in your preferred diameter drill bit from the other end like this: 

<img width="497" height="346" alt="image" src="https://github.com/user-attachments/assets/34ef66d2-7e41-4a22-847b-cf3361107368" />

again, it's better to advance 2 mm and retreat once. repeat till you get it through (to the throat). 




#### 2.2.4 repeat section two and section three multiple times

please repeat section two and section three multiple times and end it up with section two as a finishup. i don't know how to explain this. hope i m scientific enough. 

test it with water. water goes in from the hopper end should be able to come out from the nozzle by gravity:

<img width="483" height="290" alt="image" src="https://github.com/user-attachments/assets/98ef1d32-0747-466f-9266-141b8b373ee8" />








### 2.3 outer perimeter of nozzle

this is how it looks like when finished with the above steps:

<img width="716" height="410" alt="image" src="https://github.com/user-attachments/assets/ba2d8fba-8120-4315-a44b-d8a2dafce95c" />

we need to cut it sharper. theoretically, anything sharp enough can do this. you can even use a soldering tip to do this (but i don't recommend that). 

my choice is ultrasonic cutter (e.g., Magicutter): 

<img width="616" height="423" alt="image" src="https://github.com/user-attachments/assets/4aa30571-5a9e-4599-9b41-bc5f4e2a9faf" />

the ultrasonic cutter is easy to use and can slightly melt the ASA print making it smoother. 

make the nozzle perimeter as thin as possible (the thinner the better print quality but harder to make): 

<img width="571" height="473" alt="image" src="https://github.com/user-attachments/assets/8beb7895-3bf3-4dac-b844-50e69653c067" />

(optional) you may file the perimeter a bit if you like: 

<img width="372" height="274" alt="image" src="https://github.com/user-attachments/assets/421204f3-76b8-408e-9664-b4c3cf9bb67b" />

then sanding it with at least 2500 grit sandpaper **with water**: 

<img width="722" height="501" alt="image" src="https://github.com/user-attachments/assets/1fc0112a-3452-422b-ad5e-9353ff32d32b" />

this would be okay (the perimeter should look polished): 

<img width="734" height="473" alt="image" src="https://github.com/user-attachments/assets/b816262e-8b99-45f3-be6f-5045d1d8ce53" />




### 2.4 buffer for positioner

i use PTFE tape as buffer. you can also print a TPU one (like the one in r9.3).

<img width="474" height="355" alt="image" src="https://github.com/user-attachments/assets/e3842cda-5e40-42d2-87fe-93ae03621413" />

(optional) and wrapped up by some kind of tape that water cannot wash away: 

<img width="487" height="362" alt="image" src="https://github.com/user-attachments/assets/f35ffd53-a35b-4376-8347-4808616be34a" />

(optional) better write down the nozzle diameter on the body:

<img width="487" height="370" alt="image" src="https://github.com/user-attachments/assets/089792c8-e752-4b6a-8dc3-ae1269eb70ea" />






### 2.5 bearing retainer

M3x4x5 VORON standard heat inserts set in the FDM printed bearing retainer part. also here are one 608 bearing and two M3x40 SHCS.

<img width="495" height="254" alt="image" src="https://github.com/user-attachments/assets/6e22bb77-c8c0-45cc-ae50-71a64692a528" />

preload the 608 bearing into the retainer: 

<img width="480" height="316" alt="image" src="https://github.com/user-attachments/assets/e03bd903-bb9f-48df-b581-169e039e1c58" />

screw up the two of M3x40 SHCS: 

<img width="504" height="368" alt="image" src="https://github.com/user-attachments/assets/7f5f4802-2dbb-4b12-a415-2861282a6efb" />


### hypocenter

*to be continued*

*to be continued*

*to be continued*

now it's ready to be installed on vcp voron toolhead. 
