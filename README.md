# IIITB ASIC COURSE
# Table of Contents
- [DAY-0 - Tools Installation](#day-0---tools-installation)
- [DAY-1-Introduction to Verilog RTL Design and Synthesis](#day-1-introduction-to-verilog-rtl-design-and-synthesis)
- [DAY-2-Timing Libs Hierarchical vs flat synthesis and efficient flop coding styles](#day-2-timing-libs-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-styles)
- [DAY-3 - Combinational and Sequential Optimizations](#day-3---combinational-and-sequential-optimizations)
- [DAY-4 - GLS, Blocking vs Non Blocking and Synthesis Simulation mismatch](#day-4---gls-blocking-vs-non-blocking-and-synthesis-simulation-mismatch)
- [DAY-5 - If,case,for loop and generate](#day-5--if-case-for-loop-and-generate)
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
<details>
 <summary>
  OpenLane Installation
 </summary>


_Steps to Install OpenLane_

```

 $ sudo apt-get update
 $ sudo apt-get upgrade
 $ sudo apt install -y build-essential python3 python3-venv python3-pip make git

 $ sudo apt install apt-transport-https ca-certificates curl software-properties-common
 $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

 $ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu (lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

 $ sudo apt update

 $ sudo apt install docker-ce docker-ce-cli containerd.io

 $ sudo docker run hello-world

 $ sudo groupadd docker
 $ sudo usermod -aG docker $USER
 $ sudo reboot 

 # After reboot
 $ docker run hello-world

 # Check dependencies 
   git --version
   docker --version
   python3 --version
   python3 -m pip --version
   make --version
   python3 -m venv -h

 # Below steps installs PDKs and Tools
  $ cd $HOME
  $ git clone https://github.com/The-OpenROAD-Project/OpenLane
  $ cd OpenLane
  $ make
  $ make test

```

<img width="789" alt="Screenshot 2023-08-13 121625" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ba348b32-c8e6-4ec5-b079-3252dbfeac13">


<img width="573" alt="Screenshot 2023-08-13 121801" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/6f0b1e69-d619-4bf9-bd80-d69fd832dbca">


<img width="936" alt="Screenshot 2023-08-13 121901" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/5edac02a-c470-452a-a7f4-a1c20f712cf2">

 
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




## DAY-2-Timing Libs Hierarchical vs flat synthesis and efficient flop coding styles


<details>

<summary>
   SKY130RTL D2SK1 - Introduction to timing.libs
 </summary>


## SKY130RTL D2SK1 - L1 - Introduction to .lib -1

The .lib file is opened in vim to understand its contents in depth. 
TITLE : Explanding the title of the lib file: 30nm tech, typical out of fast,slow and medium at 25 degree celsius of temperature. Thus the title explains "process", "voltage" and "temperature". These create variations in the design.


<img width="503" alt="Screenshot 2023-08-10 172234" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/d8684758-584c-4c21-9842-e7dd78a2407c">


<img width="504" alt="Screenshot 2023-08-10 172546" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/0efe6f92-c363-49da-8394-a073b3994f5e">




## SKY130RTL D2SK1 - L2 - Introduction to .lib -2

Futhermore, it tells about the technology(here,cmos) , delay models(LUTs), units(nsecs,Volts,nW,mA,kohms for the respective parameters), operating conditions(P,V,T).


<img width="346" alt="Screenshot 2023-08-10 172640" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/bc138827-d07c-4712-95a8-a7fe442521b7">



Moving on, the standard cells, specified by the keyword "cell" are visible. Gates are present as standard cells.


<img width="386" alt="Screenshot 2023-08-10 172725" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/835c2f6a-ba4b-45ab-b218-9b8d112c4bc2">


Each cell consists of details such as leakage power, number of inputs and function performed on the inputs and so on. The verilog model of each of these gates can be found by specifying the name of the cell along with the path of the verilog files. 
Also, we can find out power and timing information of each of the input.

The verilog file of the corresponding standard cell can be found in the verilog_model under the my_lib file. It can be accessed with the command shown in the image below:

<img width="810" alt="Screenshot 2023-08-10 173352" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/7ea6b692-25d4-4cde-9b20-dfaf2907ff71">




## SKY130RTL D2SK1 - L3 - Introduction to .lib-3

Elaborating the same with the use of a 2 input and gate. On comparing different types of and gate cells: wider cells consume more power and less delay as mentioned earlier.


<img width="357" alt="Screenshot 2023-08-10 182820" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/af86d53b-6cb1-4b3f-9be1-b285dbefdf2e">




<img width="532" alt="Screenshot 2023-08-10 182737" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/cbd7c0a2-0b71-4b53-a03a-007b9dece648">



</details>

<details>

<summary>
   SKY130RTL D2SK2 - Hierarchical versus Flat synthesis
 </summary>


## SKY130RTL D2SK12 - L1 - Hierarchical and Flat Synthesis - 1

First enter into the path where verilog_files are located and enter into the mutiple_modules file in the editor.


<img width="646" alt="Screenshot 2023-08-10 195302" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/05f300b6-14c4-460a-ae31-77752359a8f6">


Execute the following commands:

```
 
 $ yosys
 $ read_liberty -lib /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ read_verilog multiple_modules.v
 $ synth -top multiple_modules
 # title of the module is given in the synth command
 $ abc -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ show
 # throws an error
 $ show multiple_modules
 # displays on dot viewer
 $ write_verilog -noattr multiple_modules_hier.v
 $ !vim multiple_modules_hier.v
 $ flatten
 # to not have multiple models hierarchically
 $ write_verilog -noattr multiple_modules_flat.v
 $ !vim multiple_modules_flat.v


```

In heirarchial, it is observed that the implemetation is done through nand gates, while design did not have a nand gate implementation. This is done because in Cmos implementation or stacking PMOS for generating OR gate which is a bad idea as PMOS mobility is low and wider cells are required; whereas NMOS stacking doesnt create these problems and can generate NAND logic, hence it is preffered by the synthesis tool. 


<img width="302" alt="Screenshot 2023-08-10 201000" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/e6602bcb-184f-411a-8216-e3f4ef3049b0">



## SKY130RTL D2SK12 - L2 - Hierarchical and Flat Synthesis - 2

Similarly following commands for flatten, there is no longer a hierarchial instantiation.


![WhatsApp Image 2023-08-10 at 21 19 18 (1)](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/a30541df-e922-4923-8773-d3c42af72e35)

<img width="417" alt="Screenshot 2023-08-10 205354" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/e03f98a4-f22e-4240-908d-f05d5d6a28f0">

<img width="460" alt="Screenshot 2023-08-10 211305" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/d861bae5-e254-4c35-bd04-d2fe18bce1a0">




Further, on following the above commands to synthesize only the first sub module, we obtain the netlist as follows:

<img width="305" alt="Screenshot 2023-08-10 212516" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/da3ef19e-00c2-4cae-8486-22e2a7b8c2b8">


This is useful so as to not synthesize multiple instantiations of the same function, but synthesize once and replicate n times. In large designs the netlists are split to ensure optimal synthesis and the all are integrated together.
$synth -top module_name.v

</details>


<details>

<summary>
   SKY130RTL D2SK3 - Various Flop Coding Styles and optimization
 </summary>


## SKY130RTL D2SK3 - L1 - Why flops and Flop coding styles-1

We need flip flops for combinational circuits as well because propagation delays of the gates may cause glitch; flip flops (D) restrict glitches beacause the output changes only at clock edge. Thus the output will be stable even if input is glitching i.e output shielded from input glitch. To control the data into and out of FF, there are reset(sync and async) and set.


## SKY130RTL D2SK3 - L2 - Why flops and Flop coding styles-2

Verilog codes of synchronous and asynchronous reset for D flip flops are discussed.



## SKY130RTL D2SK3 - L3 - Lab flop synthesis simulations-1

Simulating the verilog codes of async and sync set and reset and checking their outputs and verifying the same.


<img width="960" alt="Screenshot 2023-08-10 231636" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/384c629f-d93f-4005-82f5-a78fc13f0172">

<img width="782" alt="Screenshot 2023-08-10 232433" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/cf936de4-3eba-4a54-9a36-12cf4a73401d">



## SKY130RTL D2SK3 - L4 - Lab flop synthesis simulations-2

To synthesize the file, run the following commands in yosys:

```

  $ yosys
  $ read_liberty -lib /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
  $ read_verilog dff_asyncres.v
  $ synth -top dff_asynres
  $ dfflibmap -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
  #The above keyword dfflibmap is to read flipflop from .lib file
  $ abc -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
  $ show


```


<img width="635" alt="Screenshot 2023-08-10 233244" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/743d539a-c240-4b98-8539-0527717af975">


Follow similar commands to sythesize all the variations of reset and set.



## SKY130RTL D2SK3 - L5- Interesting Optimizations-1

Through multiper circuits, it is obsereved that there is no use of memory in the design and hence is optimized.
It is obsereved that the multiplication of a number by 2 involves left shifting its contents and appending a zero at the end. Hence by using this simple logic, the use of standard cells and be avoided.


<img width="270" alt="Screenshot 2023-08-13 112736" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/443949fa-5fa5-4f8e-a313-dec915e8fdb7">




## SKY130RTL D2SK3 - L6- Interesting Optimizations-2

Similarly, optimization of multiplication of a 3-bit number by 9 generates a 6-bit number that involves multiplication of the number by 8 which shifts the bits left by 3 units and then appending 3 right most bits with zeros; then adding the original 3 bit number. This is the design without the use of any standard cells. As demonstrated above, the multiplication does not require any memory.

```
 $ module mult8 (input [2:0] a , output [5:0] y);
   	 assign y = a * 9;
   endmodule

```
</details>

## DAY-3 - Combinational and Sequential Optimizations

<details>
 <summary>
SKY130RTL D3SK1 - Introduction to Optimizations
 </summary>

 ## SKY130RTL D3SK1 L1 Introduction to Optimizations-1

 ***Optimizations*** : The action of making the best or most effective use of a situation or resource. Here, it is essentially minimizing the logic so as to get the best savings in terms of area and power. 
It can be of the following types:

1. Constant Propagation
2. Boolean Logic Optimization


**Constant Propagation** :  In the example, if A=0, the whole logic will only be transformed into an inverter. The implementation will now have 2 transistors instead of 6 transistors.

**Boolean Logic Optimization** : Consider the boolean expression:
```
 $ assign y = a?(b?c:(c?a:0)):(!c)

```
This design generates 3 muxes internally. To optimize it, simplify the boolean expression generated from the 3 muxes as shown

```
 ~a~c + a(bc + ~bac)
 ~a~c + ac
 !(a^c)

```

Thus there is a K-Map reduction happening here.


 ## SKY130RTL D3SK1 L2 Introduction to Optimizations-2

 ***Sequential Logic Optimization*** : 2 types :
 1. Basic: Sequential Constant Propagation
 2. Advanced : a) State Optimization
               b) Retiming
               c) Sequential Logic Cloning (Floor Plan Aware Synthesis)



**Sequential Constant** : Consider the 2 example circuits given below:
The first example says that no matetr reset in ON or OFF, Q value is always 0 and is constant. 
In the second example, Q will not be equal to set value always; because after set=0, Q waits until the next clock cycle to check for the value of D. 
Hence, in the second example Q is not a sequential constant.

![WhatsApp Image 2023-08-13 at 12 29 57](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/fd761ffc-0bb6-4694-98ce-da0c07c18808)


 ## SKY130RTL D3SK1 L3 Introduction to Optimizations-3

***State Optimization*** : Optimization of unused states.
***Sequential Logic Cloning*** : This is done mainly on routing level of abstraction, when the physical design is aware. In the floorplan, to minimize routing delays, 2 copies of a logic block are created so that further circuits can gain easy access and computation is faster. 

![WhatsApp Image 2023-08-13 at 12 47 29](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/232322c2-a26b-4de3-b401-f8ef2d4a33db)


***Retiming*** : Retiming is a technique for optimizing sequential circuits. It repositions the registers in a circuit leaving the combinational portion of circuitry untouched. Consider the example circuit below, which ensures higher speed of operation by simply shifting parts of logic from ckt A to B. 


![WhatsApp Image 2023-08-13 at 12 47 40](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/90f467da-c4a4-4e0d-b590-42f47cc99e05)


</details>



<details>
 <summary>
SKY130RTL D3SK2 - Combinational Logic Optimizations
 </summary>

 ## SKY130RTL D3SK2 L1 Combinational Logic Optimizations-1

_STEPS_

Check the following files and their expected optimizations are listed below:
opt_check : And gate instead of a 2x1 mux.
opt_check2 : Or gate instead of a 2x1 mux. (Through de-morgan's law) 

Synthesize these files and check for schematics:

```
 $ cd /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files/
 $ yosys
 $ read_liberty -lib /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ read_verilog opt_check.v
 $ synth -top opt_check
 $ opt_clean -purge # perfroms optimizations
 $ abc -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ show

```
Check the following files and their expected optimizations are listed below:
opt_check : And gate instead of a 2x1 mux.
opt_check2 : Or gate instead of a 2x1 mux. (Through de-morgan's law) 


Results of synthesis: 
Optimizations have been done as required. 

<img width="305" alt="Screenshot 2023-08-13 125957" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/6f482e25-80c9-454d-806d-e1f9dda42546">

 
<img width="305" alt="Screenshot 2023-08-13 130035" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/7fa8f710-e1ea-4baf-aa7d-f35ed4bd6b12">


Follow similar process for checking optimization of opt_check2 file to obtain similar results. 






 ## SKY130RTL D3SK2 L1 Combinational Logic Optimizations-2

 Moving ahead with opt_check3 file. , expecting the optimized output to be a 3 input and gate.
 
 <img width="303" alt="Screenshot 2023-08-13 131019" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/852d6025-e6f3-4825-8880-a0e087dcff70">

 Expecting the optimized output to be a 2 input XNOR gate for opt_check4.v file.
 
<img width="307" alt="Screenshot 2023-08-13 131651" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ab04b05b-c182-4bdd-9606-f78ac7f5197e">

For the file multiple_module_opt.v, the optimized expression is y=ab+c, which requires a gate which ands 2 inputs and performs an or operation of it with another variable doe by gate "a21o".
Here, the synthesis result is also flattened else only the top submodule is synthesized.

<img width="305" alt="Screenshot 2023-08-13 132409" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/d35bb10a-ce4d-41d1-b036-3a6b0407c1a8">

</details>


<details>
 <summary>
SKY130RTL D3SK3 - Sequential Logic Optimizations
 </summary>

 ## SKY130RTL D3SK3 L1 Sequential Logic Optimizations-1

Optimizing and checking the results of all the files in the image below:

<img width="584" alt="Screenshot 2023-08-13 132909" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/2eb67c63-e73e-478a-b6ab-52f98397599e">

Files and their expected optimizations:

***dff_const1***  : There is no sequential constant here, thus flip flop will be a part of the design.

<img width="960" alt="Screenshot 2023-08-13 133405" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/7997f43d-dcf2-41ee-8560-89eb025d536e">

_STEPS_

```
 $ read_liberty -lib /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ read_verilog dff_const1.v
 $ synth -top dff_const1
 $ dfflibmap -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 # it is used to map sequential ckts to their appropriate library, so that tehre is no mismatch
 $ opt_clean -purge # perfroms optimizations
 $ abc -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ show

```
A flip flop is inferred in the design:

<img width="314" alt="Screenshot 2023-08-13 134324" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/390d7576-d180-4d9e-9a77-3f2caed12b93">



<img width="303" alt="Screenshot 2023-08-13 133908" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/0d41c7ba-def2-4809-b61d-d8965712044e">


 ## SKY130RTL D3SK3 L2 Sequential Logic Optimizations-2


***dff_const2***: Here, a sequential constant exists, this flip flop is not a part of the design anymore.

<img width="309" alt="Screenshot 2023-08-13 134136" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/612a83aa-d9bd-441a-94d0-daec5aa632b3">


***dff_const3***: 2 flipflops are present, but no flip flop can be optimized, hence both exist. 

<img width="306" alt="Screenshot 2023-08-13 142340" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/1d982203-da99-46e9-a38b-89c6e6e72747">


 ## SKY130RTL D3SK3 L3 Sequential Logic Optimizations-3

***dff_const4***:  2 flipflops are present, but both flip flops can be optimized, hence both cease to exist. 


<img width="303" alt="Screenshot 2023-08-13 135037" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/98224a86-952d-4131-9c6e-a77a32fbc718">




***dff_const5***: 2 flipflops are present, but no flip flop can be optimized, hence both exist. 



<img width="302" alt="Screenshot 2023-08-13 135333" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ca954e14-7810-43af-8c0c-74dad3a1fbd8">



</details>



<details>
 <summary>
SKY130RTL D3SK4 - Sequential Logic Optimizations for unused outputs
 </summary>


 ## SKY130RTL D3SK4 L1 Sequential Optimizations unused outputs-1 

 Looking into the 3 bit upcounter design, counter_opt.v. The output of the counter that is viewed is count[0], which is only 1 bit in the 3 bit counter output, hence the synthesis tool generates only 1 flip flop. 
 

<img width="439" alt="Screenshot 2023-08-13 180051" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/fc7421bd-df9c-4e2b-96d1-d3ea591f6a5b">

 

<img width="289" alt="Screenshot 2023-08-13 174040" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/87cf84be-c943-4d36-b87b-96b002fe5956">


<img width="1383" alt="Screenshot 2023-08-13 at 5 43 52 PM" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/7b1e943b-2a4a-44c3-be78-6fef8e32b589">



 ## SKY130RTL D3SK4 L1 Sequential Optimizations unused outputs-2

 Looking into the 3 bit upcounter design, counter_opt2.v. The output of the counter that is viewed is count[2:0],all 3 bits counter output, hence the synthesis tool generates all 3 flip flop. Also, since there is a lot of combinational logic being generated here, it is worthy to observe that in the previous example, they didnt exist only because the other 2 flipflops were not needed and hence all the combinational logic feeding their inputs were also optimized. 

 
 <img width="463" alt="Screenshot 2023-08-13 180129" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/856c54c7-5c19-4b8d-9b81-d6779dee1066">


<img width="354" alt="Screenshot 2023-08-13 175246" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/8c41195a-79ae-4b14-b966-661162ee6361">


 ![WhatsApp Image 2023-08-13 at 17 56 49](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/cbd50477-f07e-4382-a1cf-79e674d2ca71)

</details>


## DAY-4 - GLS Blocking vs Non Blocking and Synthesis Simulation mismatch

<details>

<summary>
   SKY130RTL D4SK1 - GLS, Synthesis Simulation match and Blocking vs Non Blocking statements
 </summary>

## SKY130RTL D4SK1 - GLS concepts and flow using verilog

***GLS*** : Gate level simulation. Here, the netlist is run along with the testbench as DUT. Essentially, netlist is same as logical code. This is needed to verify the logical correctness of design after synthesis and to ensure that the timing of the design is met. RTL does not have a notion of time but the design has to meet the specifications and timing limits as well.


![WhatsApp Image 2023-08-13 at 23 08 05](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/910b2191-b1e6-444b-a90c-ff234b5134fc)


Gate level models can be : 1)Functionally aware 2) Timing aware. The functionality needs to be tested for any kind of mismatch.


## SKY130RTL D4SK2 - Synthesis and Simulation Mismatch

As addressed above mismatches exist between simulation and synthesis .
This mismatch can occur because of the following factors:

***1) Missing Sensitivity list*** : Simulators are change sensitive, only changes in the inputs trigger outputs. Thus, they sense 'activity'.  In the RTL design it is of utmost importance to trigger the assignments appropriately.
***2) Blocking vs Non blocking***
***3) Non standard verilog coding***


