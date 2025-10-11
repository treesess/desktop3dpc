# desktop3dpc - vCP (vibration concrete printing 振子砼列印)

desktop scale 3d printing concrete/mortar using a vibration unit in the toolhead to make concrete fluid down. 

**check out the latest version of build [here](https://github.com/treesess/desktop3dpc/tree/main/vCP250306)**

251007 update: SSR applied as buffer to isolate the vibration from the toolhead to the printer frame. Metal nozzle adopted. Vibration motors directly hits on metal nozzle. 4 mm nozzle printed cement paste with stable flowrate. 

<img width="543" height="566" alt="image" src="https://github.com/user-attachments/assets/6eedbb54-41da-4814-803d-f8970bee166d" />




--------

![image](https://github.com/user-attachments/assets/7d29cb28-643e-41ec-9e74-a3d78a74e0d9)

1) put a vibration device just above the nozzle. not a stirrer but an actual vibrator. 
2) heat bed on, like fdm

in this way, you can easily print concrete to whatever height you want on a desktop. 

no need of any additions (e.g., PFA, GGBS, silica fume, plasticizer, AC, balabala), just OPC and sand can work this through. 

![image](https://github.com/user-attachments/assets/cc6c881b-42c3-41dc-b51f-30b61f1c5645)

i used modified CR10s as the motion system, changed the toolhead, and printed about 300 mm wall in vase mode with about 20 mm thick of width. 

you may see the flow rate unstable in the picture, that's because i just came up with the vibrator idea last night and was controlling the flow manually. surely will do a better control of flow rate. 


-----

the advantage is clear: 

1) no need of pump, which is a must in industrial printers.
2) no need of additions, which make it pretty easy for raw material prep.
3) water cement ratio can be serious low. 
4) Klipper firmware and fdm slicer can do most of the gcodes, easy for turn digital obj into print file.
5) simple toolhead, basically every fdm machine can be modified into a concrete printer with a slight change of toolhead.

----

note: 

1) for sand, you better seive it into 0.3 to 0.6 mm size. of course if you use a larger nozzle, you can even do coarse aggregate.
2) heatbed greatly reduces the first setting time of concrete. but it might affect the strength of concrete. however, it's desktop, you want the shape but not the strength, don't you?

