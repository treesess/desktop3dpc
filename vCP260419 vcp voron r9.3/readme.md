r9.3 is a version you can build and do stable prints. 

documentation for details coming soon. 

if anything doesn't seem right, my apologies. please let me know. Thanks!

---------------------

## toolhead intro

i hope this intro can show you how this toolhead works clearly. parts were put into folders. 

### 1 x carriage

<img width="698" height="387" alt="image" src="https://github.com/user-attachments/assets/46908c60-bb9a-4452-bd92-f940aacb6983" />

based on the x extrusion of VORON2.4r2. 

### 2 positioner

<img width="681" height="393" alt="image" src="https://github.com/user-attachments/assets/d4a2ee59-52a9-4b8f-b4ee-24d0978f7faf" />

to make the major functional part in position, as well as connect to PG13.5 umbilical cable mount. a thick TPU ring is between the major part and the positioner as a buffer. 

### 3 feed screw and barrel

<img width="674" height="395" alt="image" src="https://github.com/user-attachments/assets/86de3674-f11b-4695-a251-2b9a0b5de019" />

paste put in here. this group includes the feed screw, screw barrel, stepper, Orbiter planetary gearbox, stirrer, etc. the feed screw provides better extrusion accuracy. the stirrer avoids material buildup inside the hopper. the stepper and the gearbox drive them. 

### 4 hypocenter

<img width="690" height="381" alt="image" src="https://github.com/user-attachments/assets/43599fac-f8a8-4489-a651-b2f64e43480d" />

this group generates pulse vibration by forcing step loss of the stepper. no worry about the counter-EMF (counter-electromotive force), the 608 bearing limits it and i tested it. 

### 4.1 stepper with hitter 

<img width="693" height="419" alt="image" src="https://github.com/user-attachments/assets/496e347e-b08c-4cff-9863-8cd8181bda6f" />

sorry i don't know how to name it. this group inside the hypocenter has been working very stably through many versions in the prototyping. the hitter is a M3 screw with many shims to thicken it (try any other metal way to make it as you want). 

### 4.2 608 clamp and hotend

<img width="800" height="426" alt="image" src="https://github.com/user-attachments/assets/7debac9b-fd87-4948-b6a5-81f28be089c8" />

the hitter driven by the stepper hits the 608 bearing, where the heat block is locked tightly by 3x M3 screws so that the vibration can be passed to the nozzle in a rigid structure. the heat block is the CR10 one. the nozzle is SUS304 tube been cut and tapped with M6 threads. 

-------

## make of toolhead parts

### 1 FDM printed parts

- since almost all parts are under cyclic load, ASA is recommended for the printing of vcp voron toolhead with 0.3 mm layer height. 
- for the barrel/hopper one, 0.1 mm layer height is recommended to make a smooth inner surface of the barrel as possible.
- for the feed screw, 0.1 mm layer height is recommended. better sand it smoother. 
- get some more perimeters and higher infill percentage as possible. sorry i don't have tests to tell how strong they need to be. 
- there is only one TPU part. you need to cut it vertically after print. if you don't want TPU, you can just use some tapes (PTFE Tape i recommend).

### 2 metal parts

- the M3x100 SHCS needs to be straight.
- the M3x100 SHCS needs to be straight. 
- the M3x100 SHCS needs to be straight. 

this M3x100 is to strengthen the feed screw. i may try metal print of the feed screw later. 

### 3 heat set inserts

only the "standard VORON heat set inserts" M3x5x4 mm is used. 

- 4.6 mm holes are for heat inserts
- 5.7 mm holes are for SHCS caps


*to be con't*


-------

## toolhead assembly