## SKY130RTL D4SK3 - Blocking and Non Blocking assignments.

_Blocking statements_ : It is a sequential execution, one after the other. 
_Non Blocking_ : Parallel execution

Blocking statemts if not written accurately cause extensive problems in the design and functionality can be lost as well. This problem more specifically arises in sequential circuits.



## SKY130RTL D4SK4 - Caveats with Blocking Statements.

Consider this code given below:

![WhatsApp Image 2023-08-14 at 00 34 09](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/b7ccb655-75d0-4997-8dd9-f9d2d7a734ba)


The old value of q0 is used for simulation and thus the output will be faulty. Instead, the order of statements inside the always block can be interchanged to ensure latest value of q0 to be used for simulation and hence calculation of y. Note that in both designs generate the same circuit.


</details>

<details>

<summary>
   SKY130RTL D4SK2 - Labs on  GLS, Synthesis Simulation mismatch
 </summary>


## SKY130RTL D4SK2 L1 - Labs on  GLS, Synthesis Simulation mismatch-1

Consider the GLS simulation for the following design 

<img width="593" alt="Screenshot 2023-08-14 004434" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ec4e2569-4c96-4526-9543-807f050c4916">

RTL output:

<img width="504" alt="Screenshot 2023-08-14 004708" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/10564d33-d203-4c46-8dde-08f5edc31d13">\

