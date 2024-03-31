To Do:
1.  Add comment re: beveling inner edge of PTFE tubes and cleaning up filament funnel hole if necessary.
2.  Update pics to latest parts
3.  Discuss tuning for rim slip vs o-ring slip and recommended roller surfaces.
4.  Cover o-ring replacement process.
5.  Design a spool weight?
6.  Check/update test code at bottom (single tool should be good)
7.  Mention design compromises around space/compactness.  It's a simpledesign so feel free to usermod to your heart's content!
 - height to fit Beta team's enclosures
 - width to fit 6 across a 350
    - this drove minimal roller rim size (and to print without supports)
8.  Discuss spool widths and the suggestion for usermods to widen as needed (i.e. KVP at 72mm wide, KVP printed "Koil" spool, etc.)
9.  Sync strongly recommended with NEMA17 do to slip resistance for fuller spools.
10.Some o-ring and gear grinding debris will be generated (incorporate a filament wiper?)


<h1 align="center">The "Filamentalist"</h1>


#  In Beta Testing

# An "analog" passive filament driven buffer project currently in Beta build/testing by an elite team of MMU buffering experts.

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/91a91edf711fef61f6d5f5e6cde604b599f564d3/Filamentalist/Images/Filamentalist1.jpg" width="250" height="400">
</p>

See video of 3 buffers swapping here:  https://photos.app.goo.gl/iyLBGgytfVCPNLVBA

# Theory of operation:
The Filamentalist uses the axial force delivered by the ERCF gear motor along the filament to load and unload to/from the filament spool.  An adjustable spring clamp forces the filament against two o-rings that sit on the drive pulley to create a high traction interface.  A one-way clutch style bearing locks against the drive shaft and rotates the filament spool to take up filament during an unload.  For loading and print extruding, the clutch modulates between engagement/disengagement allowing for effective free-spooling of the filament spool simliar to a roller style spool holder.  For unloading/buffering, some slip will occur between the filament and the o-ring interface and/or the spool rim and the rim roller of the buffer to account for the varying diameter range of a spool from full to empty (full spool = max slip, empty spool = no/minimal slip).

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/1798f91db1e9171a195a754c68675f0b5da8bcaf/Filamentalist/Images/Filamentalist6.jpg" width="300" height="400">
</p>

## **BOM:**

| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | 8mm D x 80mm Stainless Steel Dowell Pin | https://www.amazon.com/uxcell-Stainless-Chamfered-Support-Elements/dp/B0BC8VFSWD | or cut any 8mm stainless rod to 80mm lengths |
|   5   | MR608 bearings | Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  | MR608RS, MR608ZZ, etc. |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS, Aliexpress | 8mm Bore, 12mm length, 14.2mm Diameter. |
|   1   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | A locking clip is required and can be bought or printed (stl included) |
|   2   | #110 O-rings | Home Depot, https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/, Aliexpress | 13/16" ID, 1-1/16" OD or 20mm ID, 27mm OD Nitrile Butadiene Rubber|
|   1   | Spring  | https://www.amazon.com/gp/product/B08FDYJLYC/, Aliexpress | Like in extruders - 304 Stainless Steel,6mm OD,1mm Wire Size,7.5mm Compressed Length,15mm Free Length,37.2N Load Capacity |                                 |
|   2 | 3mm Heatset  |  | Voron standard size | one as a spring stop on the 3x50mm SHCS tensioning screw and the other set into the Tensioner Mnt |
|   1   | 3x35mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw anything in the range of 35mm +/- 10mm should work|
|   6   | 3x12 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Mnt and Rear Axle installation 8/10/12mm lengths will work|
|   2   | 3x18 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Arm clamp bearings and Tensioner Mnt pivot installation 16mm length will work |
|   2   | Rubber Band | https://www.amazon.com/dp/B0CPJPN41V | Size #94 (3 1/2" x 3/4"), any wide rubber bands in the 2.5"-3.5" size will work.  Can combined multiples across face of rollers |
| var.  | 2.5mm ID PTFE tubing | Amazon, Aliexpress, 3D printing vendors | 2.5mm ID recommended but you can try whatever you have.  Length depends on the distance from your buffer location to your ERCF inputs |


