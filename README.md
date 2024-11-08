# CMOS Bidirectional Counter
This project involves the pre-layout simulation of a bidirectional counter implemented using CMOS technology, along with an analysis of its associated parameters.
# Contents
 * Overview of CMOS Bidirectional Counter IP
 * Block diagram of CMOS Bidirectional Counter IP
 * Circuit diagram of CMOS Bidirectional Counter IP
 * Specifications
 * Perfomance Parameters
 * Open Source Tools used
 * Installation in Ubuntu
     * eSim Installation
     * Ngspice Installation
     * SkyWater PDK Installation
 * Installation in Windows
     * eSim Installation
 * Pre Layout Schematic and Simulations
 * Contributors
 * Acknoledgements
 * Contact Inormation
   
# Overview of CMOS Bidirectional Counter IP
    
  This project presents the implementation of a CMOS-based bidirectional counter, a crucial component in digital electronics for applications requiring counting in both increasing and decreasing 
directions. By leveraging complementary metal-oxidesemiconductor (CMOS) technology, the design achieves low power consumption and high noise immunity, making it suitable for portable and battery-operated devices. 
The bidirectional counter operates by utilizing control signals to determine the counting direction, 
enhancing flexibility in digital systems. Key advantages include reduced chip area, improved speed due to parallel processing capabilities, and robustness against 
temperature variations. The project highlights the potential of CMOS technology in advancing digital 
counting mechanisms.
[Leveraging CMOS for Advanced Bidirectional Counter Designs.pdf](https://github.com/user-attachments/files/17679646/Leveraging.CMOS.for.Advanced.Bidirectional.Counter.Designs.pdf)
 

# Block diagram of CMOS Bidirectional Counter IP
![Block diagram of bidirectional counter](https://github.com/user-attachments/assets/861b7d9d-4fb3-424c-92db-4d2ea6a981c9)

# Circuit diagram of CMOS Bidirectional Counter IP
![1_pages-to-jpg-0001](https://github.com/user-attachments/assets/744635a7-c302-48d1-84d0-f4ea30df6d02)

# Specifications
CMOS (Complementary Metal-Oxide-Semiconductor) technology is widely used in modern digital and analog circuits, with process nodes ranging from 180nm to 7nm. It operates with supply voltages between 1.0V and 5.0V, depending on the process, and supports switching frequencies up to several GHz. CMOS circuits offer low static power consumption, with dynamic power consumption depending on the switching frequency. Key electrical characteristics include propagation delays between 1ns and 10ns, and threshold voltages typically between 0.3V and 0.7V. CMOS is used in applications such as logic gates, processors, and mixed-signal circuits.

A Bidirectional Counter is a digital counter capable of incrementing and decrementing based on a control signal, commonly used in digital systems like clocks, position tracking, and frequency division. Bidirectional counters typically operate with clock frequencies ranging from 1Hz to several MHz, depending on the design. They are usually powered by 3.3V or 5V, with a range of 1-bit to 32-bit (or more) widths. Performance characteristics of bidirectional counters include propagation delays from 5ns to 200ns, depending on the bit width and clock frequency. These counters are often used in timekeeping, digital signal processing, and position encoding applications.
# Perfomance Parameters

| **Parameter**               | **Description**                                                | **Min**  | **Actual** | **Max**  | **Unit** | **Condition**             |
|-----------------------------|----------------------------------------------------------------|---------|------------|----------|----------|---------------------------|
| **Supply Voltage (Vdd)**     | The voltage required for operation                             | 1.0     | 3.3        | 5.0      | V        | Typical CMOS process      |
| **Input Voltage (Vin)**      | The voltage levels required for input signals                 | 0       | Vdd/2      | Vdd      | V        | CMOS logic gates          |
| **Leakage Current (I_leak)** | The current that flows through transistors when off            | 1nA     | 10nA       | 100nA    | A        | Static (no switching)     |
| **Static Power Consumption** | Power consumed when the circuit is not switching              | 1uW     | 10uW       | 100uW    | W        | Static operation          |
| **Dynamic Power Consumption**| Power consumed during switching activity                      | 10uW    | 100uW      | 1mW      | W        | Switching operation       |
| **Switching Frequency (f_max)** | Maximum frequency for stable operation                      | 100MHz  | 1GHz       | 3GHz     | Hz       | Process-dependent         |
| **Propagation Delay (t_pd)** | Time for signal to propagate through a gate                   | 1ns     | 10ns       | 50ns     | s        | Typical gate delay        |
| **Power Supply Rejection Ratio (PSRR)** | The ability to reject noise on the supply line         | 40dB    | 60dB       | 80dB     | dB       | For analog circuits       |
| **Threshold Voltage (Vth)**  | The voltage at which the transistor switches                  | 0.3V    | 0.7V       | 1.0V     | V        | CMOS logic gates          |

---

## Bidirectional Counter Performance Parameters

| **Parameter**               | **Description**                                                | **Min**  | **Actual** | **Max**  | **Unit** | **Condition**             |
|-----------------------------|----------------------------------------------------------------|---------|------------|----------|----------|---------------------------|
| **Clock Frequency (f_clk)**  | The frequency at which the counter is clocked                  | 1Hz     | 1MHz       | 100MHz   | Hz       | Counter operation         |
| **Counting Range**           | The number of unique states the counter can count              | 0       | 2^N-1      | 2^N-1    | -        | N-bit counter             |
| **Max Count Time (t_max)**   | Time to reach maximum count                                    | -       | 1µs        | 1ms      | s        | For N-bit counter         |
| **Resolution**               | The smallest increment of the counter                         | 1       | 1          | 1        | -        | Binary counting           |
| **Input Frequency (f_in)**   | Frequency of the input signal for bidirectional count         | 1Hz     | 1kHz       | 10MHz    | Hz       | For bidirectional control |
| **Propagation Delay (t_pd)** | Time for the counter output to change after input             | 10ns    | 50ns       | 200ns    | s        | For binary counter        |
| **Power Consumption (P)**    | Power consumed by the counter                                  | 1mW     | 10mW       | 100mW    | W        | Static and dynamic modes  |
| **Clock to Q Delay (t_cc)**  | Time for the counter output to reflect clock signal           | 5ns     | 20ns       | 100ns    | ns       | For digital counters      |
| **Setup Time (t_setup)**     | Minimum time for stable input before clock edge                | 2ns     | 10ns       | 20ns     | ns       | Counter setup condition   |
| **Hold Time (t_hold)**       | Minimum time after clock edge for stable input                 | 1ns     | 5ns        | 15ns     | ns       | Counter hold condition    |

---

# Open Source Tools Used

    1.  eSim installation in Ubuntu OS (LINUX)
   
    2.  eSim installation in Microsoft Windows OS



# Installation in Ubuntu
    
   	i.      After downloading eSim, extract it using: 
  
   		       * unzip eSim-2.4.zip

   	ii.     Now change directories in to the top-level eSim directory (where this INSTALL file can be found).

   	iii.    To install eSim and other dependencies, run the following command :

   		       * chmod +x install-eSim.sh
   		       * ./install-eSim.sh --install

   	iv.     To uninstall eSim and all of its components, run the following command :

   		       * ./install-eSim.sh --uninstall


   How to Run eSim
   =================
   
    A.  Through Terminal
   		
   		   * esim

    B.  Double click eSim desktop icon



# Installation in Windows

    i.      Download eSim for Windows OS from "https://esim.fossee.in/". Disable the antivirus (if any).

    ii.     If MinGW and/or MSYS is already installed in your machine, then remove it from the
            PATH environment variable as it may interfere with eSim and might not work as intended.

    iii.    Now double click on eSim installer and then follow the instruction to install eSim.

    iv.     After the installation is completed, please download and add the following file to the esim home directory(FOSSEE\eSim\ folder):
            https://github.com/FOSSEE/eSim/blob/master/src/frontEnd/TerminalUi.ui#L6

    v.      Please download and add the following executable to the nghdl folder(FOSSEE\eSim\nghdl\src location):
            https://drive.google.com/file/d/17MNCCq9cG6A7fnIH-4KMUMY-yb4rW9s4/view?usp=sharing

    vi.     Hence the installation is completed.

    vii.    To uninstall eSim and all of its components, run the uninstaller "uninst-eSim.exe" located at 
            top-level eSim directory (where this INSTALL file can be found).



Note
======
Please report any eSim installation related issue/error at "https://forums.fossee.in/"

# Overview of CMOS Bidirectional Counter IP

# Contributors
 * Dhayanesh G
   
 * Kunal Ghosh
   
 * Pankaj Agrawal

# Acknowledgments

* Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
  
* Ankur Sah, M.Tech Embedded Systems, NIT Jamshedpur

# Contact Information

* Dhayanesh G, Undergraduate Student, Rajalakshmi Engineering College 230801045@rajalakshmi.edu.in

* Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com

* Pankaj Agrawal, Postgraduate Student, International Institute of Information Technology, Bangalore 1811pankajagrawal@gmail.com
