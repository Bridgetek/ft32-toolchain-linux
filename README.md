# FT9xx Toolchain

The FT9xx Toolchain is a free tool to enable code development and debug for the FT9xx series. It uses the free popular GCC compiler.
Driver support for each of the main functional units of the MCUs are also included in the installation package, provided as C code and precompiled binaries in addition to sample projects.

Install files for Debian-based Linux dirtibutions for the FT9xx Toolchain are stored as releases on this repository.

[Release Notes for the FT9xx Toolchain](Release Notes.txt).

Refer to [AN 325 FT9xx Toolchain Installation and Start Guide](https://brtchip.com/document/installation-guides/) for more information.

## Toolchain Installation

The installation package provides a simple method for automatic installation and configuration. To install the GCC compiler tools, hardware libraries, environment, and source code:
```
sudo dpkg -i ft9xxtoolchain_2.7.6_amd64.deb
```
Environment variables ```FT9XX_TOOLCHAIN``` and  ```FT9XX_COMPILER``` are created and the ```PATH``` is update to include paths to executables for the toolchain.
```
FT9XX_COMPILER=/opt/ft32
FT9XX_TOOLCHAIN=/opt/ft9xxtoolchain
PATH=...:/opt/ft32/bin:/opt/ft9xxtoolchain/programmer:/opt/ft9xxtoolchain/eclipse:/opt/ft32/bin:...
```
Additional tools provided as part of the toolchain include a one wire programmer and debugger interface, plus the ability to update firmware over DFU – the USB Device Firmware Update port.

Software Examples supplied with the installation package, may be used as reference material to develop further projects or to verify existing hardware functionality. The default location where these can be found is 
```
/var/opt/ft9xxtoolchain/2.7.6/Examples/
```
Other examples can be found [here](https://brtchip.com/software-examples/ft90x-examples/) for FT90x projects and [here](https://brtchip.com/software-examples/ft9xx-examples/) for FT9xx compatible designs.

## Eclipse IDE Installation

To install the optional Eclipse plugin for the FT9xx toolchain:
- select "Install New Software..." in an existing installation of Eclipse with C/C++ Development Tooling - [Eclipse CDT](https://projects.eclipse.org/projects/tools.cdt).
- add an "update site" as the following location:
```
/var/opt/ft9xxtoolchain/2.7.6/Eclipse plugins
```
- follow the Eclipse plugin installation process to install the BridgeTek plugin.

The Eclipse IDE itself will provide a comprehensive design environment including a project explorer, colour coded text editor and additional error and warning windows. Compilations and deployment of project code to the target hardware may all be handled within the IDE.

## Visual Studio Code Support
Microsoft Visual Studio Code (VSCode) is a popular IDE for developers. Bridgetek provide the required compilation and debugging tools in the FT9xx Toolchain to use VSCode to develop programs for the FT9xx. 
The VSCode configuration for FT9xx is setup using JSON configuration files. The GitHub project [Bridgetek/ft9xx-vscode](https://github.com/Bridgetek/ft9xx-vscode) provides a template application demonstrating use of VSCode for FT9xx devices.