# Beta Test Potential Failure Modes to Test/Vette:

1.  O-ring durability.  The Chinese design used little, kinda thick silicone rings.  Those would wear through in ~70 cycles.  We are not seeing noticeable wear on the dual Buna-N o-rings at this point but at thousands of cycles we might see it.  Test CF filament.
2.  Potential slippage and grinding at the ERCF gear due to buffer drag and variation of top hat clamping force across the user base.  Not an issue so far in real-workd printing cases.  Can/does occur when running test scripts and cycling the same section of filament in-and-out of the gears over-and-over.
3.  The sharp bend at the clamp and tension could cause brittle filament to break.  SkiBikeMake and Cheesefrog have experienced this with specific spools.  SkiBikeMake plans to revise design of tensioner arm to include an additional rolloer guide to lessen the severity of the bend at the clamp.
4.  Potential for being on the edge of gear motor stall.  We are close to the stall threshold so the risk is that there is enough variation in the user community's ERCF builds, motors, and buffer builds that stall arises as an issue.  I definitely have occasionally experienced stall if something caused a small increase in resistance.  I may need to go NEMA17 to provide the headroom but will test on NEMA14 first.
5.  TPU may not be stiff enough to transmit power to the Drive Roller and/or kink/bunch in the bowden path and create a high friction situation that inhibits the ability to unload filament.  Shore Hardness 96A TPU has been tested and functioned well.


# Printing Guidelines:

## **General:**
- Material: ABS or ASA (~170 gm per site)
- Print Time: ~8hr 17min (based on the Ellis PIF profile speeds, accelerations, and volumes)
- 0.2mm layer height
- 40% infill recommended.  Linear style infills are fastest (rectilinear, monotonic, grid, triangles, stars, etc.)
- Wall Count: 4
- Solid Top/Bottom Layers: 5

## **Part Specific:**
- Orientation suggestions are relative to the installed assembly orientation and are shown in the slicer images below.
  
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/91a91edf711fef61f6d5f5e6cde604b599f564d3/Filamentalist/Images/Filamentalist1.jpg" width="125" height="200">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2280388ff64afb17f64c013231463de9fa64cc20/Filamentalist/Images/Filamentalist%20Sliced%20(Black).jpg" width="250" height="200">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2280388ff64afb17f64c013231463de9fa64cc20/Filamentalist/Images/Filamentalist%20Sliced%20(Orange).jpg" width="250" height="200">


| **Qty per Site** | **Part**  | **Pic** |  **Orientation**            | **Printed Supports Needed** | **Comments** |
|------|-----------------------------------------|------------|--------------------|-----|---------------------------------|
| 1       | Right Support | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Right%20Support.jpg" width="40" height="40"> |  Horizontal                   | N     |                                  |
| 1       | Left Support | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Left%20Support.jpg" width="40" height="40">                                                            | Horizontal                   | N     |                                  |
| 1       | Rear Roller Axle  | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rear%20Roller%20Axle.jpg" width="40" height="40"> | Horizontal | N | align flat of "D" to build plate |
| 1       | Rim Roller | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rim%20Roller.jpg" width="40" height="40">                                                   | Horizontal                | N       | Dished side up, scattered seams for press-fit bore     |
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

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/662caf6e50f499b8f42359d868c06f1419f9e44f/Filamentalist/Images/Tensioner_Mnt.jpg" width="400" height="350">

   - 1.1 Install 3mm heatset insert into Tensioner Mnt.
   - 1.2 Install the ECAS fitting into the Tensioner Mnt.  It should be a moderate press-in.  You may need to push it in firmly using the end of a 8mm steel shaft or printed rear axle shaft to get it to sit flush to the Tensioner Mnt mating surface.