Synthesis ouput:
A mux is generated by the design


<img width="304" alt="Screenshot 2023-08-14 005012" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/9b1a644e-9cd8-4caf-9d06-4e457f6416c8">


 ```
 $ yosys
 $ read_liberty -lib /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ read_verilog ternary_operator_mux.v
 $ synth -top ternary_operator_mux
 $ write_verilog ternary_operator_mux_net.v
 $ abc -liberty /home/sush/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
 $ show
 # exit yosys
 # the below commands are for gls synthesis
 $  iverilog ../my_lib/verilog_model/primitives.v  ../my_lib/verilog_model/sky130_fd_sc_hd.v ternary_operator_mux_net.v        tb_ternary_operator_mux.v
 # reads the primitives and the netlist i.e a separate file that reads all the standard cell modules
 $ ./a/out
 $ gtkwave tb_ternary_operator_mux.vcd

```
The GLS simulation design while viewing on gtkwave has the netlist markers under uut. 
<img width="505" alt="Screenshot 2023-08-14 005929" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ca2a8f9e-a621-4d1e-8c5d-2f4abf65a56a">


## SKY130RTL D4SK2 L2 - Labs on  GLS, Synthesis Simulation mismatch-2

Considering a bad mux design where the always block is triggered when select line changes (somewhat like that of a flip flop) and simulating its RTL design, it is seen that changes of the input arent sensed if there is no change in select, thus giving an erroneous output.


