this is a vCP-e version where e for extruder axis in use. That is, FDM CAM slicers (e.g., OrcaSlicer) with default E gcode generation can be directly used for this toolhead in a print. 

<img width="365" height="377" alt="image" src="https://github.com/user-attachments/assets/784c701c-9509-4f92-b6b9-77299dd2b2ac" />

yes it's already this good without detailed tuning. check out how it moves: https://youtu.be/I5zWxPGP2qw 


the greatest benefit of using E axis in FDM slicer is that, you can do perfect *TRAVEL*, i.e., you can move your toolhead without leaking a single bit of cementitious mixture! 


recommended Klipper configuration for extruder:

```
rotation_distance: 5  ; this affects the pulse your drive sends to the motor if i m not wrong. to be simple, the smaller this is, the higher frequency the stepper does. 
microsteps: 8   ; or 16 is fine if your MCU doesn't report errors. 
full_steps_per_rotation: 200    ; for 4240 1.8 degree stepper motor
; gear_ratio is not needed

```

and its drive: 

```
interpolate: False  ; i don't know, LLM told me so
run_current: 0.5   ; worked longest for me. smaller run current can make your stepper not that easy to fail under fatigue caused by cyclic impact loading. 
hold_current: 0.5  ; better keep it same as the run_current

```

All CAD and 3MF uploaded for your reference. this version is much stabler than any of the previous versions (including many versions never uploaded...)

BOM of this toolhead: 

| name    | qty. |    descriptions  |
| -------- | ------- | ------- |
| stainless nozzle   |1 piece    |dimensions pls see the f3d CAD file thx|
| steel rod                 | 1 piece     |diameter of 6 mm, length of at least 40 mm               |
| M3x80 SHCS                  |   2 pcs  | for the upper part of mounting|
| M3x50 SHCS               |    2 pcs  | for the lower part of mounting |
| M3x8 SHCS          | 7 pcs   | |
| Heat set inserts (M3 Threaded Insert )        | 3 pcs   | The VORON "standard" ones (M3x5mmx4mm)|
| LSR (liquid silicone rubber)         | 7 pcs   |  20  degree or lower. 50 grams (A+B) is enough for one cast of the rubber buffer parts|
| stepper motor    |1 piecs |  4240 or longer      | 

<img width="576" height="478" alt="image" src="https://github.com/user-attachments/assets/69eb4f81-3166-426b-bef9-6ea85bb78186" />

printing recommendations:

- PETG is recommended for all the parts. 

- Only the bowl part needs a bit support (sorry for that, i don't want to but that's quicker. and i m not sure if the ears of the bowl can be cut off. better have them to simplify the installation). All other parts can be printed without support. You can use PLA to print the molds for LSR if stringing is a big issue for you. 

- maximize the wall/perimeter counts for all parts (except the "front" part) since they are going to suffer from heavy fatigue loading. i ve made them skinny as i think good enough so even if you print all parts in 100% plastic inside, it's not much heavy.

<img width="493" height="430" alt="image" src="https://github.com/user-attachments/assets/f048a972-2626-446a-9f8b-8e21460f6eb3" />

for the "bowl" part, only a bit of support have been painted in the .3mf fyr. 




for casting LSR, please screw your long M3 SHCS into the molds first, similar to the below photo (sorry that the below photo is showing a previous version but i m sure you can get what i mean): 

<img width="473" height="312" alt="image" src="https://github.com/user-attachments/assets/6f6e5994-469d-4025-b398-d8166ed2b397" />


------------

still testing stuff. but the news is, this version of toolhead is still not my ideal plan. new toolhead is on the way. 



