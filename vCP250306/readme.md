this is the first design of vCP. based on the motion system of CR10s, changed the x carriage and toolhead and succeeded in stable flow rate mortar printing. 

**all CAD STL are open-sourced (GPL-3.0 license) for download. Welcome to build yours and let me know!**

All plastic parts were designed for easy and strong FDM printing without adding additional support. Let me know if you have doubts about which direction to put on heatbed. 

![image](https://github.com/user-attachments/assets/bacb2a73-b690-4403-90f2-e00ddbaf349d)


![image](https://github.com/user-attachments/assets/acc7785e-c92e-4a1d-9e78-e0b117987513)

on its second print, using already hardened mixture after 2 hours of mixing, it still printed rather consistent lines nicely. 

![image](https://github.com/user-attachments/assets/2f7e98dd-9f64-4296-891a-0baf6e4d6d26)

note that this was 10 mm nozzle printing 7 mm layer height, which isn't recommended since layer height too large makes very weak interlayer cohersions. 

-----------

here goes a brief intro of how this toolhead works: 

![image](https://github.com/user-attachments/assets/1666dccf-596d-4490-8672-8fd00c69a5da)

inserted into the bowl is this torsional shaking bit along main shaft. it has some blades, and keep around 5 mm distance to the bowl wall so that the vibrated concrete could be pushed into the "tunnels" to have a more consistent flow rate (at least this is how i think it works, tbh i m not 100% sure if the explanation is correct, but the printing results were seriously good)

![image](https://github.com/user-attachments/assets/15ffcc85-d303-4e74-99e6-3c39a1c3f425)

The main shaft is a 8 mm diameter rod with M5 nut grooves on both ends. it is constrained by two 608zz bearings from horizontal movement, but free to have torsional movement and vertical movement. 

Then the upper is the vibration motor unit clampe to the main shaft by two M3 SHCS. 

At last the top, there is an F625z bearing and M5 nut holding the main shaft which serves as the "hanger" and adjustment of the vertical positioning of main shaft so as the vibration unit inserted into the concrete bowl. 

The vibration motor is driven by DC power and the voltage can be adjusted by a DCDC module. The voltage controls the rpm/frequency of the vibration unit. 


so far these are my thoughts and put into practice. i m sure there are many to be optimized. and i actually don't know exactly how it works. i can't explain to you why the horizontal vibration of motor can be turned into the torsional one in the vibration unit but this is what happened when i observed in [here](https://github.com/treesess/STEAMRELAY/tree/main/showcase/250119%20mod%20of%20drill%20for%20concrete%20vibration%20in%20plastic%20mold). Maybe it's some kind of crank. idk. please teach me if you have a clue, big thanks! 