there is no screw must be fastened very tight to make it work. overtighten might cause plastic failure or fail of assembly (i've been there). 


### 1 x carr 

<img width="504" height="377" alt="image" src="https://github.com/user-attachments/assets/ceb9e724-4c0f-49a0-aa12-b0e29d433536" />

- 2x M3x40 SHCS to assemble the left and right parts.
- 4x M3x8 SHCS to fix the x carr parts to MGN12H slide block with belts through. similar to the original x carr. 

btw i kept the 32.5 mm horizontal distance of screw distance for the x carr but the failed to follow the vertical distances. 

if you need to change the x carr frequently, i would recommend marking the belt as in the photo. 


### 2 hypocenter stepper w hitter

<img width="492" height="367" alt="image" src="https://github.com/user-attachments/assets/ee02bc3c-0886-4d86-8ff6-308795f53d7e" />


### 3 pancake NEMA 17 w Orbiter planetary gearbox (8 mm shaft)

<img width="508" height="370" alt="image" src="https://github.com/user-attachments/assets/17f035b0-48fb-4daa-879f-d0f151d25a32" />

### 4 hotend (2x CR10 heat blocks)

<img width="273" height="278" alt="image" src="https://github.com/user-attachments/assets/1d791858-5b82-4819-b14b-eeb64b58c1a0" />

drill out the M6 threads of the upper one or not seems does not matter. 

### 5 feed screw w stirrer

<img width="511" height="323" alt="image" src="https://github.com/user-attachments/assets/0d461b6c-5a82-41a2-87dd-4f857da38c79" />

get a 0.5 mm M3 shim in between the feed screw and stirrer is recommended. 

### 6 coupler

<img width="281" height="357" alt="image" src="https://github.com/user-attachments/assets/8479c451-fcc8-4ee6-8fca-cece5f888102" />

screw the M3x100 tight now. but not too tight to break the plastic...

### 7 to the pancake

<img width="506" height="275" alt="image" src="https://github.com/user-attachments/assets/7f88816e-298e-46fe-9238-fa068876e36a" />

### 8 into the screw barrel

<img width="283" height="378" alt="image" src="https://github.com/user-attachments/assets/3ef9b423-6263-437c-a2e3-2785b16efa79" />

### 9 tight up pancake mount

<img width="281" height="374" alt="image" src="https://github.com/user-attachments/assets/fa596168-43dc-4822-8c53-6328a146317a" />

check if you can rotate the feed screw and stirrer manually. if you can't, try loose the four mount screws a bit. 

the feed screw should not have relative rotation to the stirrer. or you need to check step 7. 

### 10 hypocenter motor

<img width="504" height="372" alt="image" src="https://github.com/user-attachments/assets/59a8ad58-fa5e-468a-8b45-a3854941bdd5" />

watch out the cable exit and hitter direction. 

if you feel it time consuming to screw in these two M3, just drill the motor mount with a 3 mm drill bit. 

don't overtighten these two M3. 



### 11 checkpoint

<img width="508" height="379" alt="image" src="https://github.com/user-attachments/assets/91ee4fbd-28de-44d2-b678-2b2791b987b7" />

### 12 nozzle

<img width="505" height="370" alt="image" src="https://github.com/user-attachments/assets/0c6a71d9-64a3-41a9-8a0e-bbacca99073d" />

it is SUS304 tube, OD 6 mm ID 3 mm. thread the tube with M6 so that you can get it into the CR10 heat blocks. the total length doesn't have to be accurate. not even the length of threads. just about 40 mm long is fine. you will find out why when you finish the assembly and G28 z. 


### 13 nozzle assembly

<img width="507" height="380" alt="image" src="https://github.com/user-attachments/assets/39fb997a-c032-4f2e-9ab1-8cd89a3b7d4d" />

screw the nozzle into the CR10 heat blocks and push it into the lower end of barrel. there should be a small gap as shown in the photo. don't really matter how large the gap is. or you can use a feeler gauge to be certain. just define the gap by yourself. sorry i m lazy to do that. 

### 14 secure the nozzle

<img width="506" height="377" alt="image" src="https://github.com/user-attachments/assets/b57f00b0-0a0b-47b9-a63f-0bbad493fccc" />

- two M3 screws first
- M6 nut later

### 15 608 clamp

<img width="501" height="376" alt="image" src="https://github.com/user-attachments/assets/5640f28b-eff9-41df-a47e-2295a40376eb" />

<img width="504" height="376" alt="image" src="https://github.com/user-attachments/assets/9df489be-61bf-4d31-a695-23d1fbeb823d" />

<img width="508" height="379" alt="image" src="https://github.com/user-attachments/assets/e142a1e0-c86b-4afe-be68-e4d1a69e444b" />

set steppers off, and move the hitter manually. it should be free to move several millimeters with the limit of 608 bearing. if it's too tight to move it. try loose the two motor screws a bit or the clamps and twist it a little. 


### 16 TPU buffer

<img width="510" height="380" alt="image" src="https://github.com/user-attachments/assets/e444d384-7d83-4bfb-b67d-f638d3d14417" />

### 17 fake position

<img width="512" height="377" alt="image" src="https://github.com/user-attachments/assets/2f1879dc-ff6d-44c1-ab81-4878d13c5a61" />

since i don't have xyz endstops for now. i fake the position at 150 0 0 and manually set z offset. there is no QGL so far. sorry. 

### 18 tighten up the positioner parts

<img width="503" height="378" alt="image" src="https://github.com/user-attachments/assets/392a266a-6f54-49ec-b8c2-0f938b0949c2" />

and the PG13.5 umbilical cable mount. 

the optional COB LED light bar is also included in the cad file .f3d. just hook it up if you make it too. 

