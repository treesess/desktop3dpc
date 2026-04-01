finally i've got a stable version of toolhead. still, too many to improve, trying very hard every day. 

pls see the f3d CAD file for details. 

if you wanna build one, please let me know and i will sort things up and upload them for you. 

<img width="443" height="601" alt="image" src="https://github.com/user-attachments/assets/c98bf18c-269e-4254-a277-c04955016414" />


The motion system is VORON2.4. X carriage is in the f3d as well. For the modification of bed into a seperate/independent one (to isolate vibration from the frame to the bed), i used a piece of concrete and 4 rubber footpads, not a neat design, may upload later. 





## 1 Explanation of how this toolhead works

1) generation of pulse vibration

Using an M3 bolt as the oscillating impactor, repeatedly tapping the inner race of a 608ZZ bearing to induce periodic (pulsed) vibrations. This M3 impactor was driven by the 42 stepper. The 42 stepper simply executed the gcode of normal E instructions but lost most of the steps due to the constraint of 608 bearing. 

the 608 bearing was tightly constrained with the heat block. the SUS304 tube was tapped and screwed through the heat block. in this way the pulse vibration was passed to the tube. 

2) flow path

the mixture was added into the hopper. since the vibration of the toolhead, the mixture went down by gravity then entered the SUS304 tube. the lower end the the tube was the actual nozzle as the exit of mixture flowing on to the print layer. 

3) why vibration works

cementitious materials are thixotropic, simply speaking they stay sold when static, but become fluid under vibration. we control the vibration of this toolhead, when the toolhead moves to the position to extrude, vibration starts so the mixture become fluid therefore goes down under the gravity. after the extrusion, the mixture stays on a static bed, therefore becomes quite solidified to support other layers. we can do travel without extrusion with the same logic. as long as we don't vibrate, there is no extrusion. 

4) heatbed and hotend

heatbed with 50 to 70 ℃ can accelerate the hydration of cementitious materials. hydration is the chemical reaction that makes the cement-based mix sold permenantly. but temperature too high may cause shrinkage of the print. in real case this doesn't hurt too much because the new layers bring water to the previous layer, to keep it wet. however, overall speaking the chemical reaction needs water to go on, therefore at some point we add water to the print to keep it wet. this is subtle, can only spray a bit because too much water will destroy the print since it needs hours to complete initial setting. the print is vulnerable before that. that's why we need a separate/independent bed for it. 

hotend is experimental. as we heat up the mixture in the toolhead, it increases the workability of mixture and makes it easier to extrude. higher temperature also makes the extruded part cure faster. but there are problems with this doing. if the mixture has been staying in your hopper for too long (1 or 2 hours), it's partially cured, higher temperature make this quicker. the worst case is, when you pause the print, the mixture near the nozzle may complete the initial setting and block your nozzle. 

both heatbed and hotend have another problem, that, higher temperature dry up the mixture and print fast. we really want to keep the water in our mixture because that makes the viscosity stable thus stable flowrate. but heat evaporates the water so this is a subtle balance game. 


5) printing

it is very similar to FDM printing. but much slower. 10 mm/s speed is considered high to me. if one layer has its layer time under 1 minute, it's very likely the next layer will drag it forth and back. so i recommend making a PAUSE to these fast layers. i don't recommend you to slow down these layers since you will need to tune the flowrate for different speed. 

large overhang and medium bridge are all possible. because the mixture is sticky. you may easily print a large overhang successfully, but please wait some time before printing the next layer because it needs more time to set. if you don't wait, the next layer might crush your beautiful overhang. same thing to bridging. 

for large area of bridging (such as the ceiling of 3dbenchy, 250% size), it's totally possible, but, you need to PAUSE every 2 to 3 lines. or the next line may drag the previous line down. 


(to be continued)





## 2 cement paste mix design

i used a simple mix for multiple print tests so far. 

| item    | gram | descriptions |
| -------- | ------- |  ------- |
|OPC (Ordinary Portland Cement)|100|major blinder|
|PFA (fly ash)|40|secondary blinder|
|water|50| may add more if your mix is too viscous|

