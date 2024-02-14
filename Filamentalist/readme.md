<h1 align="center">The "Filamentalist"</h1>


#  In Beta Testing

# An "analog" passive filament driven buffer project currently in Beta build/testing by an elite team of MMU buffering experts.

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/319ebc64c6f7203fbcce4f664d93e957d442db1c/Filamentalist/Images/Filamentalist1.jpg" width="250" height="400">
</p>

# Theory of operation:
The Filamentalist uses the axial force delivered by the ERCF gear motor along the filament to drive a spool roller system for filament loading and unloading.  A one-way clutch style bearing locks against a drive shaft and drives the filament spool to take up filament during an unload.  For loading and print extruding the clutch disengages and allows for free-spooling of the filament spool simliar to a roller style spool holder.

The system uses an adjustable spring clamp that forces the filament against two rotating o-rings that sit on the drive pulley to create a high traction interface.  An ~3:1 spool rotation ratio is required to provide enough spool rotation range to buffer and unload onto a nearly empty filament spool or a new/full filament spool.  Because of this range, a full spool is overdriven and some slip is required in the system.  This slip occurs between the bearings in the Filament Tensioner Arm and the o-ring gripping point on the drive roller.  As the tension on the filament from the overdriven spool increases, the spring tensioned Tensioner Arm lifts and momentarily releases grip on the filament.  This happens in a smooth, continuous, and modulated fashion at various degrees depending on the diameter of the ever changing filament roll.

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/d4a97d975891752a95d3143c7ecd344cd291694b/Filamentalist/Images/Filamentalist6.jpg" width="300" height="400">
</p>

## **BOM:**

| ** Qty per Site ** | ** Part ** | ** Source Reference ** | ** Comments ** |
|---------|-----------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
|   1   | 8mm Stainless Steel Rod  |https://www.amazon.com/dp/B09P9MC953?ref=ppx_yo2ov_dt_b_product_details&th=1 | Length to your preference.  75mm is the minimum for standard spool widths.  If you use something other than 80mm the Center Drive Roller Spacer widths require adjustment|                    |
|   4   | MR608 bearings | Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  |  |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS?psc=1&ref=ppx_yo2ov_dt_b_product_details | 8mm Bore, 12mm length, 14.2mm Diameter |
|   2   | F683 flanged bearings  |  https://www.amazon.com/gp/product/B0CGX9C167/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1 |  |
|   1   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | Locking clips are required and can be bought or printed (stl included)|
|   2   | #110 O-rings | Home Depot, https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/ref=sr_1_5?crid=1LSZX361EMYL1&keywords=%23110+13%2F16+buna-n+o-ring&qid=1706477152&s=industrial&sprefix=+110+13%2F16+buna-n+o-ring%2Cindustrial%2C166&sr=1-5 | 13/16" ID, 1-1/16" OD or 20mm ID, 27mm OD  |
|   1   | Spring  | https://www.amazon.com/gp/product/B08FDYJLYC/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1 | Like in extruders - 304 Stainless Steel,6mm OD,1mm Wire Size,7.5mm Compressed Length,15mm Free Length,37.2N Load Capacity |                                 |
|   2 | 3mm Heatset  |  | Voron standard size | one as a spring stop on the 3x45mm SHCS tensioning screw and the other set into the Tensioner Mnt |
|   1   | 3x50mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw anything in the range of 40mm + should work|
|   6   | 3x12 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Mnt and Rear Axle installation |
|   2   | 3x18 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Arm clamp bearings and Tensioner Mnt pivot installation |
| var.  | 2.5mm ID PTFE tubing | | 2.5mm ID recommended but you can try whatever you have.  Length depends on the distance from your buffer location to your ERCF inputs | |


# Beta Test Potential Failure Modes to Test/Vette:

