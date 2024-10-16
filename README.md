# VSD SoC NASSCOM Course

This project is part of the **VSD SoC NASSCOM Course**, combining both theory and practical lab sessions for a comprehensive learning experience.

## Table of Contents
1. [Introduction](#introduction)
2. [Theory and Lab Sessions](#theory-and-lab-sessions)
3. [Conclusion](#conclusion)
4. [Contact](#contact)

---

## Introduction

The OpenLane ASIC flow is a comprehensive design process used for developing Application Specific Integrated Circuits (ASICs). This flow guides designers through multiple stages, starting with a high-level hardware description in Register Transfer Level (RTL) and ending with a Graphical Data System II (GDSII) file, which is essential for chip fabrication. Each step, from synthesis to physical layout, plays a crucial role in transforming a conceptual design into a manufacturable chip.

The process involves key stages such as synthesis, where RTL code is converted into a gate-level netlist, and physical design steps like floorplanning and power planning. The OpenLane flow integrates these stages seamlessly, ensuring that design constraints are met and that the final chip layout is optimized for performance, power, and area. Through this structured approach, designers can efficiently transition from design logic to a ready-for-fabrication layout.

---

## Theory and Lab Sessions

### Topic 1: Open-Source EDA, OpenLANE, and Sky130 PDK

---

**Theory: Understanding Chip Packaging and Wire Bonding**

In the world of embedded systems and semiconductor manufacturing, what we often refer to as a "chip" is, in reality, just the *chip package*. This package serves as a protective layer around the delicate silicon die, which contains the actual circuitry of the chip. The package plays a critical role in maintaining the integrity and performance of the chip, providing physical support, protecting it from environmental factors, and enabling the chip to be mounted onto a board.

At the heart of the package lies the actual manufactured silicon chip, which is usually connected to the external environment using a method called *wire bonding*. Wire bonding uses fine wires to create electrical connections between the chip and the package, facilitating communication with the outside world. This method has been widely used due to its reliability and cost-effectiveness in mass production.
![Image 1: QFN-48](https://github.com/user-attachments/assets/b8d4054e-4900-4838-95be-dcea01f6bc24)

![Image 2: Chip Package Illustration](https://github.com/user-attachments/assets/33d265ed-006b-4e1d-a8e5-70590d1a8d02)



---

**Theory: Core, Pads, Die, and Foundry IPs**

The chip consists of two major regions: the *core* and the *pads*. The **core** is where all the fundamental digital logic is placed. It contains combinational circuits, as well as soft and hard IPs (intellectual property blocks) that define various aspects of the chip’s functionality. Surrounding the core are the **pads**, which form the interface between the core and the external world. These IO pads include input, output, and power pads, which allow signals to flow in and out of the chip. Together, the core and pads make up the **die**, the basic manufacturing unit in the semiconductor industry.

The chip is produced in a *foundry*, a specialized facility that fabricates semiconductor devices. Foundries provide *Foundry IPs*—pre-designed blocks of logic such as SRAM, PLLs, and ADC/DACs—that can be integrated into designs. These IPs require human expertise to develop, while simpler, repeatable logic blocks known as *macros* are more standardized and reusable.

![Image 1: Chip Layout](image3_url)
![Image 2: Wafer Die and Foundry IPs](image4_url)

---

**Theory: The Role of Instruction Set Architecture (ISA) and RTL Flow**

The *Instruction Set Architecture (ISA)* is a critical layer in defining how a processor interacts with the software running on it. It forms a bridge between high-level programming languages and the hardware. For example, a C program written for a specific chip undergoes several transformations before it can be executed. First, the C program is compiled into an assembly language that adheres to the **RISC-V ISA** (Reduced Instruction Set Computing – V). This is a simplified instruction set architecture designed to make chips more efficient and flexible.

Once compiled, the assembly language program is converted into **machine code**, a binary format (0s and 1s) that the hardware can understand. At this stage, a hardware description language, such as RTL (Register Transfer Level), is used to implement the ISA’s logic. The RTL code defines how the chip will process data and perform computations. The design then goes through a series of synthesis and verification steps, ultimately generating a **netlist** (a list of logical gates and connections) that is used for physical implementation.

The final stage in this process is the **Place and Route (PnR)** flow, where the design is translated into a layout file (GDSII), which is sent to the foundry for fabrication.

![Image 1: C to Assembly to Machine Code Flow](image5_url)
![Image 2: RTL to Netlist Synthesis](image6_url)

---

**Theory: Physical Design Kit (PDK) and OpenLANE**

A *Physical Design Kit (PDK)* is an essential interface between the foundry and the IC (Integrated Circuit) design engineers. The PDK provides a collection of files, libraries, and tools that describe the manufacturing process and ensure that the design is manufacturable. The PDK contains critical elements such as **device models**, **Design Rule Checks (DRC)**, **Layout Versus Schematic (LVS)** checks, and **standard cell libraries**. These elements help ensure that the design adheres to the foundry’s rules and can be fabricated correctly.

In this course, we focus on the **SkyWater 130nm PDK**, specifically the `sky130_fd_sc_hd` library, which is a part of the Sky130 open-source PDK provided by SkyWater Technology. This PDK is designed for the **130nm technology node**, which is widely used for educational and prototyping purposes. The PDK integrates seamlessly with **OpenLANE**, an open-source EDA toolchain that covers the complete physical design flow, from RTL synthesis to final GDSII layout generation.

OpenLANE offers a set of open-source tools for each step of the design process, making it possible to take an RTL design and produce a manufacturable layout, all within an open-source framework. It democratizes chip design by allowing users to access tools and flows that were traditionally locked behind expensive commercial licenses.

![Image 1: PDK Components Overview](image7_url)
![Image 2: OpenLANE Flow with Sky130 PDK](image8_url)



---

## Contact

For support, contact us at [your-email@example.com].
