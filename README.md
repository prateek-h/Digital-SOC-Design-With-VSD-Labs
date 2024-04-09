# Digital-SOC-Design-With-VSD-Labs
The NASSCOM-VSD SoC Design Program aimed to provide training and certification in Digital SoC Design.Digital System-on-Chip (SOC) design is a fundamental aspect of modern electronics engineering, facilitating the integration of various digital components onto a single chip.
### Benefits
1.Crafting and characterizing standard cells.

2.Gaining practical experience in the Physical Design domain.

3.Generating a complete GDSII from an RTL netlist.

4.Diving into and enriching the open-source EDA landscape.

CREATING NEW VIRTUAL MACHINE:
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/d5d70668-1679-43c2-8c3d-82cffa880bff)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/0f11ff9d-fd02-4a01-88ac-97b7ba0d4f4b)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/cb6a2e20-17e4-48d3-9654-2d9b923e5467)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/066680b4-7162-4821-b276-e9ecf1819ed5)
# DAY 1: S1 Inception of open source EDA Openlane and Sky130 PDK
Introduction to QFN-48 Package,chips,core,die and IPs
Pads are components that allow us to transmit a signal inside the chip, Core is the location of all fixed logic gates presentand Die is the entire chip's size.
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/8f6b8c7d-2d2a-4bcc-b7ef-6ef2cee61f8c)
## RISC-V
RISC-V is an open standard instruction set architecture (ISA) based on established reduced instruction set computer (RISC) principles. Unlike most other ISA designs, RISC-V is provided under royalty-free open-source licenses. Many companies are offering or have announced RISC-V hardware open source operating systems with RISC-V support are available, and the instruction set is supported in several popular software toolchains.
## Process of Software application to hardware
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/340d6abc-9f7f-40af-a221-c7570de109aa)
The above image shows how the process converting a program that is needed to be run is carried out
1)The 'C' language program is converted to a Instruction set by the OS in a .exe file .

2)The assembler present in the system only understands the instruction language.

3)The assembler then converts this instruction set to binary code as the hardware only has binary inputs to function.

## Introduction to all components of open source ASIC design
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/e1f19fac-55ba-4e87-8782-61fc0fe5177c)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/6c032240-1663-4caf-9166-e5c24298cc22)
The above image shows that how an open sorce ASIC is ready to use by having all the required enablers RTL, PDK data adn EDA Tools
## RTL2GDS FLOW
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/45bae11f-eb99-4097-87e7-70b7399e2b84)
The above image shows the simplified version of RTL2GDS flow
## Getting familiar to EDA tools
Design prearation steps

![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/f921141c-1d47-4e0c-8567-fcc0279a99f6)
#Running synthesis
`run_synthesis`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/5f5bcfd7-4b06-407d-b2d5-24f1a72c3f1b)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/926330c0-4e5a-4579-b6d2-aef423822062)
#Calculating flip-flop ratio
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/03c396d5-9e5f-4457-81e5-9c669b5ea3dc)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/da7cd1d4-a77e-45a5-a074-7599cef2f157)


Flip-flop ratio = total number of Dflip-flops divided by total number of cells.

Percentage = Flip flop ratio * 100

Ratio=1613 / 14876

Ratio = 10.84296854%.
## DAY 2: Good floorplan vs Bad floorplan and introduction to library cells
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/e92b9276-2b3d-44ac-92ec-d5b735e367e1)

#Utilization and Aspect Ratio
Utilization Ratio is the ratio of the total cell area to the core area.
Utilization Factor is the ratio of area occupied by Netlist to the total area of core.
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/c617ce5a-bd1a-4230-b45a-c549e87c311f)

Aspect Ratio is the ratio of height and width of the core.
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/90e0bebb-97f8-4a46-88b0-73c7e0c68dfe)

#How are Pre-placed cells located in the core.
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/377af797-608e-40fb-af62-77d4328fbc98)

Also some of the IP's which are only used once in the chip instead of using them over and over such as Memory, Clock, Comparator, MUX,etc .

#Power planning
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/6e0e2b5b-b0ed-47f1-9d00-bf2eb058a9eb)
Here's how power planning is done in a chip. It is in a grid like fashion so that where ever a logic cell or a functional cell is placed it becomes easier for the block to reach the Vss and Vdd.
Also a Die is present around the core where the Pins are placed according to the blocks inside the core.