1.  O-ring durability.  The Chinese design used little, kinda thick silicone rings.  Those would wear through in ~70 cycles.  We are not seeing noticeable wear on the dual Buna-N o-rings at this point but at thousands of cycles we might see it.  Test CF filament.
2.  Potential slippage and grinding at the ERCF gear due to buffer drag and variation of top hat clamping force across the user base.  Not an issue so far in real-workd printing cases.  Can/does occur when running test scripts and cycling the same section of filament in-and-out of the gears over-and-over.
3.  The sharp bend at the clamp and tension could cause brittle filament to break.  SkiBikeMake and Cheesefrog have experienced this with specific spools.  SkiBikeMake plans to revise design of tensioner arm to include an additional rolloer guide to lessen the severity of the bend at the clamp.
4.  Potential for being on the edge of gear motor stall.  We are close to the stall threshold so the risk is that there is enough variation in the user community's ERCF builds, motors, and buffer builds that stall arises as an issue.  I definitely have occasionally experienced stall if something caused a small increase in resistance.  I may need to go NEMA17 to provide the headroom but will test on NEMA14 first.
5.  TPU may not be stiff enough to transmit power to the Drive Roller and/or kink/bunch in the bowden path and create a high friction situation that inhibits the ability to unload filament.


# Printing Guidelines:

## **General:**
- Material: ABS or ASA (~170 gm per site)
- Print Time: ~8hr 17min (based on the Ellis PIF profile speeds, accelerations, and volumes)
- 0.2mm layer height
- 40% infill recommended.  Linear style infills are fastest (rectilinear, monotonic, grid, triangles, stars, etc.)
- Wall Count: 4
- Solid Top/Bottom Layers: 5
- Seams:  Scattered seam pattern recommended for cyclindrical and press fit parts to aid in maintaining concentricity

## **Part Specific:**
- Orientation suggestions are relative to the installed assembly orientation and are shown in the slicer images below.
  
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/319ebc64c6f7203fbcce4f664d93e957d442db1c/Filamentalist/Images/Filamentalist1.jpg" width="125" height="200">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2280388ff64afb17f64c013231463de9fa64cc20/Filamentalist/Images/Filamentalist%20Sliced%20(Black).jpg" width="250" height="200">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2280388ff64afb17f64c013231463de9fa64cc20/Filamentalist/Images/Filamentalist%20Sliced%20(Orange).jpg" width="250" height="200">


| **Qty per Site** | **Part**  | **Pic** |  **Orientation**            | **Printed Supports Needed** | **Comments** |
|------|-----------------------------------------|------------|--------------------|-----|---------------------------------|
| 1       | Right Support | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Right%20Support.jpg" width="40" height="40"> |  Horizontal                   | N     |                                  |
| 1       | Left Support | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Left%20Support.jpg" width="40" height="40">                                                            | Horizontal                   | N     |                                  |
| 1       | Rear Roller Axle  | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rear%20Roller%20Axle.jpg" width="40" height="40"> | Horizontal | N | align flat of "D" to build plate |
| 1       | Rim Roller | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rim%20Roller.jpg" width="40" height="40">                                                   | Horizontal                | N       | Dished side up, scattered seams for press-fit bore     |
| 1       | Hub-Rim Roller-Splined |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Hub-Rim%20Roller.jpg" width="40" height="40">                                    | Horizontal                   | N         |   |
| 1       | Rim Roller-Splined | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rim%20Roller-Threaded.jpg" width="40" height="40">                                     | Horizontal                   | N         |    |
| 1       | Center Drive Roller  | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Center%20Drive%20Roller.jpg" width="40" height="40">                                                        | Horizontal                 | N        | Scattered seams for press fit-bore                              |
| 2       | Center Drive Roller Spacer |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Center%20Drive%20Roller%20Spacer.jpg" width="40" height="40">    | Horizontal                 | N        | Scattered seams                               |
|         | Tensioner Arm Left |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Tensioner%20Arm%20Left.jpg" width="40" height="40"> | Horizontal                          |        |  |
|         | Tensioner Arm Right |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Tensioner%20Arm%20Right.jpg" width="40" height="40"> | Horizontal                          |        |  |
| 1       | Tensioner Mnt | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Tensioner%20Mnt.jpg" width="40" height="40">                           | Vertical (as installed)                |   |   |
| 1       | Rear Roller   | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Rear%20Roller.jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1    | Axle Pressing Tool | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Axle%20Pressing%20Tool.jpg" width="40" height="40"> | Vertial | N | Pocket opening up.  Print with 100% infill for reuse strength and durability when building multiple buffers. |
| 2 | ECAS Locking Clip | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/6837e24c214d6256fef5f5dbc52ac9dc8a1a9989/Filamentalist/Images/ECAS%20Locking%20Clip.jpg" width="40" height="40"> |  Horizontal | N | Tab up |