# 2. Tensioner Arm Installation

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/b3865d1dce459810b443cc16736aa5070a433a71/Filamentalist/Images/Tensioner_Assy.jpg" width="400" height="350">

   - 2.1 Lay the Tensioner Arm Right part on a flat surface.  Slide the 608 bearing onto the bearing post.  Place the Tensioner Arm Left part into postion making sure the triangular indexing peg seats correctly at the bottom of the arm (light hammer taps with a tiny hammer may be required to seat).
   - 2.2 Place a 3x18 FHCS (or x16, x12) through the bearing mount hole of the Tensioner Arm Left part and moderately tighten the screw into the Tensioner Arm right piece.  Once installed verify that the bearing turns freely.
   - 2.3 Place a 3x18 FHCS (or x16, x12) through the hole in the Tensioner Arm Left part at the "nose" end and moderately tighten the screw into the Tensioner Arm right piece.  
   - 2.4 Install the Tensioner Arm onto the Tensioner Mnt using a 3x18mm FHCS screw (or x16) .  Tighten until snug and then back off until the arm rotates freely on the mount.
   - 2.5 Place an M3 washer followed by the spring onto an M3x35 SHCS (or x30, x40) and slide through the hole in the bottom of the arm assembly.  Screw the SHCS into the heatset insert of the Tensioner Mnt.  No tension should be on the spring at this point.

# 3. Drive Roller Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2f235409913aefef5219e5df66e258a4124f445c/Filamentalist/Images/Center%20Drive%20Roller%20with%201-Way%20Bearing.jpg" width="300" height="300">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f54f216b3775447bf40aa44d1984c6e510ab18f7/Filamentalist/Images/Drive%20Roller%20Assembly.jpg" width="400" height="400">

- 3.1 Press HF081412 One-Way Bearing into Center Drive Roller.  Orientation does not matter at this point.
- 3.2 Insert the Rim Roller Splined Hub part into the Rim Roller Splined part until they are flush with each other.  You may need to place them on a hard surface and give it a little hit to pop in flush.  Place the roller onto the Axle Pressing Tool as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Roller assembly until the shaft bottoms-out on the pocket in the Axle Pressing Tool.  If tapping the shaft in, you will hear when the shaft reaches the floor of the Axle Pressing Tool.

The purpose of this two-piece roller is to allow for future o-ring replacement by removing the rim from the hub versus having to press a roller off of the axle and then press it back on.  For o-ring replacement, remove the Drive Roller Assembly from the buffer (unscrew the Right and Left SUpports).  Then gently rock the splined roller and it should pop loose from the splined hub.  You can now remove the old o-rings and install a pair of new ones, pop the splined roller back onto the hub, and install the supports back on.

- 3.3 Slide (1) Center Drive Roller spacer followed by the Center Drive Roller (with One-way bearing already installed) followed by the second Center Drive Roller spacer onto the axle shaft.  Orientation is still not important.  If for universal harmony reasons you want the threaded Rim Rollers of each buffer all located on the same side then pick an orientation for the one-way bearing and stay with that.
- 3.4 Position the Rim Roller part (non threaded roller) onto the Axle Pressing Tool with dished side facing down as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Rim Roller part until the shaft bottoms-out in the pocket of the Axle Pressing Tool.

# 4. Base Assembly

There is an alternate version of the base that clips into two 2020 rails spaced 170mm apart (center-to-center). It enables quick add/remove/relocate capabilities and require no hardware to mount.  You print all of the same parts except for the 2 Base Supports that use the clip mount version.  Assmebly is the same.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Base%20MR608%20Bearings.jpg" width="300" height="350">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Rear%20Roller%20MR608%20Bearings.jpg" width="300" height="250">

   - 4.1 Press a total of (4) MR608 bearings into the Right Support, Left Support, and Rear Roller parts.  The Axle Pressing Tool can be used to aid with pressing the bearings into the deep bearing pockets of the Rear Roller.  Ensure the inner races of the bearings in the Right/Left Support parts turn freely.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/ab9b4967ab9052f7a707d3c00bb203262c5fd5c7/Filamentalist/Images/Base%20Assembly.jpg" width="400" height="350">

   - 4.2 Place the Tensioner Assembly around the Drive Roller Assembly and screw the Tensioner Mnt onto one of the Support parts using (2) 3x12 FHCS screws (or x10, x8).
