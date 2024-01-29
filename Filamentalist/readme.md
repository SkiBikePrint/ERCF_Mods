#  In Beta Testing

# The "Filamentalist" 

# A passive filament driven buffer project currently in Beta build/testing by an elite team of MMU buffering experts.

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/319ebc64c6f7203fbcce4f664d93e957d442db1c/Filamentalist/Images/Filamentalist1.jpg" width="250" height="400">
</p>

# Theory of operation:
The Filamentalist uses the axial force delivered by the ERCF gear motor along the filament to drive a spool roller system for filament loading and unloading.  A one-way clutch style bearing locks against a drive shaft and drives the filament spool to take up filament during an unload.  For loading and print extruding the clutch disengages and allows for free-spooling of the filament spool simliar to a roller style spool holder.

The filament driven interface interface uses an adjustable spring clamp that forces the filament against two o-rings that sit on the drive pulley.  An ~3:1 spool rotation ratio is required to provide enough spool rotation range to buffer and unload onto a nearly empty filament spool or a new/full filament spool.  Because of this range, a full spool is overdriven and some slip is required in the system.  Thanks to the one-way clutch bearing this slip occurs between the spool rim rollers and the center drive pulley.  Depending on the weight of the spool the system may experience slippage at the rim on the front rollers.  This is an acceptable, low drag behavior.

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/d4a97d975891752a95d3143c7ecd344cd291694b/Filamentalist/Images/Filamentalist6.jpg" width="300" height="400">
</p>

## **BOM:**

| ** Qty per Site ** | ** Part ** | ** Source Reference ** | ** Comments ** |
|---------|-----------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
|   1   | 8mm Stainless Steel Rod  |https://www.amazon.com/dp/B09P9MC953?ref=ppx_yo2ov_dt_b_product_details&th=1 | Length to your preference.  75mm is the minimum for standard spool widths.  |                    |
|   4   | MR608 bearings | Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.  |  |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS?psc=1&ref=ppx_yo2ov_dt_b_product_details | 8mm Bore, 12mm length, 14.2mm Diameter |
|   2   | F683 flanged bearings  |  https://www.amazon.com/gp/product/B0CGX9C167/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1 | F623 bearings will also work but recommend adding a tiny printed spacer between them |
|   2   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | Locking clips are required and can be bought or printed (stl included)|
|   2   | #110 O-rings | Home Depot, https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/ref=sr_1_5?crid=1LSZX361EMYL1&keywords=%23110+13%2F16+buna-n+o-ring&qid=1706477152&s=industrial&sprefix=+110+13%2F16+buna-n+o-ring%2Cindustrial%2C166&sr=1-5 | 13/16" ID, 1-1/16" OD or 20mm ID, 27mm OD  |
|   1   | Spring  | https://www.amazon.com/gp/product/B08FDYJLYC/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1 | Like in extruders - 304 Stainless Steel,6mm OD,1mm Wire Size,7.5mm Compressed Length,15mm Free Length,37.2N Load Capacity |                                 |
|   1 | 3mm Heatset  |  | Voron standard size | |
|   1   | M3 Nylock Nut |  | Can use standard M3 nut and threadlocker/Superglues as an alternative |
|   1   | 3x45mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw |
|   6   | 3x12 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Mnt and Rear Axle installation |
|   2   | 3x18 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Arm clamp bearings and Tensioner Mnt pivot installation |


# Beta Test Potential Failure Modes to Test/Vette:

1.  The o-ring wear rate is unacceptable.  The Chinese design used little, kinda thick silicone rings.  Those would wear through in ~70 cycles.  I am not seeing noticeable wear on the dual Buna-N o-rings at this point but at thousands of cycles we might see it.  Test CF filament.
2.  The one-way bearing behavior seems indeterminate.  I had to add a little friction at the spool roller rim on my proto rig to keep it from locking at load even though the shaft is rotating faster than the bearing race on load.  This is where I replaced 608’s on the shaft with a printed bushing and that slight additional drag at the shaft solved it.  I will be able to test by tonight or tomorrow (80mm shaft delivery delayed to tonight) as to if having the rear roller running on 608’s provides enough system friction to be able to stay with the 608’s up front or if I stay with the bushings (my test rig was a vertical feed spool holder for the belt version so no second spool roller).
3.  Slippage and grinding at the ERCF gear due to variation of top hat clamping force across the user base.
4.  The sharp bend at the clamp and tension could cause brittle filament to break (Glenn hasn't experienced yet with 3-4 spools that are relatively fresh)
5.  If we are on the edge of gear motor stall.  We are close to the stall threshold so the risk is that there is enough variation in the user community's ERCF builds, motors, and buffer builds that stall arises as an issue.  I definitely have occasionally experienced stall if something caused a small increase in resistance.  I may need to go NEMA17 to provide the headroom but will test on NEMA14 first.


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
- Orientation suggestions are relative to the installed assembly orientation.
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/319ebc64c6f7203fbcce4f664d93e957d442db1c/Filamentalist/Images/Filamentalist1.jpg" width="125" height="200">

| **Qty per Site** | **Part**                           | **Orientation**            | **Printed Supports Needed**             | **Comments** |
|---------|-----------------------------------------------------------------|----------------------------|--------|---------------------------------|
| 1       | Right Support                                                            | Horizontal                   | N     |                                  |
| 1       | Left Support                                                            | Horizontal                   | N     |                                  |
| 1       | Rear Roller Axle  | Vertical | N | 5mm brim recommended, Scattered Seam Pattern |
| 1       | Rim Roller                                                    | Horizontal                | N       | Dished side up, scattered seams     |
| 1       | Hub-Rim Roller-Threaded                                       | Horizontal                   | N         |  Threaded end pointing up, scattered seams |
| 1       | Rim Roller-Threaded                                       | Horizontal                   | N         |  Threaded end pointing up, scattered seams  |
| 1       | Center Drive Roller                                                           | Horizontal                 | N        | Scattered seams                               |
|         | Tensioner Arm |  Horizontal                          | Y **Supports everywhere**                                        | see pic bellow for supports **Pending Grafton's 2-piece no-support version** |
| 1       | Tensioner Mnt                             | Vertical (as installed)                | Y for ECAS hole                  |  see pic for supports **Need built-in supports** |
| 1       | Rear Roller   |  Vertical  | N  |  Scattered seams |
| 1    | Axle Pressing Tool | Vertial | N | pocket opening up |
| 2 | ECAS Locking Clip | Horizontal | N | Tab up |

Tensioner Arm.stl supports:

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/9b6f7d0f2c5870e15f50cc03dbd517c558120d39/Filamentalist/Images/Tensioner%20Arm%20Supports.jpg" width="150" height="150">

Tensioner Mnt.stl supports:

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/9b6f7d0f2c5870e15f50cc03dbd517c558120d39/Filamentalist/Images/Tensioner%20Mnt%20Supports.jpg" width="225" height="225">

# Assembly Instructions:

# 1. Tensioner Mount Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/15306ce88a8914127b4261a9ca0a5065250d8bc6/Filamentalist/Images/Tensioner%20Mnt%20Assembly.jpg" width="400" height="400">

   - 1.1 Install 3mm heatset insert into Tensioner Mnt.
   - 1.2 Screw 3x45mm SHCS all of the way into threaded heatset insert
   - 1.3 Install 3mm Nylock nut onto 3x45mm SHCS with ~4mm of the screw protruding beyond the nut.  You can use a standard nut with threadlocker or Superglue as an alternative to a Nylock nut.  It is important that the nut does not turn on the screw once it is installed.
   - 1.4 Remove the lower rubber seal portion from two ECAS fittings and then install the fittings into the Tensioner Mnt.  It should be a light press-in.
   - 1.5 Insert a section of bowden tube now.  2.5mm ID is recommended.  The tube should protrude through the ECAS nearest the Drive Roller ~3-4mm.  Place locking clips in ECAS (if you don't have these an stl file is provided to print the locking clips).  Cut your section of tubing a little long for the location of the buffer and the run to the ERCF slot position.  You can fine tune/trim the length after installtion of the buffer.


# 2. Drive Roller Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2f235409913aefef5219e5df66e258a4124f445c/Filamentalist/Images/Center%20Drive%20Roller%20with%201-Way%20Bearing.jpg" width="300" height="300">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/d615fa2dca00380d7070693baba3a1330b1d9656/Filamentalist/Images/Drive%20Roller%20Assembly.jpg" width="400" height="400">

- 2.1 Press HF081412 One-Way Bearing into Center Drive Roller.  Orientation does not matter at this point.
- 2.2 Position the Hub-Rim Roller-Threaded part onto the Axle Pressing Tool as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Hub-Rim Roller-Threaded part until the shaft bottoms-out on the Axle Pressing Tool.
- 2.3 Slide the Center Drive Roller (with One-way bearing already installed) onto axle shaft.  Oreientation is still not important.  If for universal harmony reasons you want the threaded Rim Rollers of each buffer all located on the same side then pick an orientation for the one-way bearing and stay with that.
- 2.4 Position the Rim Roller part (non threaded roller) onto the Axle Pressing Tool as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Rim Roller part until the shaft bottoms-out on the Axle Pressing Tool.
- 2.5 Screw the Rim Roller-Threaded part onto the Hub-Rim Roller-Threaded part until flush with the hub.  The threads should not be so sticky that they cause the pressed-on hub to rotate on the steel shaft while screwing the roller on.  If necessary, clean up any rough mating surfaces with an X-acto knife and/or add a lubricant to the threads such as a small amount of silicone lubricant or parafin.

# 3. Base Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Base%20MR608%20Bearings.jpg" width="300" height="350">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Rear%20Roller%20MR608%20Bearings.jpg" width="300" height="250">

   - 3.1 Press a total of (4) MR608 bearings into the Right Support, Left Support, and Rear Roller parts.  The Axle Pressing Tool can be used to aid with pressing the bearings into the deep bearing pockets of the Rear Roller.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/ab9b4967ab9052f7a707d3c00bb203262c5fd5c7/Filamentalist/Images/Base%20Assembly.jpg" width="400" height="350">

   - 3.2 Screw the Tensioner Mnt onto one of the Support parts using (2) 3x12 FHCS screws.
   - 3.3 Insert the Rear Roller Axle through the same base part aligning the "D" shape end to the flat in the 8mm pocket ofr the Support and secure with (1) 3x18 FHCS screw.
   - 3.4 Slide the Rear Roller onto the Rear Roller Axle.
   - 3.5 Insert the Drive Roller Assembly Axle into the MR608 bearing of this same Support Part.
   - 3.6 Install the opposite side Support part to assembly with (3) 3x12 FHCS screws.

# 4. Tensioner Arm Installation

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/961bef88cec5f960faba6ed866f236203cd86fbc/Filamentalist/Images/Tensioner%20Mnt%20Assembly.jpg" width="400" height="350">

   - 4.1 Install the two F683 bearings into Tensioner Arm using a 3x18 FHCS screw.  There are tiny standoffs printed into the gap of the arm where the bearings install.  Inspect these, make sure the are there and there is no blobs that could rub on the bearing body.  Do not overtighten the screw.  Once installed verify that both bearings turn freely.  It may be hard to see if the bearings are turning.  One trick is to place sSharpie dots on the bearing faces to see if they move while turing the bearings.
   - 4.2 Install the Tensioner Arm onto the Tensioner Mnt with a 3x18mm FHCS screw.  Again, don't overtighten this screw.  The arm should rotate freely on the mount.
   - 4.3 With the 3x45mm SHCS spring tensioning screw screwed out to make space in the spring pocket of the mount, compress and force the spring into the opposing mount and arm spring pockets.  A small flat bladed screwdriver might help with this.


# Tuning

The only tuning the system requires is Tensioner Arm clamping force.  The arm does not need an extreme amount of tension.  To tune the spring force, lift the tensioner and insert a section of filament through the o-ring bearing interface and into the bowden tube.  Hold the center roller by placing your thumb against the o-rings and try to pull the filament out.  You want the slip force to be slightly more than what the overall system drag is, so you have to imagine the range of gear motor pull force vs buffer drag and set a slip range in-between the two "imaginary" lines.  Err on the light side.  Run the buffer and observe if any slippage is occuring at the o-rings.  I there is none, gradually reduce the spring tension until there is slippage and then increase tension in ~1/4 screw turn increments until you feel you have the lightest slip-free tension.


# Testing

Below is a macro you can cut and paste into the bottom of your ercf_software.cfg to test and tune the buffer.

Happy multi-material printing and buffering!


[gcode_macro rewinder_test]
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

#
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist1.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist2.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist3.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist4.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist5.jpg)