<img width="507" alt="Screenshot 2023-08-14 010500" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/13f67115-64ce-4f28-8f70-cedd055ff141">


Following the above commands to generate its GLS design:
Here, the output is sensitive to the changes in inputs as per changes with the slect line as well.


<img width="508" alt="Screenshot 2023-08-14 011222" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/10137491-093d-46b1-8020-f1eeec5c72f7">

</details>


<details>

<summary>
   SKY130RTL D4SK3 - Labs on Synthesis mismatch for Blocking statement
 </summary>

## SKY130RTL D4SK3 L1 - Lab Synth Sim mismatch for Blocking statement-1


Considering file blocking caveat.v, the circuit generates an or and an and gate. It is written in a blocking statement, so the output y will use old value of the output of OR gate as its input hence computing the wrong value.


RTL simulation results: Error in logic designed. 

<img width="505" alt="Screenshot 2023-08-14 012427" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/e7594b43-2786-449a-81c5-6b53256b612a">

## SKY130RTL D4SK3 L2 - Lab Synth Sim mismatch for Blocking statement-2

GLS Synthesis results: 

<img width="960" alt="image" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/9b3e7ff2-4dda-45fd-97a1-1ef1ac9a3020">


The error is gone! The blocking caveat creates an illusion that a flipflip exists, but as a matter of fact, no flop exists in the netlist.

