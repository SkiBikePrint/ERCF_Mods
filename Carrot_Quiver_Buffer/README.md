# ERCF_Mods
The "Carrot Quiver" ( https://discord.com/channels/460117602945990666/909743915475816458/1040665326410530836 ) , and integrated 3-slot filament buffer to mount on the back of a 3D printer with a v-slot extrusion based frame or use with an intermediate frame system.

BOM per 3 Slot Buffer:
1. Qty (2) 608-2RS bearing
2. Qty (2) heat set inserts either M5 (preferred) or M3 for the M3 version Wheel Block and Axle
3. Qty (2) M5x16 screws to secure wheel axle (any head style, I like the looks of button head for this design) or M3 for the M3 version Wheel Block and Axle
4. Qty (6) PC4-M10 pneumatic fittings for the bowden tubes
5. Qty (2) M5 roll-in t-nuts for Top and Bottom frame mounts
6. Qty (2) M5x16 Socket Head Cap Screws for Top and Bottom frame mounts



Printing Guidelines:

General:
- Material: ABS
- 0.2mm layer height
- 40% infill
- Wall Count: 4
- Solid Top/Bottom Layers: 5

Part Specific:
- Orientation suggestions are relative to a vertically mounted quiver

Wheel-2 Bearing.stl, Axle [M3 or M5] 2 Bearing.stl, Axle Spacer 2 Bearing.stl
- Orientation:  horizontal
- Supports: under bearing pocket overhang
<img src="https://user-images.githubusercontent.com/99146508/233866230-dec0d1e8-ea42-4073-9981-23632dba694f.png" width="200" height="200">

Bottom Block.stl
- Orientation:  upside down
- Supports: under mounting overhangs
<img src="https://user-images.githubusercontent.com/99146508/233863705-f1ffcbe8-fb5b-45d4-989a-ead8690f04f7.png" width="200" height="200">

Filament Slots Lower.stl
- Orientation:  vertical
- Supports: under base overhangs
<img src="https://user-images.githubusercontent.com/99146508/233864010-4586f18f-6f1f-48b0-bea9-a5dbbb27515a.png" width="200" height="200">

Filament Slots Upper.stl
- Orientation:  vertical
- Supports: under slot dividers at base
<img src="https://user-images.githubusercontent.com/99146508/233864766-6b052176-e57c-4d2c-845c-9a1897ab4dfd.png" width="200" height="200">

Top Mount.stl
- Orientation:  vertical
- Supports: under slot dividers at base and mounting overhangs
<img src="https://user-images.githubusercontent.com/99146508/233865046-6b3a7e8c-6fec-481d-8ccc-a11b4ac22bba.png" width="200" height="200">

Wheel Block [M3 or M5].stl
- Orientation:  upside down
- Supports: none
<img src="https://user-images.githubusercontent.com/99146508/233865181-52b5c38f-4d20-4791-b4f5-dc2ba823445f.png" width="200" height="200">



Assembly Steps:
1. Press fit the (2) 608-2RS bearings into each side of the wheel. It is IMPORTANT to press to the full depth of the pocket in the wheel.  You can use a second wheel bearing as a pressing tool to drive the bearing in to full depth.
2. Press Axle through bearing flush to the shoulder on the axle.  
3. Press a total of (8) 8x3mm neodymium into the Wheel Block and Top Mount.  Take care to get orientation the same for all four on each part correct so that they attract to each other and allow for the Wheel Block to be oriented on the Top Mount in either direction as it is a symmetrical part.  Removal slots are designed in for the magnets if you need to pop any out.  These should be a strong press fit bit depending on your print toleraces you can add a dab of superglue in the bottom of each hole as you are installing (again, confirm orientation before commiting to glue!).  Also, note that the magnets should slightly protrude out of the Top Mount and be recessed in the Wheel Block which provides for an alignment feature for the two blocks.  If further positive alignment is needed (but there shouldn't be a need) there is also holes in the these two parts for (2) M3 socket head cap screws.  You can screw the cap screws into the undersized holes in the Wheel Block.  The Top Mount has holes to receive the larger diameter of the socket head of the screws as a slip fit.
4. Press Axle Spacer onto axle flush to bearing.
5. Install heatset inserts into Wheel Block.
6. Screw in M5x16 (or M3x16) into heatset inserts.
7. If there is any rubbing/interference with the wheel and Wheel Block or Top Mount, locate spot(s) and clean up with exacto, sandpaper, etc.
8. Mount top and bottom mounts onto printer extrusions in the desire location using M5 roll-in T-nuts and M5x16 socket head cap screws.  Once buffer is fully assembled it is necessary to remove the slots to access these screws so you will want to get the mounts positioned into their final location if possible.  It is not the end of the world if you have to move them, it just takes a few minutes to pop the slots back out of the mounts.
9. Slide the first section of the "Filament Slots 165" part into top mount.  It will not snap into place so you need to hold it in place for now.
10. Slide the second "Filament Slots 165" part into the slots above it.
11. Slide the third section, the "Filament Slots Lower 165" part (it has a floor) into the bottom mount.  Firmly press it upwards until it snaps into place.  If you need to removed this part to remove or relocate the buffer you can use a flat bladed screwdriver to gently pry each side of the buffer slots from below while pushing down on the buffer slots to clear the retention tabs.

Congratulations, you are ready load some carrots into your quiver!  Does that sound inappropriate...???

I will caution that this design has tight tolerances around the wheel so that filament can not get lodged in any gaps or neighboring slots.  This means the axle needs to be aligned well and any rubbing between the wheel and the upper quiver parts may need to be filed, sanded, exacto knifed away.  I also used a M10 tap to clean out the M10x1 printed threads for the bowden fittings and M3 and M4 drill bits to clean up the bowden tube holes.  ~41mm of 4mm bowden tubing should insert through the fitting and down to where it seats in the Wheel Block.  If it does not go in ~41mm then the hole needs to be cleaned out with a 4mm drill bit.  Do not clean out the hole any deeper than 41mm as there is a step down to 3.2mm at this point to serve as a stop for the tubing.  You can run a 3mm drill bit through the entire hole if necessary to ensure an open path for filament.  So this design does require a little bit of post processing and tuning but once right it works well and is easy to thread and gain access to the filament.

For those who may not have M5 heatsets, I have added a version of the Wheel Block and Axle for M3 heatsets and screws.

It is important that the heatsets get installed straight.  One trick is to have a flat metal object ready and as your are pressing in the heatset, stop while it is still slightly above the surface of the wheel block and then finish seating it with the flat metal object pressing flat against the face of the Wheel Block axle boss.  Some people use black brass wax sealing stamps for this purpose.  I am using a small cylindrical calibration weight.
#
#
![image](https://user-images.githubusercontent.com/99146508/201385208-b8b762a2-a182-4361-b0ca-81ff4d03c71a.png)
![image](https://user-images.githubusercontent.com/99146508/201385286-f2886694-4932-4fee-a045-746c4a64086c.png)
![image](https://user-images.githubusercontent.com/99146508/201385442-d1756d61-d571-46b7-ad13-d2b10e60efc9.png)
![image](https://user-images.githubusercontent.com/99146508/204160788-83061850-f0b8-484d-b15e-9aba2a15ad57.png)
