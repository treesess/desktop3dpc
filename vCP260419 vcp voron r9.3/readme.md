r9.3 is a version you can build and do stable prints. 

documentation for details coming soon. 

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