There is an alternate version of the base that clips into two 2020 rails spaced 170mm apart (center-to-center). It enables quick add/remove/relocate capabilities and requires no hardware to mount.  You print all of the same parts except for the 2 Base Supports that use the clip mount version.  Assembly is the same.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f96422acb504d4f098fd575ae8534f495f92b699/Filamentalist/Images/Clip%20Mount%20Version.jpg" width="400" height="250">

# Assembly Instructions:

# 1. Tensioner Mount Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/b4d31df2ec4a3d861791060331a895c2e0212f95/Filamentalist/Images/Tensioner%20Mnt%20Assembly.jpg" width="400" height="350">

   - 1.1 Install 3mm heatset insert into Tensioner Mnt.
   - 1.2 Screw 3x45mm SHCS mostly into the threaded heatset insert with ~10mm protruding out the other end.
   - 1.3 Thread another 3mm heatset insert onto 3x45mm SHCS with ~3mm of the screw protruding beyond it.  Use Superglue or threadlocker (Loctite) to lock it in place.  It is important that the heatset insert does not turn on the screw once it is installed.
   - 1.4 Install the ECAS fitting into the Tensioner Mnt.  It should be a moderate press-in.  You may need to push it in firmly using the end of a 8mm steel shaft or printed rear axle shaft to get it to sit flush to the Tensioner Mnt mating surface.

# 2. Tensioner Arm Installation

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/b4d31df2ec4a3d861791060331a895c2e0212f95/Filamentalist/Images/Tensioner%20Mnt%20Assembly.jpg" width="400" height="350">

   - 2.1 Place a 3x18 FHCS through the bearing mount hole of the Tensioner Arm Right part and slide the two F683 bearins onto it with the flanges facing outward (this should be a clearance hole).  Place the Tensioner Arm Left part into postion making sure the square indexing peg seats correctly at the bottom of the arm.  Moderatly tighten the screw into the Tensioner Arm right piece and then back off ~1/4 turn.  Once installed verify that both bearings turn freely.  It may be hard to see if the bearings are turning.  One trick is to place Sharpie dots on the bearing faces to see if they move while turning the bearings.
   - 2.2 Screw 3x45mm spring tensioning screw back into the body of the Tensioner Mnt to get it out of the way.
   - 2.3 Install the Tensioner Arm onto the Tensioner Mnt using a 3x18mm FHCS screw.  Tighten until snug and then back off ~1/4 turn.  The arm should rotate freely on the mount.
   - 2.4 Place the spring into the spring pockets of both the mount and the arm, and tape the bottom of the arm to the mount to prevent the spring from falling out while completing the rest of the build.  No tension should be on the spring at this point.

# 3. Drive Roller Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2f235409913aefef5219e5df66e258a4124f445c/Filamentalist/Images/Center%20Drive%20Roller%20with%201-Way%20Bearing.jpg" width="300" height="300">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f54f216b3775447bf40aa44d1984c6e510ab18f7/Filamentalist/Images/Drive%20Roller%20Assembly.jpg" width="400" height="400">

- 3.1 Press HF081412 One-Way Bearing into Center Drive Roller.  Orientation does not matter at this point.
- 3.2 Insert the Rim Roller Splined Hub part into the Rim Roller Splined part until they are flush with each other.  You may need to place them on a hard surface and give it a little hit to pop in flush.  Place the roller onto the Axle Pressing Tool as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Roller assembly until the shaft bottoms-out on the pocket in the Axle Pressing Tool.  If tapping the shaft in, you will hear when the shaft reaches the floor of the Axle Pressing Tool.

The purpose of this two-piece roller is to allow for future o-ring replacement by removing the rim from the hub versus having to press a roller off of the axle and then press it back on.  For o-ring replacement, remove the Drive Roller Assembly from the buffer (unscrew the Right and Left SUpports).  Then gently rock the splined roller and it should pop loose from the splined hub.  You can now remove the old o-rings and install a pair of new ones, pop the splined roller back onto the hub, and install the supports back on.

- 3.3 Slide (1) Center Drive Roller spacer followed by the Center Drive Roller (with One-way bearing already installed) followed by the second Center Drive Roller spacer onto the axle shaft.  Orientation is still not important.  If for universal harmony reasons you want the threaded Rim Rollers of each buffer all located on the same side then pick an orientation for the one-way bearing and stay with that.
- 3.4 Position the Rim Roller part (non threaded roller) onto the Axle Pressing Tool with dished side facing down as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Rim Roller part until the shaft bottoms-out in the pocket of the Axle Pressing Tool.