Thus synth-sim mismatch exist and must be taken extra care of. 


</details>




## DAY-5 -If case for loop and generate

<details>

<summary>
   SKY130RTL D5SK1 - If case constructs
 </summary>

## SKY130RTL D5SK1 L1 If Case constructs - 1

***IF*** If statements are used to construct priority logic. There can be if else or if and a series of else if statements. The hardware of this if statement is a MUX.

Both if and case staements are present inside an always block on a reg type variable.

_Infered Latch_ : This ia a downside of writing improper or poor if statements. If an if statement doesnt have an else, it stores the previous value of output because if condition is also false and there is no more option to check, hence a latch is generated in the hardware. The intention was not to create a latch, the circuit is now converted to a sequential kind.


## SKY130RTL D5SK1 L2 If Case constructs - 2

In a counter, an always block is always a part of the design, so there exists a latch generation in the hardware, irrespective of whether an incomplete if statement is present.

***Case Statement*** : Used when multiple variations of an expression need to be checked. So if 4 case staements are present, it means a 4x1 MUX is generated on the hardware front.

Caveats:
1) Incomplete case statements: Suppose all the variations of case statements are not taken care of and no default statement exists again _Latch up_ occurs. Thus default statement is very important and essential.


## SKY130RTL D5SK1 L3 If Case constructs - 3