adding river sand (fine aggregate) can improve print quality greatly sometimes, but make sure your sand particles are much smaller than your nozzle diameter (at least 1/2 or 1/3). reduce your water/cement ratio to avoid bleeding and segregation. 

(bleeding means water comes up when vibrating, segregation means aggregates sink down when vibrating.)


(to be continued)


------------------

**important note: everything is still experimental, though this version is basically stable but still need long term tests to prove the robustness which in still ongoing**

## 3 BOM

| item    | qty. | descriptions |
| -------- | ------- |  ------- |
| 608zz bearing  | 1    |as the constraint of M3 impactor   |
| SHCS M3x100 |   2   |    fastening the heat block to the hopper     |
| SHCS M3x70    |   1  |    ditto     |
|SHCS M3x35 |4 |fastening the front and the toolhead to x carriage |
|ASA or ABS filament | - | for printing toolhead components, PETG is not okay with highly alkaline cementitious mixture|
|TPU filament |-| for printing the buffer cylinder which holds the major part|
|SUS304 tube od6 in3, 112 mm long|1| lower end as the nozzle, upper end connects to hopper, you may need longer or shorter depending on bed setting|
|42 stepper |1 | to drive the impactor (hitter in CAD) |
|...|...|...|

(to be continued)

## 4 tools
| item    | qty. | descriptions |
| -------- | ------- |  ------- |
|angle grinder|1|you may need to cut or grind the hardware|
|taper reamer bit|1|for chamfering the hopper to make it smooth|
|chamfering bit 60 degree |1| for chamfering the SUS304 tube |
|round file 600 grit|1| to make the tube smoother even|
|1000 to 5000 grit sand paper|1|to make the tube extra smooth|
|angle grinder|1|you may need to cut or grind the hardware|
|allen key|1 set| for the M3 bolts|
|hex bit and screw driver|1| some M3 bolts are too long to be driven by hand|
|containers and mixing knife|3|for mixing cementitious materials, get some spares|
|digital balance, 0.1 g resolution|1-2|for weighing up raw materials for mixture|
|bucket with water|1|for cleaning. when a container or tool with mixture is done, put it in water, this makes it easy to clean later|
|tapping tool M6|1|to tap the SUS304 tube|
|drill bits 6 mm|1 set|make the holes on heat block a bit larger|
|...|...|...|

(to be continued)

## 5 assembly

this toolhead needs certain sequence to assemble. 

1) the "compressir" part to hopper with M3x70 bolt. use both M3x100 bolts for alignment. after aligned, tighten the M3x70 then take out M3x100.

2) screw the tube to the heat block. then get the tube through "compressir 2" and the "compressir" and reach the end of hopper.

3) adjust the screw of tube to make it look fit (um... i don't know how to describe here). the tube is expected to be limited by the hopper and there should be no gap between all these parts.

4) two of M3x100 go through both heat blocks and compressirs to the hopper and screw in the heat set inserts.

5) get the TPU cylinder, knife it so that you can wrap it around the "compressir"

6) get the "front" and its retainer (is it right to call this thing retainer?), wrap the assembled part and use 4 of M3x35 screws to position it to the x carriage. don't tighten, we will need to rotate it and making some adjustment later.

7) assuming you have install the impactor on the motor shaft **(more details need to be explained here)**, install the motor mount to the motor. then use two of M3x?? to fix the motor on the "compressir".

8) put 608 bearing to it's clamp and install the clamp to the lower heat block. make sure the impactor go through the 608 bearing. **(more details need to be explained here)**

9) make adjustment to make sure:

   a) the motor body doesn't touch anything;
   b) the impactor can click the 608 bearing manually **(more details need to be explained here)**;
   c) the installation height is good and the nozzle isn't hitting the bed.

11) fasten the front M3 to finish. these M3 can be used to adjust the nozzle to be parallel to the bed. 

(to be continued)

