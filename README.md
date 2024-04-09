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

#Flow of designing circuit
![image](https://github.com/prateek-h/Digital-SOC-Design-With-VSD-Labs/assets/166489309/0d9ba321-11e4-4b65-bf17-1c1b96647121)







 



 