_Caveats Contd_:

2) Partial assignments in case: Consider the following RTL design

```
 module mux(x,y,sel,a,b,c,d);
 input a,b,c,d;
 input reg [1:0] sel;
 output reg x, y;
 always @ (*)
 begin
      case(sel)
           2'b00 : begin
                   x=a;
                   y=b;
             end
           2'b01 : begin
                   x=a;
             end
           default: begin
                    x=a;
                    y=b;
              end
 endcase
 endmodule

```

Here 2 MUXes(one for each output: x and y), each 4x1(select line is 2 bit, meaning 4 cases) are genrated. But when sel is 01, the output y is not assigned any value causing the generation of a hardware latch. Thus all outputs must be assigned values in all segments of case. 

3) Overlap in Case: In if else statements only 1 statement will be executed and the remaining will not be checked when 1 of them becomes true in the sequential order. If a bad case statement is written all conditions are checked even if some statement has already matched, so if there are overlaps, unpredictable outputs arise. 


</details>

<details>

<summary>
   SKY130RTL D5SK2 - Labs on Incomplete if case
 </summary>

## SKY130RTL D5SK2 L1 Incomplete if - 1

First checking the incomplete if statement that is generating a latch. 
Simulate the RTL design and check results on GTK wave.


<img width="506" alt="Screenshot 2023-08-14 215400" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ed7f3965-3c81-4d20-aa6e-0c7fe291f88c">