#       !! THIS IS WHERE AXLE ORIENTATION MATTERS !!   
#          Orient the Drive roller assembly so that the one-way bearing locks in the filament unload/eject direction.  This can be verified byholding one of the outer drive rollers and rotating the center drive roller.  It should lock when the center roller is rotated in the direction away from the ERCF.
   - 4.3 Insert the Rear Roller Axle through the same base part aligning the "D" shape end to the flat in the 8mm pocket of the Support.  Ensure it presses all of the way in (you may need to tap it in a bit).  Secure with (1) 3x18 FHCS screw (or x10, x8).  
   - 4.4 Slide the Rear Roller onto the Rear Roller Axle.
   - 4.5 Install the opposite side Support part to assembly pressing in the D shaft end and securing with (3) 3x12 FHCS screws (or x10, x8).  Make sure there is no spring tension on the Tensioner arm for this step.
   - 4.6 Insert a section of bowden tube into the ECAS until it bottoms out/butts against the Tensioner Mnt behind the ECAS.  Place a locking clip in the ECAS (if you don't have these, an stl file is provided to print the locking clips).  2.5mm ID tubing is recommended to ensure good stiffness and minimal "buckling" of filament in the driven filament path.  Cut your section of tubing a little long for the location of the buffer and the run to the ERCF slot position.  You can fine tune/trim the length after installtion of the buffer.


# Tuning

The only tuning the system requires is Tensioner Arm clamping force.  The arm does not need an extreme amount of tension.  To tune the spring force, lift the tensioner and insert a section of filament through the o-ring bearing interface and into the bowden tube.  Hold the center roller by placing your thumb against the o-rings and try to pull the filament out.  You want the slip force to be slightly more than what the overall system drag is, so you have to imagine the range of gear motor pull force vs buffer drag and set a slip range in-between the two "imaginary" lines.  Adjust the spring tensioner screw accordingly and err on the light side.  Run the buffer (see test code below). If loose filament is forming around the filament spool during unload, tighten the spring tensioning screw.  If no loose filament is forming around the filament roll, gradually reduce the spring tension until loose filament starts to accumulate and then increase tension in ~1/2 screw turn increments until you feel you have the lightest tension that results in a tightly packed unload.


# Testing

Below are macros you can cut and paste into the bottom of your mmu_software.cfg to test and tune your buffers.

Happy multi-material printing and buffering!

Single rewinder test macro:

```[gcode_macro rewinder_test]
gcode:

    {% set gate = params.TESTGATE | default(0) | int %}
    {% set repeats = params.REPEATS | default(20) | int %}
    {% set length = params.LENGTH | default(800) | float %}
    {% set speed = params.SPEED | default(300) | float %}
    {% set accel = params.ACCEL | default(400) | float %}

    MMU_HOME TOOL={gate}

    MMU_TEST_LOAD LENGTH=50
    {% for n in range(repeats) %}

        MMU_SERVO POS=DOWN

            MMU_SELECT GATE={gate}
            MMU_TEST_LOAD LENGTH={test_load_length} # preload gate for a bit of length
            MMU_TEST_MOVE SPEED={speed} ACCEL={accel} MOVE={length}
            MMU_TEST_MOVE SPEED={speed} ACCEL={accel} MOVE=-{length}
            MMU_SERVO POS=UP

    {% endfor %}

    MMU_HOME```

Test Macro for cycling through multiple rewinders:

```[gcode_macro rewinder_test_multitool]
gcode:
    {% set gates = [5] %} # [0,1,2,3,4,5] move between these gates
    {% set test_load_length = params.TEST_LOAD_LENGTH | default(50) | float %}
    {% set repeats = params.REPEATS | default(20) | int %}
    {% set speed = params.SPEED | default(300) | float %}
    {% set accel = params.ACCEL | default(400) | float %}
    {% set length = params.LENGTH | default(800) | float %}

    MMU_HOME

#    MMU_TEST_LOAD LENGTH=50
    {% for n in range(repeats) %}
        {% for gate in gates %}
            MMU_SELECT GATE={gate}
            MMU_TEST_LOAD LENGTH={test_load_length} # preload gate for a bit of length
            MMU_TEST_MOVE SPEED={speed} ACCEL={accel} MOVE={length}
            MMU_SERVO POS=UP
            MMU_TEST_MOVE SPEED={speed} ACCEL={accel} MOVE=-{length}
            MMU_EJECT
            MMU_RECOVER

        {% endfor %}
  
    {% endfor %}
```
