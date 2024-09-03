# NASSCOM_VSD_SOC.DESIGN
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

2. Pads Pads are the contact points on the chip where electrical connections are made. In the QFN-48 package, these pads are located on the bottom and connect the chip to the printed circuit board (PCB), ensuring electrical connectivity and mechanical stability.

3. Core The core is the central part of the chip where the main functional blocks are located, including logic gates, memory cells, and other essential components.

4. Die The die is the small block of semiconductor material on which the integrated circuit is fabricated. It is the actual piece of silicon that contains the electronic circuits and is mounted on the lead frame within the QFN-48 package.

5. IPs (Intellectual Properties) IPs are pre-designed and pre-verified blocks of logic or functions that can be integrated into the chip. These include processors, memory controllers, communication interfaces, and other functional blocks, helping to reduce design time and improve reliability.

Advantages of QFN-48 Package
Compact Size: Saves space on the PCB.
Thermal Performance: Efficient heat dissipation due to the exposed pad.
Electrical Performance: Low inductance and resistance.
Reliability: Leadless design reduces the risk of bent leads.







