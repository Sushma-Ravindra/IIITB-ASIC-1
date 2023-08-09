# IIITB ASIC COURSE
# Table of Contents
- [Day-0 - Tools Installation](#day-0---tools-installation)
   - [Yosys Installation](#yosys-installation)
- [Day-1](#day-1)
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








