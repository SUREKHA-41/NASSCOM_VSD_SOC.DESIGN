OpenLane: Key Components in Open-Source Digital ASIC Design# NASSCOM_VSD_SOC.DESIGN
  Digital VLSI SoC Design and Planning Workshop
        Welcome to the OpenLane workshop! In this session, we will explore the journey of designing an Application Specific Integrated Circuit (ASIC) using the OpenLane ASIC flow. We’ll start from the Register Transfer Level (RTL) and work our way to generating the Graphical Data System (GDS) file. This process involves several crucial steps, beginning with an RTL file and ending with a GDS file.

 Mastering the RTL to GDS Flow:
 
 1.Acquired a thorough understanding of the entire process of converting a high-level hardware description into a physical ASIC layout. Recognized the critical importance of each step in the flow, from synthesis 
   to sign-off.
   
 2.Synthesis:Learned how RTL is transformed into a gate-level netlist using standard cell libraries. Identified the various views of cells, including Liberty, HDL, SPICE, and MAGIC Layout.
 
 3.Floor and Power Planning: Comprehended the significance of floor planning in chip partitioning and the placement of I/O pads.
 DAY 1
--> The RTL to GDSII flow in VLSI design involves transforming an RTL description of a digital circuit into a physical layout ready for fabrication. This comprehensive process includes stages such as RTL synthesis, floor planning, placement, routing, and generating the GDSII file format, which holds the layout data. Each step is meticulously carried out to ensure the final IC layout accurately represents the desired functionality and complies with fabrication requirements.
 
 ![ASIC-Design-Flow-400x400](https://github.com/user-attachments/assets/6a83406d-c216-48f7-aa6c-29cebd9a7952)
 
--> In VLSI (Very Large Scale Integration), the “Y chart” is a graphical representation that illustrates the connections between the design, fabrication, and testing processes in semiconductor manufacturing. It is called the “Y chart” because its shape resembles the letter “Y”.

![image](https://github.com/user-attachments/assets/6a5e25aa-bb67-494d-b983-addcdbce8f02)

BEGINNING OF OPEN-SOURCE EDA, OPENLANE AND SKY130 PDK
Introduction to QFN-48 Package, chip, pads, core, die and IPs
1. QFN-48 Package:
   The QFN-48 (Quad Flat No-Lead) package is a type of surface-mount technology used in electronic circuits. It features 48 pins and is known for its compact size, efficient thermal performance, and excellent electrical characteristics. Here are some key points about the QFN-48 package:
   
Compact Design: The QFN-48 package is designed to save space on the PCB, making it ideal for applications where board space is limited

Thermal Management: It offers improved thermal performance due to its exposed pad, which helps in dissipating heat more effectively

Electrical Performance: The package provides low inductance and resistance, which enhances the overall electrical performance of the device

Leadless Design: The absence of external leads reduces the risk of bent leads and improves reliability

![Screenshot 2024-09-03 201600](https://github.com/user-attachments/assets/8d31ea76-98ec-430b-814c-a4883df74149)

CHIP 
The chip, also known as the integrated circuit (IC), is the heart of the QFN-48 package. It contains the electronic circuits that perform the desired functions. The chip is typically made from silicon and is where the actual processing or control happens

![chip](https://github.com/user-attachments/assets/9a9334bf-830c-4685-96ef-ca2dacc56c22)

1.When examining the interior of the chip, all signals entering and exiting the chip are routed through the PADS. The region enclosed by these pads is known as the CORE, which houses all the digital logic of the chip. Together, the core and pads form the DIE, which is the fundamental manufacturing unit in semiconductor chip production.

![die](https://github.com/user-attachments/assets/85e1091a-fe22-4c75-acd6-323d74e9fe6c)


![ips](https://github.com/user-attachments/assets/60fb3f2d-a412-4191-81a4-dd960d94fd0b)


2. Pads Pads are the contact points on the chip where electrical connections are made. In the QFN-48 package, these pads are located on the bottom and connect the chip to the printed circuit board (PCB), ensuring electrical connectivity and mechanical stability.

3. Core The core is the central part of the chip where the main functional blocks are located, including logic gates, memory cells, and other essential components.

4. Die The die is the small block of semiconductor material on which the integrated circuit is fabricated. It is the actual piece of silicon that contains the electronic circuits and is mounted on the lead frame within the QFN-48 package.

5. IPs (Intellectual Properties) IPs are pre-designed and pre-verified blocks of logic or functions that can be integrated into the chip. These include processors, memory controllers, communication interfaces, and other functional blocks, helping to reduce design time and improve reliability.

Advantages of QFN-48 Package
Compact Size: Saves space on the PCB.
Thermal Performance: Efficient heat dissipation due to the exposed pad.
Electrical Performance: Low inductance and resistance.
Reliability: Leadless design reduces the risk of bent leads.

Introduction to RISC-V 
RISC-V (pronounced as risk five) is an open standard Instruction Set Architecture (ISA) based on Reduced Instruction Set Computing (RISC) computer architecture. Unlike proprietary ISAs, RISC-V is freely available to the public and is being used for many purposes, including designing, manufacturing, and selling customized RISC-V chips and software. This open standard approach has the potential to drive innovation and competition in the tech industry, as it allows for a greater diversity of products and solutions.

The significance of RISC-V in the context of modern computing cannot be overstated. As the tech industry is evolving, the need for efficient, scalable, and customizable computing solutions is more important than ever. RISC-V, with its simple and modular design, is well-positioned to meet these needs. Furthermore, as an open ISA, RISC-V has the potential to democratize access to high-performance computing, making it a key player in the future of the tech industry.

![risc v](https://github.com/user-attachments/assets/4b93efcf-210a-4ba4-a0cd-e10e830d4f86)


ISA (Instruction Set Architecture)

To run a C program on a specific hardware layout, such as the chip inside your laptop, a particular sequence of steps must be followed. First, the C program is compiled into its assembly language equivalent, which in this case is the RISC-V ISA (Reduced Instruction Set Computing - V Instruction Set Architecture). Next, this assembly language program is translated into machine language, consisting of binary code (0s and 1s) that the computer hardware can understand.

Following this, the RISC-V specification is implemented using RTL (Register Transfer Level), a type of Hardware Description Language. Finally, the process from RTL to the physical layout of the chip follows a standard PnR (Place and Route) or RTL to GDSII flow. 

From Software Applications to Hardware
In our daily lives, we use application software (apps) to interact with hardware. But how does this process work? Between the application software and the hardware is a layer called system software. The applications send their instructions to the system software, which then converts them into binary language, the language that hardware understands.

System software is made up of several layers:

  ![software to hardware](https://github.com/user-attachments/assets/53c05a22-6ecd-4199-a156-80081215b44b)

--> Operating System (OS): Besides managing tasks like input/output operations, memory allocation, and other low-level system functions, the OS translates application software into code written in languages like C, C++, or Java.

--> Compiler: The compiler then takes this code from the OS and converts it into an instruction set (such as .exe files). These instructions are customized for the specific hardware in use.

--> Assembler: Finally, the assembler translates these executable files into binary language, which the hardware can understand and execute to carry out the desired operation