#Running Floorplan
`run_floorplan`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/4ed32967-f06a-4b9c-aa27-901132a8249f)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/66bb3267-bca3-44bc-8aac-7349cd43e209)

#Visual Representation of Floorplan
For viewing the floorplan we need to run
`  magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged_unpadded.lef def read picorv32a.floorplan.def & `
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/b7000295-8e2a-403c-bf3e-8ae35dc88829)
![magic floorplan](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/ab18b6a1-1805-4040-97c1-f9fafe797c6a)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/8c24e1d3-b67c-4249-8bcf-93b456354b76)

#Run Placment
`run_placement`
Above is used to run placement tools on the given design and floorplan
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/71edfeeb-0f4a-41e6-ac95-77c2f7610e0e)
![placement cell](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/f4edfb5e-b0c1-451c-b0ed-a4c1f41006fd)

#Flow of designing a Circuit
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/0d9ba321-11e4-4b65-bf17-1c1b96647121)

#Flow of designing a Layout
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/94775558-611b-4843-8bb3-5b4366e2c16c)

# DAY 3: Design library cell using Magic Layout and ngspice characterization.
#Cloning inverter from github repository
`git clone https://github.com/nickson-jose/vsdstdcelldesign.git`
For viewing the .mag file we use the code same as before
`magic -d XR -T "/libs/sky130A.tech" mag sky130_inv.mag`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/37ee4008-01d9-4a82-b288-55593741cda9)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/b5795c4e-2c58-48bd-8b8d-a4dc710d1717)

#pmos
![pmos layout](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/44eec786-e662-47c0-9f08-3529c6cdfd50)

#nmos
![nmos in layout](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/cb234c84-d797-43cf-8704-e6903f0c0d80)

![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/c51d1050-f109-46c4-aa68-30e92dedd689)
 modifying the above file
 `
  option scale=0.01u 
include ./libs/pshort.lib
include ./libs/nshort.lib
//. subckt sky130_inv A Y VPWR VGND
M1000 Y A VPWR VPWR pshort_model. 0w=37 l=23
+ ad=1443 pd=152 as=1517 ps=156
M1001 Y A VGND VGND nshort_model. 0 w=34 l=23
+ ad=1435 pd=152 as=1365
ps=148̦
VDD VPWR 0 3.3V
VSS VGND
0 OV
Va A VGND PULSE(OV 3.3V 0 0.1ns 0.1ns 2ns 4ns)
CO A Y 0.0754fF
C1 Y VPWR 0.117fF
C2 A VPWR 0.0774fF
C3 Y VGND 0.279fF
C4 A VGND 0.45fF
// C5 VPWR VGND 0.781f
//. ends 
.tran 1n 20n
.control run
endc
end`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/57a87d9d-75fd-439f-9934-f3b81ffff4c9)

#spice 
`ngspice sky130_inv.spice`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/3b4fe12f-0773-441a-b068-135df38f60c1)
Also for plotting graph using command
`plot y vs time a`
![y vs time a](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/699ea2be-1362-4e91-a7fe-f5d2457f3290)
where value of c3 = 2fF

1) Rise time = 0.459ns
2) Fall time = 0.04ns
3) Cell rise delay = 0.06ns
4) Cell Fall Delay =0.028ns

## DRC Corrections and rules
We need files for DRC corrections. It is downloaded using below command
`wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz`
also the file is extracted using 
`tar xfz drc_tests.tgz`
all the files are listed using
`ls -all`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/79540fbd-b0ce-48f0-87a8-5fd7b5c75ff1)

## Lab introduction to Magic and steps to load Sky130 tech-rules
The command `magic -d XR` was used to open the magic tool
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/dd969bfb-b7fa-4e87-bba4-1af3a2bf544d)
The Rule were found here
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/0c810f17-4e06-46c0-a879-3c6f554fb2b6)
After loading met3.mag using magic
![m3mag](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/a739ed88-4dbd-4824-b55e-c5fc4c070ed8)

After creating a metal3 using the paints in the right side section
![m3mag metal contact](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/6967c06b-4e62-4907-bbae-a54d0fb62e52)

Now after pressing p and executing command `cif see VIA2` we get
![cifseevia2](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/0def1b0b-f6bc-4bf4-9a2f-c581c94d0415)

#LAB exercise for poly.9 error in skytech file.
loaded poly.mag file using magic.
![load sky130A](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/e56330bc-0218-482f-8d3e-8cbf3725507a)
after making changes in skytech file and opening it.
![drc check](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/9d989cf7-9a7e-4daa-87e1-f1ae1540813b)