Synthesis results: 

<img width="314" alt="Screenshot 2023-08-14 215518" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/8442376c-48d7-470c-99fe-46047f206712">

<img width="303" alt="Screenshot 2023-08-14 215544" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/d7f5e1d3-ac78-4be9-8816-2ce6bd3999e8">


## SKY130RTL D5SK2 L1 Incomplete if - 2

Consider the verilog code, incomp_if2. Its RTL design is expected to generate the following circuit:

![WhatsApp Image 2023-08-14 at 22 01 14](https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/44847dbe-21ca-4df8-b5c3-3130c321dcc1)


<img width="960" alt="Screenshot 2023-08-14 220542" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/bec2c143-c3c1-421e-97e0-dfd22db1d513">



Synthesis Result:


<img width="307" alt="Screenshot 2023-08-14 220629" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/56f39f18-ca4c-4bce-88e5-239f693cc484">


<img width="301" alt="Screenshot 2023-08-14 220645" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/5cab9b28-6456-4376-99c2-30923dfa0c51">


</details>

<details>

<summary>
   SKY130RTL D5SK3 - Labs on Incomplete Overlapping case
 </summary>

##   SKY130RTL D5SK3 - Lab Incomplete Overlapping case - 1 

Consider the example verilog file comp_case. 

<img width="673" alt="Screenshot 2023-08-14 221640" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/6e3a32f5-1d89-4999-826c-822015ccca84">


RTL simulation is incomplete: for sel = 2'b11, it displays value of the default statement, i.e output follows i2.

<img width="506" alt="Screenshot 2023-08-14 221339" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/73011d8e-e525-4173-80fa-38fdd1d540a5">

Synthesis results:

  <img width="333" alt="Screenshot 2023-08-14 221921" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/fdcad66d-5448-4ca9-87d5-e033a33ce086">

<img width="303" alt="Screenshot 2023-08-14 221937" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/c3b6095c-4975-4925-bf63-4b672c96f6e7">


##   SKY130RTL D5SK3 - Lab Incomplete Overlapping case - 2

The verilog design partial_case_assign ha a prtial assignement as discussed above.There should be a latch in the path of X as it has an incomplete assignment.


<img width="800" alt="Screenshot 2023-08-14 222700" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/d4ddd5b9-b8a4-4617-8f44-c57ee2716cd1">


##   SKY130RTL D5SK3 - Lab Incomplete Overlapping case - 3

Simulation Results:

<img width="301" alt="Screenshot 2023-08-14 223127" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/31aec2fb-664d-47f4-b691-df423cab48c1">

<img width="304" alt="Screenshot 2023-08-14 223149" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/6835bd5e-97fb-498f-bcae-73ba76fa9e9a">

Consider the verilog code bad_case:
Here, i3 is at output even if case condition is 10 because of bad style of design. The simulator will be confused and the output cannot be predicted, it is at the mercy of the simulator.

