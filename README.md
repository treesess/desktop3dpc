# desktop3dpc - vCP (vibration cementitious printing)

desktop scale 3d printing of cement-based/non-Newtonian materials (e.g., cement paste, mortar, concrete) using a vibration unit in the toolhead to make the fluid down from the nozzle. 

**check out the latest version of build [here](https://github.com/treesess/desktop3dpc/tree/main/vCP260102)**


-------
260208 update: in case you are interested in how it looks after curing, the photos fyi. 

<img width="691" height="662" alt="image" src="https://github.com/user-attachments/assets/725fa3eb-35c0-4228-ab6f-539d8bb7e512" />

<img width="712" height="672" alt="image" src="https://github.com/user-attachments/assets/15b5ab05-1a9f-4051-b883-1305dc8fbf35" />


also the non-vase mode (normal slicing, not using spiral/vase mode) print has been tried. several times: 

<img width="777" height="663" alt="image" src="https://github.com/user-attachments/assets/621af857-90ee-4456-b50a-3ec8a540a15e" />

hey, it's a VORON cube i believe, i know it's not cool enough... could you pls just give me some credits for trying the predicted disaster XD. 

yes, the flowrate wasn't good, due to, umm, some print parts cracked not long after the start of printing. 

also of also, the MCU error (actually tmc2209 drive error) has been fixed by updating the toolhead - sorry that version is not milestone enough so i may upload an even newer version after finishing the design and test. 

i think i also need to explain why there was stepper drive error. it's some kinda "reverse electromotive force", caused by the obvious - we force the stepper to lose steps all the way, so when the rotor kept bouncing backwards again the drive, thus the "reverse electromotive force". sorry that i can only explain this in a level of "making sense" because i m not a specialist on motors... 

-------
260108 update: though the MCU (skr pico) reported error from time to time (possibly due to the intentional step loss of motor), a neat enough one has been printed: 

<img width="365" height="377" alt="image" src="https://github.com/user-attachments/assets/784c701c-9509-4f92-b6b9-77299dd2b2ac" />

above is the latest print. 

------

251007 update: shore 10 solid silicon rubber (SSR) applied as a buffer to isolate the vibration from the toolhead to the printer frame. Metal nozzle adopted. Vibration motors directly hits on metal nozzle. 4 mm nozzle printed cement paste with a stable flowrate. 

<img width="543" height="566" alt="image" src="https://github.com/user-attachments/assets/6eedbb54-41da-4814-803d-f8970bee166d" />

(this was printed by a subversion toolhead, which was not uploaded, but don't worry the current version is much better.)


--------

below is my first print:

![image](https://github.com/user-attachments/assets/7d29cb28-643e-41ec-9e74-a3d78a74e0d9)

1) put a vibration device just above the nozzle. not a stirrer but an actual vibrator. 
2) heat bed on, like fdm

in this way, you can easily print cement-based stuff to whatever height you want on a desktop. 

no need of any additions (e.g., PFA, GGBS, silica fume, plasticizer, AC, balabala), just OPC and sand can work this through. 

![image](https://github.com/user-attachments/assets/cc6c881b-42c3-41dc-b51f-30b61f1c5645)

i used modified CR10s as the motion system, changed the toolhead, and printed about 300 mm wall in vase mode with about 20 mm thick of width. 

you may see the flow rate unstable in the picture, that's because i just came up with the vibrator idea last night and was controlling the flow manually. surely will do a better control of flowrate. 


-----

the advantage is clear: 

1) no need of pump, which is a must in industrial printers.
2) no need of additions, which make it pretty easy for raw material prep.
3) water/cement ratio can be seriously low. 
4) Klipper firmware and fdm slicer can do most of the gcodes, easy for turn a digital obj into print file.
5) simple toolhead, basically every fdm machine can be modified into a cementitious material printer with a slight change of toolhead.

----

note: 

1) for sand, you better sieve it into 0.3 to 0.6 mm size. of course, if you use a larger nozzle, you can even do coarse aggregate (5 mm or above).
2) heatbed greatly reduces the first setting time of the fresh mix. but it might affect the final strength of the print. however, it's desktop, you want the shape but not the strength, don't you?

