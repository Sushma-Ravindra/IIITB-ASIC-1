# IIITB ASIC COURSE
# Table of Contents
- [Day-0 - Tools Installation](#day-0---tools-installation)
- [Day-1](#day-1-introduction-to-verilog-rtl-design-and-synthesis)
- [References](#references)


## DAY-0 - Tools Installation

<details>
 <summary>
Yosys Installation
 </summary>

_Steps to install Yosys_

```
git clone https://github.com/YosysHQ/yosys.git
$ cd yosys-master   
$ sudo apt install make (If make is not installed please install it)   
$ sudo apt-get install build-essential clang bison flex \  
    libreadline-dev gawk tcl-dev libffi-dev git \  
    graphviz xdot pkg-config python3 libboost-system-dev \  
    libboost-python-dev libboost-filesystem-dev zlib1g-dev  
$ make config-gcc  
$ make   
$ sudo make install
```
Below the screenshot of successful installation of Yosys:
<img width="960" alt="Screenshot 2023-08-01 164434" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/c0dcceb9-6e75-4a9a-81b7-2b88903d5273">
</details>

<details>
 <summary>
Icarus Verilog Installation
 </summary>


_Steps to install iverilog_

```
$ sudo apt-get install iverilog
```

Below is the screenshot of sucessful installation of iverilog:


<img width="960" alt="Screenshot 2023-08-01 160329" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/a694d8c0-47f6-4d3b-ab23-93de8c2f4340">
</details>
<details>
 <summary>
GTKWAVE Installation
 </summary>

_Steps to install gtkwave_

```
$ sudo apt update
$ sudo apt install gtkwave
```
Below is the screenshot of successful installation of gtkwave:
<img width="960" alt="Screenshot 2023-08-01 161021" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/0e382340-4e0e-410a-86b5-7c883846c9b3">
</details>
<details>
 <summary>
  Open STA
 </summary> 
 
 **Commands to install OpenSTA**
 ```
 Dependencies for OpenSTA  
 sudo apt-get install cmake clang gcc tcl swig bison flex

 # Commands to Install OpenSTA
 $ git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
 $ cd OpenSTA
 $ mkdir build
 $ cd build
 $ cmake ..
 $ make
 $ sudo make install
```  
Below is the screenshot of successful installation of Open STA:
</details>

<details>
 <summary>
  MAGIC Installation
 </summary>
 
**Commands to Install MAGIC**
 
```
$   sudo apt-get install m4
$   sudo apt-get install tcsh
$   sudo apt-get install csh
$   sudo apt-get install libx11-dev
$   sudo apt-get install tcl-dev tk-dev
$   sudo apt-get install libcairo2-dev
$   sudo apt-get install mesa-common-dev libglu1-mesa-dev
$   sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```
Below is the screenshot of successful installation of MAGIC:
</details>
<details>
 <summary>
  NGSPICE Installation
 </summary>
 
**Commands to Install NGSPICE**

```
 Download the tarball from https://sourceforge.net/projects/ngspice/files/ to a local directory and then unpack it using:
 tar -zxvf ngspice-40.tar.gz

 $cd ngspice-40
 $mkdir release
 $cd release
 $../configure  --with-x --with-readline=yes --disable-debug
 $make
 $sudo make install
```


Below is the screenshot of successful installation of ngspice:

</details>

## DAY-1-Introduction to Verilog RTL Design and Synthesis
<details>
 <summary>
  SKY130RTL D1SK1 - Introduction to open-source simulator iverilog
 </summary>

### Introduction

***RTL DESIGN*** : It involves the specification of a digital circuit in terms of the flow of digital signals between hardware registers, and the logical operations performed on those signals. It is basically the implementation of specifications. RTL design lies between high-level behavioral design and low-level gate-level design. It captures the functionality of the circuit at a level where data transfers between registers are the main focus, while ignoring the specific implementation details of gates and transistors. In general,the RTL designs are described using HDLs like Verilog or VHDL. 

***SIMULATOR*** : A simulator is a device which artificially creates the effect of being in conditions of some kind. It is a tool used to check if it adheres to the designed specifications by simualating the code. It looks for changes on input signals to evaluate outputs. Here, we use iverilog tool as the simulator. 

***TESTBENCH*** : A testbench allows us to verify the functionality of a design through simulations. It is a container where the design is placed and driven with different inputs. Only the design has primary inputs and outputs, the testbench does not have them.

![WhatsApp Image 2023-08-09 at 11 39 27](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/8edd79a0-d048-4ec7-ad98-9fb99406e156)

***SIMULATOR DESIGN FLOW*** : The simulator design flow can be visualised better with the image below:

![WhatsApp Image 2023-08-09 at 11 39 16](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/d6bd4a1f-db0b-47ad-b378-168f95a7f4be)


</details>


<details>
 <summary>
   SKY130RTL D1SK2 - Labs using iverilog and gtkwave
 </summary>

 ## Introduction:

 **iverilg** : Icarus Verilog is an implementation of the Verilog hardware description language compiler that generates netlists in the desired format. It supports the 1995, 2001 and 2005 versions of the standard, portions of SystemVerilog, and some extensions.

 **GTKWAVE**: The GTKWave software is used to view simulation results when running the testbench. It is often used in conjunction with simulation tools like IVERILOG to provide a graphical representation of how signals change over time in a digital design. It gives the result in a graphic format.

 **Tools Installation**
 
_STEPS_

```
 $ mkdir VLSI
 $ cd VLSI
 $ git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git






