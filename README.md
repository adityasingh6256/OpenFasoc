# OpenFasoc
Fully-Autonomous SoC Synthesis using Customizable Cell-Based Synthesizable Analog Circuits.
The SoC synthesis tool realizes analog circuits, including PLLs, power management, ADCs, and sensor interfaces by recasting them as structures composed largely of digital components while maintaining analog performance. 
OpenFASOC is focused on open-source automate analog generation from user specification to GDSII with fully open-sourced tools. This project is led by a team of researchers at the University of Michigan is inspired from FASoC whcih sits on proprietary tools. (See more about FaSoC at website)
#Installation   

## Openfasoc   
The command used to install OpenFASOC are    
```
git clone https://github.com/idea-fasoc/openfasoc

cd openfasoc

pip install -r requirements.txt
```   
## Prerequisites   

 ### 1.OpenROAD   
The commands to install OpenROAD are,
```
git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD.git

cd OpenROAD

./etc/DependencyInstaller.sh

./etc/DependencyInstaller.sh -run

./etc/DependencyInstaller.sh -dev

mkdir build

cd build

sudo cmake ..

sudo make
```    
 ### 2. Open_PDKs   
 
 we need sky130A files   
 
 download from http://opencircuitdesign.com/open_pdks/archive/open_pdks-1.0.354.tgz    
 
 or git clone https://github.com/RTimothyEdwards/open_pdks    
 
 or git clone git://opencircuitdesign.com/open_pdks   
 ```   
 ./configure --enable-sky130-pdk
sudo make
sudo make install   
```   
you may need some prerequisites for this clone them from opencircuitdesign.com/open_pdks     

 ### 3. Klayout
 we need laytest version.
Downlaod the latest version of the Klayout from [here](https://www.klayout.de/build.html). Install the following dependencies: qt5-default, qttools5-dev, libqt5xmlpatterns5-dev, qtmultimedia5-dev, libqt5multimediawidgets5 and libqt5svg5-dev.   
```
sudo apt-get install -y libqt5widgets5

sudo dpkg -i klayout_0.27.11-1_amd64.deb

````    
### 4. Netgen  
download http://opencircuitdesign.com/netgen/archive/netgen-1.5.241.tgz   
commands for installation   
```   
./configure
make
make install   
```   
### 5. magic   
download from http://opencircuitdesign.com/magic/archive/magic-8.3.335.tgz 
```  
./configure
make
make install   
```   
### 6. yosys   
The software used to run gate level synthesis. Yosys is a framework for Verilog RTL synthesis.
To install yosys, install the prerequisites using the following command 
 ```
 sudo apt-get install build-essential clang bison flex \
	libreadline-dev gawk tcl-dev libffi-dev git \
	graphviz xdot pkg-config python3 libboost-system-dev \
	libboost-python-dev libboost-filesystem-dev zlib1g-dev
```
To install latest Version of Yosys, 
```
git clone https://github.com/YosysHQ/yosys.git

make

sudo make install 

make test

```   


