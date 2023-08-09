# IIITB ASIC COURSE
# Table of Contents
- [Day-0 - Tools Installation](#day-0---tools-installation)
- [DAY-1-Introduction to Verilog RTL Design and Synthesis](#day-1-introduction-to-verilog-rtl-design-and-synthesis)
- [Contributors](#contributors)
- [Acknowledgements](#acknowledgements)


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
<img width="685" alt="yosys" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/f7cd6406-65d2-4b58-888e-b20cc8af191c">

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

<img width="580" alt="iverilog" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/bc6eff91-48d0-491e-a172-fbb95aa6859a">


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
<img width="959" alt="gtkwave" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/6d3a756d-9ed8-4984-8479-63a09ee6a815">

</details>
<details>
 <summary>
  Open STA
 </summary> 
 
 _Steps to install OpenSTA_
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
<img width="600" alt="opensta" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/aa234289-e2d1-4f7e-8c45-778ecca88dc4">

</details>

<details>
 <summary>
  MAGIC Installation
 </summary>
 
_Steps to Install MAGIC_
 
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
<img width="960" alt="magic" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/c8496320-dcef-410e-a4a0-3a81ea30ef67">


</details>
<details>
 <summary>
  NGSPICE Installation
 </summary>
 
_Steps to Install NGSPICE_

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
<img width="595" alt="ngspice" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ea0ba9a9-8502-4b9b-8b00-208a3b012771">

</details>

## DAY-1-Introduction to Verilog RTL Design and Synthesis
<details>
 <summary>
  SKY130RTL D1SK1 - Introduction to open-source simulator iverilog
 </summary>

### Introduction to open source simulator

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

 ## SKY130RTL D1SK2 L1 Lab 1 Introduction to Labs

 **iverilog** : Icarus Verilog is an implementation of the Verilog hardware description language compiler that generates netlists in the desired format. It supports the 1995, 2001 and 2005 versions of the standard, portions of SystemVerilog, and some extensions.

 **GTKWAVE**: The GTKWave software is used to view simulation results when running the testbench. It is often used in conjunction with simulation tools like IVERILOG to provide a graphical representation of how signals change over time in a digital design. It gives the result in a graphic format.

 **Tools Installation**
 
_STEPS_


Clone the necessary lab files from the given github repository to a directory named VLSI.

```
 $ mkdir VLSI
 $ cd VLSI
 $ git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
 $ cd sky130RTLDesignAndSynthesisWorkshop
 # To view the verilog files and the lib files, go inside the respective directories
 $ cd verilog_files

```

<img width="870" alt="Screenshot 2023-08-09 114923" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/878d0336-d7c7-4d3b-ace6-47c3126f5d03">


## SKY130RTL D1SK2 L2 Lab 2 Introduction to iVerilog GTKWave - 1

Here, load the sample verilog design good_mux and its associates testbench onto iverilog and run it. \

```

 $ iverilog good_mux.v tb_good_mux.v
 $ ./a.out
 # output of simulator will be a vcd file, this vcd file is loaded to gtk wave for waveform visualization.
 $ gtkwave tb_good_mux.vcd

```
<img width="722" alt="Screenshot 2023-08-09 115619" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/e4ef3c1d-c6bb-43ee-9ad5-09c77dd2a817">


## SKY130RTL D1SK2 L2 Lab 2 Introduction to iVerilog GTKWave - 2

The gtkwave waveforms enable us to verify simulation results with that of our design. 

<img width="732" alt="Screenshot 2023-08-09 115543" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/0775fec5-7d24-4516-99cd-a2c4e4da04f0">

</details>


<details>
 <summary>
   SKY130RTL D1SK3  - Introduction to Yosys and Logic Synthesis
 </summary>

 ## SKY130RTL D1SK3 L1 Introduction to Logic synthesis and Yosys
 

***Yosys*** Yosys aims to converting high-level hardware descriptions into optimized gate-level representations that can be targeted for various FPGA and ASIC technologies. The flow for yosys is we feed the yosys with the design which is in RTL level and the .lib file which contain standard library cells then the yosys synthesizes and gives us the netlist file. 

Yosys uses its lib file which contains all the necessary cells and the design by the user to generate a netlist.

![yosysflow](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/281fab56-5b8b-4195-ada4-2cd3bb00bbfa)

Then,post synthesis to check whether the netlist obtained is valid or not, try matching the waveforms before and after synthesis. The same testbench that is used for the simulation can be used for the synthesized netlist as well. The netlist and testbench is fed back into iverilog to confirm synthesis results




## SKY130RTL D1SK3 L2 Introduction to logic synthesis - 1

 **Logic Synthesis** Synthesis converts a basic RTL design into a gate-level netlist that includes all of the designer’s limitations. Synthesis is carried out in several stages:

1.Converting RTL to basic logic gates.

2.Mapping those gates to actual technology-dependent logic gates accessible in technology libraries.

3.Optimising the translated netlist while maintaining the designer’s limitations.

The netlist is supposed to perform the same function as the corresponding HDL code. Synthesizer is the tool which convert RTL design into the netlist form. One of such tool used here is Yosys.

For the demonstartion, the following mux design is used further:


Design:


<img width="539" alt="Screenshot 2023-08-09 120454" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/3ff01da5-2609-45ed-8e94-20cbb0c1a143">

Testbench:


<img width="418" alt="Screenshot 2023-08-09 120649" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/95ef327a-5e33-4eed-b385-062d86af98d0">



## SKY130RTL D1SK3 L3 Introduction to logic synthesis - 2


**.lib file** : It is a collection of various logic modules. It contains all different kind of logic modules. like AND, OR, NOR etc, required for the synthesis of gates and further netlist file. It contains different variants of the same gate as well, like 2input, 3input, 4input, slow, fast, medium gates etc.

There is a need for all such variants in real life as illustrated below:
Consider the circuit shown below. So in this circuit for the clock frequency to be maximum so as to make a faster circuit the time period of the clock should be minimum. This will be taken care of parameter T_clk_q_A. Similarly, to ensure that there are no hold issues at fliflop B,Tclk_hold_B we need cells that work slowly. 


![259185703-2c9423ee-fea5-4ba2-9089-6254a9bf5b79](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/6fe92335-6b86-4694-a734-77e50f355b20)

Thus a collection of all such cells forms a .lib file. The selection of cells will be based on area, power and other such "constraints".



</details>


<details>
 <summary>
   SKY130RTL D1SK4 - Labs using Yosys and Sky130 PDKs
 </summary>


## SKY130RTL D1SK4 L1 Lab3 Yosys 1 good mux-1


_Steps to invoke Yosys_

```
 $ yosys
 $ read_liberty -lib /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ read_verilog good_mux.v
 $ synth -top good_mux
 $ abc -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ show

```

Reading .lib and mux files and synthesis command:

<img width="960" alt="Screenshot 2023-08-09 160445" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/56ee4399-7006-4dcb-a55e-35d4a0ef0114">

Generating netlist:

<img width="804" alt="Screenshot 2023-08-09 160821" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/a4d8eda5-7e35-458b-b60a-f19bce8f1e8a">

 Output of netlist generation and show command to display:
 
<img width="949" alt="Screenshot 2023-08-09 160903" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/8cf9e96b-a132-4f70-a706-2ed87de23ae7">

The synthesized design:

<img width="461" alt="Screenshot 2023-08-09 160934" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/02788215-e0ea-4f82-8cb6-d6093ecb7097">



## SKY130RTL D1SK4 L2 Lab3 Yosys 1 good mux-2

Next step is to generate the netlist file:

```
 $ write_verilog good_mux_netlist.v
 # The above command can be used to generate a netlist file. But to generate the same in a consice and readble format use the command below
 $ write_verilog -noattr good_mux_netlist.v
 $ !gvim good_mux_netlist.v

```

<img width="401" alt="Screenshot 2023-08-09 161633" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/00065056-8009-45ca-bc2d-92da4e11558b">


## SKY130RTL D1SK4 L3 Lab3 Yosys 1 good mux-3


The generated netlist file:


<img width="960" alt="Screenshot 2023-08-09 161559" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/97ba009d-d867-4d80-9981-1fd6fb035dd0">


As mentioned previously again this netlist file can be given to iverilog along wit testbench to simulate and results must match with that of simulation design.

</details>

## Contributors
SUSHMA R


## Acknowledgements 
www.vsdiat.com

www.github/kunal123.com

www.google.com

www.chipedge.com/everything-you-need-to-know-about-synthesis-in-vlsi/

www.electronicsforyou.com