<img width="688" alt="Screenshot 2023-08-14 223457" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/974b07f9-576b-4350-b08d-b7d6a2484374">


##   SKY130RTL D5SK3 - Lab Incomplete Overlapping case - 4


Simulation result: GLS Synthesis shows that unpredictabilty exits in the netlist design. There is no latch generated for this circuit as expected.

<img width="333" alt="Screenshot 2023-08-14 223800" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/34711d34-4ba3-4e00-807b-51673aaeb0ca">


<img width="960" alt="Screenshot 2023-08-14 224238" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/87c715b8-4633-48f2-b21e-013a3b27c558">


</details>

<details>

<summary>
   SKY130RTL D5SK4 - For Loop and Generate
 </summary>

##   SKY130RTL D5SK4 - For Loop and Generate - 1

***Looping Constructs*** 
1) For Loop: Used inside an always block. To evaluate an expression 'n' number of times.
2) Generate : It is a generate loop followed by a for loop.Outside an always loop. Used to instantiate hardware 'n' number of times.

##   SKY130RTL D5SK4 - For Loop and Generate - 2


Different examples of writing good verilog designs are written using blocking statements, where for construct comes very handy to reduce a number of lines of coding.

For-generate on the other hand is used for (instantiating) replicating hardware.

```
genvar i;
generate
for (i=0 ; i<8; i = i+1) begin
  #instantiate a function of choice
end
endgenerate

```

Thus there will be 8 instances of the function called. 


##   SKY130RTL D5SK4 - For Loop and Generate - 3

In the design of a ripple carry adder, if it is required to have an N-bit adder, there is a need to replicate the hardware of a FA N times. 
Simliar to for-generate, if-generate also exists.

</details>


<details>
 
<summary>
 SKY130RTL D5SK5 - Labs on For Loop and For Generate
</summary>


##  SKY130RTL D5SK5 - Labs on For Loop and For Generate - 1

Using the following design for simulation.

```
 module mux_generate (input i0 , input i1, input i2 , input i3 , input [1:0] sel  , output reg y);
 wire [3:0] i_int;
 assign i_int = {i3,i2,i1,i0};
 integer k;
always @ (*)
begin
 for(k = 0; k < 4; k=k+1) begin
        if(k == sel)
                y = i_int[k];
 end
 end
 endmodule

```

This is a 4x1 Mux design using for loop. 
RTL Simulation shows that it behaves perfectly like a mux as is required.

Check the synthesis simulation result:
GLS synthesis also gives correct output and it matches with RTL synthesis.

<img width="959" alt="Screenshot 2023-08-14 233701" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/06f4b59f-535b-4335-996b-8e9c46df5ebc">

##  SKY130RTL D5SK5 - Labs on For Loop and For Generate - 2

Next, consider, demux written using for loop.

Synthesis and RTL simulation is a match.

<img width="872" alt="Screenshot 2023-08-14 234453" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/7ff32d0a-bd98-4ee2-b05d-ab80cf01c12b">

<img width="960" alt="Screenshot 2023-08-14 234833" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/86ef01a3-5e4e-4c2d-975b-658867a0c354">


##  SKY130RTL D5SK5 - Labs on For Loop and For Generate - 3

Consider the Ripple carry adder module, written using generate loop, which instantiates the Full Adder module n times.

<img width="730" alt="Screenshot 2023-08-14 235251" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/f4e589f6-5cdf-419e-af83-6ff2b0117a95">


##  SKY130RTL D5SK5 - Labs on For Loop and For Generate - 4


Checking the RTL Simulation and the GLS Synthsis simulation and verifying that they are the same.


<img width="700" alt="Screenshot 2023-08-14 235917" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/ed9d99dc-6c5d-457c-9f27-b30c9c0ae62f">

<img width="960" alt="Screenshot 2023-08-15 000255" src="https://github.com/Sushma-Ravindra/IIITB-ASIC-1/assets/141133883/0177fa62-15d3-4feb-b989-6eec5b7e4042">

The addition is still being performed with accuracy.





## Contributors
SUSHMA R


## Acknowledgements 
www.vsdiat.com

www.github/kunal123.com

www.google.com

www.chipedge.com/everything-you-need-to-know-about-synthesis-in-vlsi/

www.electronicsforyou.com

www.github/OpenRoad.com