#LAB exercise for N-well
Selecting the design in magic.
![nwell](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/ca0cbe57-b383-4a33-b86b-d883af2e80f7)
After making necessarcy changes in the skytech file 
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/28fa7ff2-71b8-4b1f-b27e-b17562aaf9f3)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/bdd5ecd3-309b-4de6-a69d-6651ebb9b929)
![dnwell_shrink](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/a8021983-15bf-4cc9-96dd-b9b707489c74)
![nwell_missing](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/c9b55fc8-d47c-428b-a9fb-816628d20681)

# DAY 4 Pre-layout timing analysis
#tracksinfo
`pdk/sky130/libs.tech /openlane/sky130_fd_sc_hd/track.info`
![tracks](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/16e41495-442d-4d3f-9b4f-cb7d32489d65)

#Lab steps to convert magic layout to std cell LEF
![ip and op on same grids](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/37d76245-048b-48a0-a9dd-1ffb309060af)
![localli A](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/d624af28-1d11-439b-8c6c-09be841e1548)

Now, we open this file in the magic by the command

`magic -T sky130A.tech sky130_vsdinv.mag &`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/64a3a842-a205-4acf-8c75-171dfa01f7dc)
modify the config.tcl file of picorv32a directory

![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/f0e12069-e373-4b7a-b2f4-8baacae2b57d)

Now Execute

![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/fc335002-b505-4aa4-9aaf-21d5f0cb6ae2)

`./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]      
add_lefs -src $lefs
run_synthesis`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/4d655f24-4262-4b2c-9883-6f3e3d0665b2)

`prep -design picorv32a -tag 01-04_12-54 -overwrite

set lefs [glob $::env(DESIGN_DIR)/src/*.lef]

add_lefs -src $lefs

echo $::env(SYNTH_STRATEGY)

set ::env(SYNTH_STRATEGY) "DELAY 3"

echo $::env(SYNTH_BUFFERING)

echo $::env(SYNTH_SIZING)

set ::env(SYNTH_SIZING) 1

echo $::env(SYNTH_DRIVING_CELL)

run_synthesis

prep -design picorv32a -tag 01-04_12-54 -overwrite`

Solving errors
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/028df899-29d3-4530-ac4e-a21cbc54d100)

![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/03e4a181-9e88-45d9-83bb-e838f7acad69)

 run the placement using command `run_placement`
 How placement looks
 ![new placemnet](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/06648ac3-025e-4ff9-bee8-4a46709c743d)
![skyvsdinv cell](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/e0e19242-f755-45dd-ae16-752e1e9bdc23)
![expanded skyvsdinv](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/3a42552d-8086-438a-bd49-2c59356c936a)

#configure OpenSTA for post-synth timing analysis
`docker
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
set ::env(SYNTH_SIZING) 1
run_synthesis`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/e4c5ac7e-eb95-4a2c-b7d0-a051c93af9c7)
Make a new pre_sta.conf file.
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/2c2d0458-faa1-49ea-939e-d3a02264b9a4)

![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/edb3fdaf-8fb0-4cc1-bae4-dde2380dd555)
Now we will create a my_base.sdc file
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/dc82a9aa-7876-4ba6-87d3-d3ebe3c28eca)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/cf47e3b2-694f-4d10-89e7-a4c726f5d781)
Now run `sta pre_sta.conf`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/4b3b5ad9-758c-47c8-891c-f42961be19c7)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/bc805112-15c3-4edd-84a2-2305ca114e32)
Change the FANOUT parameter
`prep -design picorv32a -tag 02-04_05-27 -overwrite

set lefs [glob $::env(DESIGN_DIR)/src/*.lef]

add_lefs -src $lefs

set ::env(SYNTH_SIZING) 1

set ::env(SYNTH_MAX_FANOUT) 4

echo $::env(SYNTH_DRIVING_CELL)

run_synthesis`
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/5c151be3-79ac-4367-a7e9-c4412228ce33)
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/1b329585-59b3-4314-a00f-b3084a1e40cb)

OR gate
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/8a71db7f-33b4-4928-af40-ce5d18005ed2)
`report_net -connections _11672_`   Reports all the connections
`help replace_cell` Check the command syntax
`replace_cell _14510_ sky130_fd_sc_hd__or3_4` Replace the cell
`report_checks -fields {net cap slew input_pins} -digits 4`Generate the custom timing report






 



 


