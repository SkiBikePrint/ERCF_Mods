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
|   4   | MR608S bearings |  |  |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS?psc=1&ref=ppx_yo2ov_dt_b_product_details | 8mm Bore, 12mm length, 14.2mm Diameter |
|   2   | F683 flanged bearings  |  https://www.amazon.com/uxcell-F63800ZZ-10x19x7mm-Shielded-Bearings/dp/B0CP7N8V32/ref=sr_1_1_sspa?crid=2NINSDZD6AV58&keywords=f683%2Bbearing&qid=1706430383&sprefix=f683%2Bbearing%2Caps%2C163&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1 | F623 bearings will also work but recommend adding a tiny printed spacer between them |
|   2   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | Locking clips are required and can be bought or printed|
|   2   | #110 O-rings | Home Depot, https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/ref=sr_1_4?crid=35R5YUC9C64AF&keywords=13%2F16+id+1-1%2F16+OD+o-ring&qid=1706195690&s=industrial&sprefix=13%2F16+id+1-1%2F16+od+o-ring%2Cindustrial%2C179&sr=1-4 | 13/16" ID, 1-1/16" OD or 20mm ID, 27mm OD  |
|   1   | Spring  | https://www.amazon.com/gp/product/B08FDYJLYC/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1 | Like in extruders - 304 Stainless Steel,6mm OD,1mm Wire Size,7.5mm Compressed Length,15mm Free Length,37.2N Load Capacity |                                 |
|   1 | 3mm Heatset  |  | Voron standard size | |
|   1   | M3 Nylock Nut |  | Can use standard M3 nut and threadlocker/Superglues as an alternative |
|  misc | Various M3 BHCS and countersunk flathead screws to be detailed | | |
|   1   | 3x45mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw |
|


# Potential Failure Modes to Test/Vette:

1.  The o-ring wear rate is unacceptable.  The Chinese design used little, kinda thick silicone rings.  Those would wear through in ~70 cycles.  I am not seeing noticeable wear on the dual Buna-N o-rings at this point but at thousands of cycles we might see it.  Test CF filament.
2.  The one-way bearing behavior seems indeterminate.  I had to add a little friction at the spool roller rim on my proto rig to keep it from locking at load even though the shaft is rotating faster than the bearing race on load.  This is where I replaced 608’s on the shaft with a printed bushing and that slight additional drag at the shaft solved it.  I will be able to test by tonight or tomorrow (80mm shaft delivery delayed to tonight) as to if having the rear roller running on 608’s provides enough system friction to be able to stay with the 608’s up front or if I stay with the bushings (my test rig was a vertical feed spool holder for the belt version so no second spool roller).
3.  Slippage and grinding at the ERCF gear due to variation of top hat clamping force across the user base.
4.  The sharp bend at the clamp and tension could cause brittle filament to break (Glenn hasn't experienced yet with 3-4 spools that are relatively fresh)


# Printing Guidelines:

# Assembly Instructions:

#
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist1.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist2.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist3.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist4.jpg)
![image](https://github.com/SkiBikePrint/ERCF_Mods/blob/86302ecd9cdc81f8ce3870dd59cb7f5b5a7dbf87/Filamentalist/Images/Filamentalist5.jpg)


