# ProtoHead_v6

This repository includes the mechanical parts for a Protohead v6 DIY FABtotum head. To be fully functional it requires either the original PCB of the v4 version, or this alternative PCB:

https://github.com/imarin2/Protohead_PCB_v4_FAB_24V

# So what is this in short?

A Bowden type hotend print only FABtotum head looking like this:

![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_3d.png?raw=true)

![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_mounted_1.png?raw=true)

![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_mounted_2.png?raw=true)

As its v4 predecesor, it is based on a low cost almost all metal hotend with reference 3DA-002 (long version, so coming with a press-fit) and looking something like this:
https://grabcad.com/library/hotend-3da-002-1

The "mechanical design" is made in FreeCAD and the full source is included.

The design requires of an Arduino Mini Pro to be available separately and attach to the PCB via a 4 pin angled header. The I2C pins must be connected separately using a cable. The firmware for the Arduino (currently only identifying itself as 0xFFFFFFFF) is here:
https://github.com/imarin2/ProtoHead

# What does v6 improve over v4?

- A lower amount of 3d printed parts: only 4 parts. There is a bigger part (around 10 hours of print time) and the remaining parts are small and can even be printed in batch mode.
![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_slic3r_fabtotum_connector.png?raw=true)
![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_batch_mode.png?raw=true)

- Reduced number of bolts and nuts, in fact only 2 M4 nuts for attachment of the extruder to the basic part and 2 M3 nuts for the PCB. The remaining M4 bolts are attached on tappered plastic.

- Improved extruder cooling: The input is very similar to v4. However the output is much more open, facilitating the out stream of hot air.

- Improved attachment of the part cooling duct using one M4 bolt.

![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_partially_exploded.png?raw=true)

![alt tag](https://github.com/imarin2/ProtoHead_v6/blob/master/images/Protohead_v6_partially_exploded_1.png?raw=true)

# Is this tested?
- Yes it is tested. The part cooling can be improved. A better duct design may help.

# Why are there so many STLs?

- There are two versions of the base and mount. The normal one and a 2mm offset version. The normal one is designed so that the tip is in the same position as the FABtotum hybrid head. Many persons seem to have problems that this position requires them to have the heated bed at the top-most position, which causes bad electrical contact of the heated bed. The 2mm offseted version has the nozzle point about 2 mm under the FABtotum hybrid head. Print the set that better suits you.
- There are 3 possible ducts. Take care that some ducts REQUIRE that you home on the right side of the FABtotum, as they hit on the raspicam support (it is a 2 mm thing, but still).

# What do I need to make it?
- An arduino mini pro, I have the one with the 368 chip, but any would do.
- A 3DA-002 (long version, so coming with a press-fit) with a 24V heater (sometimes is cheaper to get one with a 12V cartrige and buy a 24V cartridge separately). The thermistor that comes with them is generally a type 11 that, I hope, will be supported soon in FABlin if my last pull-request is merged.
- A 5V blower fan 5015S DC 5V 50x50x15mm
- An axial fan 60x60 mm, 5V.
- M4 and M3 bolts and nuts of different sizes (I will hopefully make a list some day, see the FreeCAD source). Better than the hex screws is to use hex socket (allen, imbus) screws.
