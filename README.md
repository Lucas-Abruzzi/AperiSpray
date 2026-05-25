# AperiSpray

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Cover-page.png" style="width:75%;">

## Table of Contents
- [Overview of Source](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#overview-of-source)
    - [Disclaimer](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#disclaimer)
    - [Schematic](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#schematic)
    - [Parts List](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#parts-list)
- [Source Construction](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#source-construction)
    - [3D Printing](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#printing-parts)
    - [Source Disassembly](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#source-disassembly)
    - [Soldering the Electronics](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#soldering-electronics)
    - [Assembling the Shaft Assembly](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#assembling-the-shaft-assembly)
    - [Assembling the High-Voltage Termination](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#assembling-the-high-voltage-termination)
    - [Installing the Strip Mount](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#installing-the-strip-mount)
    - [Installing Assembly in the ESI Housing](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#installing-assembly-in-the-esi-housing)
- [Opensource Strip Construction](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#opensource-strip-construction)
    - [Cutting Paper Strips](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#cutting-paper-strips)
    - [Printing Strip Holder and Strip Holder Clips](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#printing-strip-holders-and-strip-holder-clips)
    - [Assembling Strips](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#assembling-strips)
- [Operating Instructions](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#operating-instructions)
    - [Positioning Calibration Procedure](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#positioning-calibration-procedure)
    - [Spray Solvent Delivery Set Up](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#spray-solvent-delivery-set-up)
    - [Method Development](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#method-development)
    - [Sample Preparation](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#sample-preparation)
    - [Loading and Analyzing a Paper Strip](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#loading-and-running-a-paper-strip)
    - [Trouble Shooting](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#trouble-shooting)
    - [Unloading Used Paper Strips](https://github.com/Lucas-Abruzzi/AperiSpray/tree/main#unloading-used-paper-strips)

## Overview of Source

The AperiSpray is a low-cost, simple to use assembly that converts existing Thermo Scientific OptaMax NG heated electrospray ionization (H-ESI) housings into paper spray ion sources, making use of 3D-printed parts and off-the-shelf hardware. AperiSpray features instrument-controlled high-voltage and spray solvent delivery and can use either in-house-built or commercially available paper spray strips. Many laboratories that perform routine LC-MS analyses already have surplus H-ESI sources available for conversion, and those that don’t, can purchase inexpensive used or defective housings from third party sellers, making AperiSpray a low-investment option for those wanting to experiment with PS-MS. Additionally, unlike the commercial PS-MS platform, AperiSpray is compatible with almost any Thermo Scientific mass spectrometer with an atmospheric pressure interface, allowing it to be coupled to high-resolution Orbitrap instruments. Although outside the scope of this document, components of this design could be adapted to construct PSI sources for instruments from other manufacturers.

### Disclaimer

Following these instructions may void instrument warranties, risk damage to instruments, and/or expose you to risk of electrical shock. Do so at your own risk. Do not perform modifications to the source while it is mounted to the instrument. Ensure that the instrument is in “standby” or “off” before attempting to load or unload a paper strip from the source and never raise the shaft while the spray voltage is turned on.

### Schematic

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Schematic.png" style="width:75%;">

### Parts List

| Designator | Qty | Source | Part No. | Cost /ea (CAD) | Material |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Shaft guide  | 1 | 3D-printed | N/A | $2.43 | PLA-CF |
| Shaft  | 1 | 3D-printed | N/A | $2.46 | PLA-CF |
| Cap  | 1 | 3D-printed | N/A | $1.46 | PLA-CF |
| Electronics enclosure | 1 | 3D-printed | N/A | $1.60 | PLA-CF |
| HV female connector | 1 | 3D-printed | N/A | $0.16 | PLA |
| Strip mount | 1 | 3D-printed | N/A | $0.72 | PA6-GF |
| Strip holder + clip  | N/A* | 3D-printed | N/A | $0.06 | PA6-GF |
| Strip tray | 1 | 3D-printed | N/A | $0.73 | PLA |
| Harting connector | 1 | Digikey.ca | [1195-1808-ND](https://www.digikey.ca/en/products/detail/harting/09200102612/3180391?s=N4IgTCBcDaIIxwJwFYC0cAcAGDqByAIiALoC%2BQA) | $29.82 | PC |
| 2.15 kΩ resistor | 1 | Digikey.ca | [56-SFR2500002151FR500CT-ND](https://www.digikey.ca/en/products/detail/vishay-beyschlag-draloric-bc-components/SFR2500002151FR500/595788?s=N4IgTCBcDaIKwDYC0BlAYgJTHADHnYAjHIZrjgMIAqSAcgCIgC6AvkA) | $0.20 | Ceramic |
| 22 MΩ resistor | 1 | Digikey.ca | [BC4913CT-ND](https://www.digikey.ca/en/products/detail/vishay-beyschlag-draloric-bc-components/VR37000002205JA100/7350819?s=N4IgTCBcDaIEIGEAsBOAjAZgQFQLQDkAREAXQF8g) | $0.74 | Ceramic |
| Pogo pin | 1 | Digikey.ca | [54-7949-0-15-20-09-14-11-0-ND](https://www.digikey.ca/en/products/detail/mill-max-manufacturing-corp/7949-0-15-20-09-14-11-0/13531603?s=N4IgTCBcDaIKwBYC0B2AnAtSAMSCMcSYu2WeyeeOSAcgCIgC6AvkA) | $4.76 | Brass alloy |
| 20 AWG wire | 4 cm | mcmaster.com | [8054T184](https://www.mcmaster.com/products/8054t184/) | $0.02 | Copper |
| HV cable | 70 cm | mcmaster.com | [8296K17](https://www.mcmaster.com/products/8296k17/) | $25.67 | Silicone |
| 1/4"-PP tubing | 6 cm | mcmaster.com | [5392K12](https://www.mcmaster.com/catalog/132/170/5392K12) | $0.20 | PP |
| Threaded insert | 1 | mcmaster.com | [94100A110](https://www.mcmaster.com/products/94100a110/) | $0.70 | SS |
| Set screw (cap) | 1 | mcmaster.com | [92605A098](https://www.mcmaster.com/products/92605a098/) | $0.15 | SS |
| Thumb knob | 1 | mcmaster.com | [2577K21](https://www.mcmaster.com/products/2577k21/) | $12.57 | SS |
| Flanged sleeve bearing | 1 | mcmaster.com | [7815K11](https://www.mcmaster.com/products/7815k11/) | $5.17 | Bronze |
| Lead screw | 1 | mcmaster.com | [6350K694](https://www.mcmaster.com/products/6350k694/) | $81.44 | SS |
| Shaft collar | 1 | mcmaster.com | [6462K12](https://www.mcmaster.com/products/6462k12/) | $7.17 | SS |
| Lead screw nut | 1 | mcmaster.com | [6350K683](https://www.mcmaster.com/products/6350k683/) | $31.63 | POM |
| Mounting screws | 2 | mcmaster.com | [92196A151](https://www.mcmaster.com/products/92196a151/) | $0.11 | SS |
| Set screw (strip-mount) | 1 | mcmaster.com | [92765A005](https://www.mcmaster.com/products/92765a005/) | $0.33 | Steel alloy |
| HV contact screws | N/A* | mcmaster.com | [92949A174](https://www.mcmaster.com/products/92949a174/) | $0.07 | SS |
| Chromatography paper | N/A* | Fishersci.ca | [057146](https://www.fishersci.ca/shop/products/whatman-31et-chr-chromatography-paper/057146?searchHijack=true&searchTerm=057146&searchType=RAPID&matchedCatNo=057146) | $0.02 | Cellulose |
| PEEK nut | 1 | Coleparmer.ca | [0201343](https://www.coleparmer.ca/i/idex-fingertight-one-piece-long-thread-natural-peek-1-16-od-tubing-10-32-coned-10-pk/0201343?searchterm=0201343) | $11.32 | PEEK |
| PEEK nut adapter | 1 | Coleparmer.ca | [0201420](https://www.coleparmer.ca/i/idex-threaded-adapter-peek-0-040-id-10-32-coned-f-to-1-4-28-flat-bottom-m/0201420) | $40.81 | PEEK |
| Crimp butt connector | 1 | grainger.ca | [GGE4FRH9](https://www.grainger.ca/en/product/SPLICE-CONNECTOR-VINYL-RED-PK100/p/GGE4FRH9?searchBar=true&nls=NLSAA_NA-7&initialSearchTerm) | $0.13 | Vinyl |
| Pen tube | 1 | grainger.ca | [TOYGSM11-2](https://www.grainger.ca/en/product/PEN-BALLPT-MED-BIC-ROUND-BLUE-12-PK/p/TOYGSM11-2?searchBar=true&nls=NLSAA_NA-7&initialSearchTerm) | $0.47 | PP |
| Heat shrink | 1 | homedepot.ca | [1000843481](https://www.homedepot.ca/product/gardner-bender-3-inch-l-x-assorted-diameter-heat-shrink-black-tubing-set-of-160-/1000843481?searchterm=1000843481) | $25.41 | Polyolefin |

*Denotes consumable

## Source Construction

### Printing Parts

#### Filament
For the cap, shaft, shaft guide, electronics enclosure, and strip tray, most standard FDM filament materials are acceptable. We prefer carbon-fiber PLA because it is dimensionally stable, easy to print and has a desirable surface texture. For the strip mount and strip holders, we recommend a material that is resistant to solvent to prevent interference and instrument contamination. In normal operation of the source, the strip mount should not come in direct contact with spray solvent, so PLA or ABS can be used if necessary, however in our experience, solvent overflow will occasionally occur while calibrating solvent deposition rate and volume, so a solvent-resistant material is highly recommended. Strip holders come in contact with solvent during normal operation. Some good options for strip holders (and strip mounts) include natural polyoxymethylene (POM), and natural PA6 Nylon. We recommend natural glass fiber reinforced PA6 nylon as it is both chemically resistant and easy to print on consumer grade printers, whereas POM suffers from poor print-bed adhesion and severe warping.

#### Printer Settings
Printer settings are highly dependent on the filament material and printer. We recommend using your printer’s default print settings for the filament chosen and adjusting as necessary.

#### Slicer Settings

<ins>Shaft guide:</ins>

Print the shaft guide in an upright position. Tree support is recommended for the overhang in the loading cutaway.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/shaft_guide-sliced.JPG" style="width:75%;">

<ins>Shaft:</ins>

We recommend printing the shaft upright to ensure the surface that mates with the lead screw nut is flat. You will need support under the mounting bracket on the inside of the shaft. 

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Shaft_sliced.JPG" style="width:75%;">

<ins>Cap:</ins>

The cap should be printed upside down with the top face against the build plate. No support is necessary. 

<ins>Electronics enclosure:</ins>

Print the electronics enclosure with the backside down on the build plate. Support is only needed for the bottom lips.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Electronics_enclosure-sliced.JPG" style="width:75%;">

<ins>HV female connector:</ins>

Print with the threaded end up. No support is needed.

<ins>Strip mount (for open-source or commercial strips):</ins>

The strip mount is best printed upside down with support under the ridge, in the strip pocket, and in the threaded solvent hole.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Strip-mount_sliced.JPG" style="width:75%;">

<ins>Calibration Strips:</ins>

Calibration strips are for calibrating the strip position relative to the inlet of the mass spectrometer. They are inserted into the strip pocket on the strip mount and extend to where the opening of the inlet should be relative to the strip mount. By default, the calibration strips extend 4 mm further from the strip mount than actual paper strips would to create a 4 mm gap between paper strips and the inlet when used to calibrate positioning. If a larger or smaller gap is desired, the FreeCAD file for the calibration strips can be modified by increasing or decreasing the “Inlet_gap” variable in the variable set. Print calibration strips out of whatever filament you have on hand. They are best printed in an upright position with the backside against the print bed. Support is only necessary on the calibration strip for the commercial strip mount.

### Source Disassembly

Remove the 4 screws holding the front plate on the source and pull the front plate away from the housing.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_1.jpg" style="width:50%;">

Remove the metal cover protecting the electronic and pneumatic connections.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_2.jpg" style="width:50%;">

Disconnect gas lines by pushing down on quick connect tab while pulling up on gas tubing. Remove the retainer knobs for the API spray insert and heater assembly and the 4 socket head screws that mount the spray insert and heater assembly to the housing. 

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_3.jpg" style="width:50%;">

Remove the 3 socket head screws and the side panel on the right side of the housing. 

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_4.jpg" style="width:50%;">

Remove the 4 socket head screws and metal plate covering the APCI corona discharge needle high-voltage connection.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_5.jpg" style="width:50%;">

Remove the 2 screws and the plastic mount housing the high-voltage corona discharge needle connector and adjacent grounding connection. The right-side panel can be replaced.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_6.jpg" style="width:50%;">

Remove the API spray insert and the 4 socket head screws and the heater assembly cover.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_7.jpg" style="width:50%;">

Remove 3 socket head screws holding on the heater assembly and carefully pull the heater assembly away from the mounting body while feeding wire.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_8.jpg" style="width:50%;">

Carefully slide the positioning plates up and over the heater assembly and electrical connections to separate them from the electronic components

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_9.jpg" style="width:50%;">

Loosen and remove the 4 nuts retaining the 10-pin Harting connector to the front plate and unscrew the transparent square nut connecting the HV wire to the HV plug on the front plate.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Disassembly_10.jpg" style="width:50%;">

Separate the connector from the front plate.

### Soldering the Electronics

Add the nuts from the original Harting connector to the new one and mount the new connector to the front plate. Thread a 3/8-32 panel nut onto the HV plug to clamp it to the front plate and tighten it to prevent the HV plug from turning freely in the front plate. 

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_1.jpg" style="width:50%;">

Cut a 10 cm section of HV wire and strip 1 cm from each end. Cut a second 60 cm section and strip 1 cm from one end. Solder the 22 MOhm resistor between the two sections of HV wire. Cut a 6 cm section of 1/4”- polypropylene tubing and slide it over the resistor. 

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_2.jpg" style="width:50%;">

Add heat shrink over the tubing. Add a short section of heat shrink to each end of the previous heat shrink to prevent the tube from sliding. Feed the long end of the HV cable through the port in the top of the 3D-printed electronics enclosure and carefully fold the resistor in.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_3.jpg" style="width:50%;">

Cut the plastic insulation off one end of a butt splice crimp connector using wire cutters.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_4.jpg" style="width:50%;">

Slide the 3D-printed HV connector onto the short end of the HV wire with the threaded end facing out. Feed the short end of the HV wire into the uncut end of the crimp connector and crimp. Slide the cut end of the crimp connector over the gold-plated solder well on the inside end of the HV plug mounted to the front plate. It should slide on easily but make firm contact.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_5.jpg" style="width:50%;">

Heat shrink a 2.15 kOhm resistor, leaving the last 5 mm of each lead exposed. Strip 5 mm from each end of a 4 cm section of wire to make a jumper. Place the resistor between pins 6 and 10 in the Harting connector and place the wire jumper between pins 4 and 9. Tighten the set screws fix the connections.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_6.jpg" style="width:50%;">

Thread the 3D-printed HV female connector onto the inside end of the HV plug and tighten to secure the crimped HV line to the HV plug. Carefully fold the HV cable into the 3D-printed electronics enclosure and mount the front plate to the electronics enclosure using the 2 of the original flush head mounting screws.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Soldering_7.jpg" style="width:50%;">

### Assembling the Shaft Assembly

Cut the 1/4-40 lead screw to a length of approximately 9 cm using whatever cutting tool you have on hand. The threads on the cut end do not need to be preserved. Modify the lead screw nut so it fits into the shaft with the two mounting holes lining up with the corresponding threaded holes on the shaft. The nut is made of acetal/POM, so it is easily shaped with common tools (files, hacksaw, dremel, etc.)

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_1.PNG" style="width:50%;">

Thread the uncut end of the lead screw into the lead screw nut from the bottom until approximately 29 mm protrudes from the top of the nut. Mount the lead screw nut in the 3D-printed shaft using two 6-32 screws.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_2.jpg" style="width:50%;">

Slide the shaft up through bottom of shaft guide by lining up the grooves in the shaft with the guide pins on the inside of the guide shaft. All 3D printers print slightly differently, so tolerances may need to be adjusted in the original design files. Variable sets have been included in each design file to simplify adjustments of critical dimensions. If the shaft does not slide smoothly in the shaft guide, you may need to increase the bore diameter of the shaft guide by editing the “Bore_diameter” variable in the FreeCAD [file](https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/FreeCAD/Shaft_guide.FCStd) for the shaft guide. If the shaft is too loose in the shaft guide, decrease the bore diameter. If the shaft slides smoothly in the shaft guide but cannot pass the guide pins, you may need to increase the pin-to-pin distance (“Pin_to_pin_distance” variable in the FreeCAD file for the shaft guide) or decrease the pin radius (“Pin_radius” variable). If the shaft has rotational play, you may have to decrease the pin-to-pin distance or increase the pin radius.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_3.jpg" style="width:50%;">

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Shaft_guide_bore-drawing.png" style="width:50%;">

Push brass flanged sleeve bearing into the hole in the 3D-printed cap and press the M3 threaded insert into the side mounting hole from the inside.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_4.jpg" style="width:50%;">

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_5.jpg" style="width:50%;">

Slide shaft collar over the top end of the lead screw and tighten the set screw 13 mm below the top.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_6.jpg" style="width:50%;">

Guide lead screw up though the brass bushing in the cap. Slide the thumb knob onto the lead screw. While pushing the thumb knob against the shaft collar, tighten the set screw on the thumb knob to fix it to the lead screw. Turn the thumb knob clockwise while lining up the grooves on the shaft with the ridges on the inside of the cap until the cap slides over the shaft.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_7.jpg" style="width:50%;">

Thread M3 set screw into threaded insert on back side of cap, but don’t tighten it all the way. Feed the free end of the HV wire coming from the electrical enclosure through the hole in the top of the cap and down through the shaft. Do the same with one end of the PEEK line.

### Assembling the High-Voltage Termination

Disassemble a Bic Round Stic® pen and flush the polypropylene ink cartridge tube out with methanol to remove all the ink. Cut a 60 mm section of the pen tubing. Strip 70 mm of insulation off terminus of HV wire. Slide a 60 mm section of heat shrink onto the stripped portion of the wire and heat.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_8.jpg" style="width:50%;">

Slide the plastic pen tube over the heat-shrinked portion of the wire all the way to the terminus of the insulation and solder the HV pogo pin onto the terminus of the wire.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_9.jpg" style="width:50%;">

Slide the plastic tube down onto the splines of the pogo pin and heat shrink where the plastic tube meets the HV wire insulation.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_10.jpg" style="width:50%;">

### Installing the Strip Mount

(procedure is the same whether using the commercial paper strips or paper strips produced in-house).

Feed PEEK tubing and the HV terminus through the holes on the top surface of the cap and down through the shaft.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_11.jpg" style="width:50%;">

Slide a 10-32 threaded (male) 1/16-inch nut onto the end of the PEEK line. Slide a 10-32 to 1/4-28 adapter onto peak line and begin to thread the 1/16-inch nut into the adapter. Position the bottom of adapter 32 mm from terminus of PEEK line and tighten connection to clamp the PEEK fittings in place on the PEEK tubing.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_12.jpg" style="width:50%;">

Feed the PEEK terminus into the threaded hole in the 3D-printed strip mount, and the HV terminus into the unthreaded hole. Thread in the 1/4-28 PEEK adapter while ensuring the PEEK tubing is rotating freely within the shaft assembly. Thread the 4-40 set screw into the threaded hole on the side of the strip mount but don’t fully tighten.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_13.jpg" style="width:50%;">

Insert a paper strip holder into the strip mount and ensure it is fully seated. If the paper strip holder does not slide in easily, you will need to increase the vertical tolerance by decreasing the “Strip_Height” variable in the FreeCAD [file](https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/FreeCAD/Opensource_strip-holder.FCStd) for the strip holder (if using opensource paper strips), or by increasing the “Strip_pocket_height” variable in the FreeCAD [file](https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/FreeCAD/Commercial_strip-mount.FCStd) for the strip mount (if using commercial paper strips). If the paper strip holder is loose in the strip mount, you will need to decrease tolerances. Slide the high voltage terminus into the strip mount until it contacts the rivet/screw on the paper strip assembly (look down along top of paper strip to ensure). Push it an additional mm to ensure good contact between pogo pin and rivet/screw, but not so far that the pogo pin is fully depressed. Tighten set screw on the side of the strip mount to fix the height of the high voltage contact.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_14.jpg" style="width:50%;">

Turn the PEEK adapter nut clockwise until the PEEK terminus is roughly 1 mm above the surface of the paper strip (make sure the PEEK is turning freely within the shaft assembly so as not to introduce torsion in the PEEK tubing). The following image shows a strip mount with properly adjusted high voltage contact and solvent line.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_15.jpg" style="width:50%;">

Line up locking lugs on insert with slots on the shaft, slide insert into shaft while twisting clockwise until insert clicks into place. Pull extra slack in high voltage line up through the cap.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_16.jpg" style="width:50%;">

### Installing Assembly in the ESI Housing

Pass the electrical enclosure assembly and PEEK tubing up through the bottom of the positioning plates.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_17.jpg" style="width:50%;">

Slide the positioning plates over the shaft assembly and seat them on the shaft guide.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_18.jpg" style="width:50%;">

Mount the positioning plates and shaft assembly to the ESI housing and replace the 4 mounting screws. Replace the left thumbscrew only, to allow easier access to the loading port in the shaft guide when loading and unloading strips.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Assembly_19.jpg" style="width:50%;">

## Opensource Strip Construction

### Cutting Paper Strips

If you choose to make your own paper strips, you will need to have a method of cutting the strips out of the chromatography paper. Paper strips can be cut by hand using a razor blade, by custom die cutters, or by a laser cutter. Whichever technique is chosen, it is crucial that the tip of the paper is cut to a fine point without any fraying otherwise you may experience unstable spray. If using a laser cutter, we recommend rinsing the strips in deionized water prior to use to remove pyrolysis products generated from the heat of the laser. We have included an [.svg](https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/SVG/Paper_strip.svg) file for laser cutting. Laser settings must be optimized for your specific laser cutter.

### Printing Strip Holders and Strip Holder Clips

The FreeCAD [file](https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/FreeCAD/Opensource_strip-holder.FCStd) for the strip holder contains the strip holder clip as well. Print the strip holders and the strip holder clips standing vertically with the back surfaces on the build plate. Support should not be necessary, as the overhangs are minimal. 

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Strip-holder_sliced.JPG" style="width:50%;">

Print the strip tray laying flat. Support is recommended for the overhangs.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Strip-tray_sliced.JPG" style="width:50%;">

### Assembling Strips

Place a paper strip in a 3D-printed strip holder with the holes in the paper strip and strip holder aligned.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Strip_1.png" style="width:50%;">

Thread a 2/56 socket cap screw into the hole in the strip holder and tighten until the paper strip is clamped flat against the strip holder.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Strip_2.png" style="width:50%;">

Slide a 3D-printed strip holder clip over the end of the paper strip and onto the strip holder until it clicks. Be careful not to damage the tip of the paper. The paper should be laying flat in the strip holder. You may need to modify tolerances in the FreeCAD [file](https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/FreeCAD/Opensource_strip-holder.FCStd) for the strip holder clip and/or strip holder to ensure a snug fit.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Strip_3.png" style="width:50%;">

Put each assembled strip into a 3D-printed strip tray for storage until use. 

## Operating Instructions

The following instructions assume familiarity with instrument software and general instrument use. Refer to your instrument user manual for more specific instructions.

### Positioning Calibration Procedure

-	Turn off the heat to the ion transfer tube / inlet and allow it to fully cool.
-	Loosen the 3 socket head screws and remove the left side panel from the source. Using your fingers, push the view port plug out of the source housing from the inside. 
<p align="center">
    <img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Positioning_1.jpg" style="width:50%;">
</p>

-	With source removed from the instrument and the shaft at the bottom of its travel, insert a distance calibration strip and slide the shaft assembly to the back of its travel.
-	Mount the source to the instrument. 
-	While looking through the side view port, slide the shaft assembly forward until the calibration strip is close to the inlet. Adjust the vertical positioning of the calibration strip by turning the thumb knob on the shaft assembly until the center of the calibration strip is aligned with the inlet. When the desired height is reached, tighten the set screw on the backside of the cap.
<p align="center">
    <img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Positioning_2.jpg" style="width:50%;">
</p>

-   To calibrate the gap between the inlet and paper strips, slide the shaft assembly forward until the calibration strip touches the inlet. It is crucial that the inlet is cool for this step, or the calibration strip may melt onto the ion transfer tube and contaminate the instrument. Tighten the black retainer knob on the source housing to clamp the shaft assembly in position.
-	Remove the source from the instrument and remove the calibration strip from the strip mount. The viewport plug and side panel can be replaced.

### Spray Solvent Delivery Set Up

The free end of the PEEK tubing can be terminated with a Luer-Lok adapter and connected to a 10 mL glass syringe filled with the desired spray solvent. We recommend priming the solvent delivery line before mounting the first strip to be run to remove air from the solvent line. 
Using a syringe pump connected to the instrument allows solvent delivery to be programmed into the instrument method along with voltage and scan parameters.

### Method Development

The source should be recognized by the instrument as an ESI source. Develop the instrument method as a direct infusion ESI method. If the source is not recognized, check the resistance across pins 6 and 10 on the Harting connector. You may need to replace the resistor if resistance is greater or less than 2.15 kΩ.

Spray solvent should be selected based on the matrix that your sample is in and the analytes of interest. Refer to the literature for examples of spray solvent composition for different applications.

Program solvent delivery to start at the beginning of the method before voltage turns on to give the analytes time to dissolve into the solvent and the solvent time to wick to the tip of the paper. It takes approximately 80 µL of spray solvent to wet a paper strip, so the solvent flow rate will determine the amount of time needed to pre-wet the paper. Exact solvent flow rates and deposition volumes can be altered to optimize sensitivity and achieve stable spray for the desired method duration. The amount of solvent on the paper can affect the spray mode, which in turn affects ionization and transmission efficiency.

Program the voltage to come on once the paper strip is wet. We recommend optimizing spray voltage for the spray solvent, sample matrix, and analytes you are interested in, but 3600 – 4000 V are typical for paper spray methods in positive mode. Negative-mode paper spray requires lower spray voltages to prevent corona discharge and charring of the paper. The duration of high voltage depends on the desired length of the method. Paper spray methods can range from a few seconds to several minutes.

Program data acquisition to continue for several seconds after the voltage turns off so the signal returns to baseline at the end of the method. This will simplify peak integration during data processing.

### Sample Preparation

A diverse variety of sample types are amenable to paper spray mass spectrometry including but not limited to biofluids, water samples, health supplements, pharmaceuticals, forensic residues, and tissue homogenates. In most cases, little to no sample preparation is required and samples can be directly deposited on the paper strips without prior filtration or extraction steps. A sample deposition volume of 10 µL is standard, but lower volumes are sometimes used for complex sample matrices. 

Samples should be allowed to dry on the paper, either at ambient conditions or with the help of a drying oven or desiccator prior to analysis. 

### Loading and Analyzing a Paper Strip

To load a paper strip, raise the shaft to its upward position by pulling upwards on the cap. The shaft and cap rotate 90° clockwise in the shaft guide to allow strips to be loaded from the cutout in the right side of the shaft guide.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Loaded_strip.jpg" style="width:50%;">

Ensure the strip is properly seated in the strip mount and slide the shaft to the bottom of its travel. The bottom of the cap should be flush with the top of the shaft guide.

The strip is now loaded, and you can run the instrument method. You should get a sharp increase in signal when the voltage turns on and a sharp decrease in signal when the voltage turns off.

<img src="https://github.com/Lucas-Abruzzi/AperiSpray/blob/main/Media/Chronogram.JPG" style="width:50%;">

### Trouble Shooting

If the signal doesn’t come on, there is either a problem with the electrical contact, the solvent delivery, or the positioning of the strip. Try the following steps in order:

-	With the voltage turned off, raise the shaft to the upward position and visually inspect the paper strip for solvent. It should be saturated with solvent but not overflowing or forming a drop at the tip. If there is no solvent, prime your syringe pump to remove air and check your instrument method to confirm it is programmed correctly to deliver solvent. You may need to increase the solvent delivery rate / duration.
-	If the paper looks saturated with solvent and there is still no signal, try moving the shaft assembly forward to decrease the inlet gap.
-	If there is still no signal, remove the source from the instrument and use a multimeter to confirm continuity between the pogo pin and the HV plug. There should be approximately 22 MΩ of resistance. If there is no continuity, remove the electronics enclosure and determine where the connection is broken.
-	If the HV line has appropriate resistance, check your instrument method to confirm the voltage and scan parameters are correctly programmed.
-	If the signal onset is delayed or choppy, try increasing the voltage onset delay or move the shaft assembly forward or back.

### Unloading Used Paper Strips

To unload a strip, raise the shaft to the upward position and use gloved fingers or forceps to extract the used paper strip. Used strips can be discarded.

If there is solvent in the strip well on the strip mount, lower the solvent deposition volume for subsequent runs to prevent carryover.