# 4. Base Assembly

There is an alternate version of the base that clips into two 2020 rails spaced 170mm apart (center-to-center). It enables quick add/remove/relocate capabilities and require no hardware to mount.  You print all of the same parts expect for the 2 Base Supports that use the clip mount version.  Assmebly is the same.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Base%20MR608%20Bearings.jpg" width="300" height="350">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Rear%20Roller%20MR608%20Bearings.jpg" width="300" height="250">

   - 4.1 Press a total of (4) MR608 bearings into the Right Support, Left Support, and Rear Roller parts.  The Axle Pressing Tool can be used to aid with pressing the bearings into the deep bearing pockets of the Rear Roller.  Ensure the inner races of the bearings in the Right/Left Support parts turn freely.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/ab9b4967ab9052f7a707d3c00bb203262c5fd5c7/Filamentalist/Images/Base%20Assembly.jpg" width="400" height="350">

   - 4.2 Screw the Tensioner Mnt onto one of the Support parts using (2) 3x12 FHCS screws.
   - 4.3 Insert the Rear Roller Axle through the same base part aligning the "D" shape end to the flat in the 8mm pocket of the Support.  Ensure it presses all of the way in (you may need to tap it in a bit).  Secure with (1) 3x18 FHCS screw.  
   - 4.4 Slide the Rear Roller onto the Rear Roller Axle.
   - 4.5 Insert the Drive Roller Assembly Axle into the MR608 bearing of this same Support Part.  
#              !! THIS IS WHERE AXLE ORIENTATION MATTERS !! 
   - Orient the Drive roller assembly so that the one-way bearing locks in the filament unload/eject direction.  This can be verified by holding one of the outer drive rollers and rotating the center drive roller.  It should lock when the center roller is rotated outward (i.e. driving filament away from the ERCF).
- 3.6 Install the opposite side Support part to assembly pressing in the D shaft end and securing with (3) 3x12 FHCS screws.  Make sure there is no spring tension on the Tensioner arm for this step.
- 3.7 Insert a section of bowden tube into the ECAS until it bottoms out/butts against the Tensioner Mnt behind the ECAS.  Place a locking clip in the ECAS (if you don't have these, an stl file is provided to print the locking clips).  2.5mm ID tubing is recommended to ensure good stiffness and minimal "buckling" of filament in the driven filament path.  Cut your section of tubing a little long for the location of the buffer and the run to the ERCF slot position.  You can fine tune/trim the length after installtion of the buffer.


# Tuning

The only tuning the system requires is Tensioner Arm clamping force.  The arm does not need an extreme amount of tension.  To tune the spring force, lift the tensioner and insert a section of filament through the o-ring bearing interface and into the bowden tube.  Hold the center roller by placing your thumb against the o-rings and try to pull the filament out.  You want the slip force to be slightly more than what the overall system drag is, so you have to imagine the range of gear motor pull force vs buffer drag and set a slip range in-between the two "imaginary" lines.  Err on the light side.  Run the buffer and observe if any slippage is occuring at the o-rings.  I there is none, gradually reduce the spring tension until there is slippage and then increase tension in ~1/4 screw turn increments until you feel you have the lightest slip-free tension.


# Testing

Below is a macro you can cut and paste into the bottom of your ercf_software.cfg to test and tune the buffer.

Happy multi-material printing and buffering!


```[gcode_macro rewinder_test]
gcode:
    ERCF_TEST_LOAD LENGTH=50
    {% for n in range(20) %}
# cycles currently set at 20, i.e. range(20).  You can changes this however you chose.
        ERCF_SERVO_DOWN
        MANUAL_STEPPER STEPPER="gear_stepper" SPEED=300 ACCEL=400 MOVE=800
# change the SPEED and ACCEL as you see fit
         ERCF_SERVO_UP
        P4 500 # dwell for a bit
# to stop a macro mid-cycle you must use the e-stop.  This dwell allows you to hit the e-stop while the servo is up so that you can pull the filament out of the ERCF while the printer/macro is stopped
        ERCF_SERVO_DOWN
        MANUAL_STEPPER STEPPER="gear_stepper" SPEED=300 ACCEL=400 MOVE=-800

         ERCF_SERVO_UP
        P4 500 # dwell for a bit
    {% endfor %}

```
