
<img align="left" src="https://raw.githubusercontent.com/levinbgu/NeatSeq-Flow_Docker/master/logo.png" width="200">

NeatSeq-Flow-Using-Docker
===============================

&nbsp;  


## Running the NeatSeq-Flow Platform on Windows/Mac Using a Docker Container

## Table of Contents    
- [Install on Windows](#install-on-windows)
  - [For Windows 10](#for-windows-10)
  - [For Older Versions of Windows](#for-older-versions-of-windows)
  - [Get and Run The NeatSeq-Flow Docker Container](#get-and-run-the-neatseq-flow-docker-container)
- [Install on Mac](#install-on-mac)
- [Running a Test Work-Flow](#running-a-test-work-flow)

***

## Install on Windows
  ### For Windows 10
  
  You Will Need (Download and Install):
    
  - [Docker for Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows). 
  - [Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/).
  - [MobaXterm](https://mobaxterm.mobatek.net/download.html)

  ### For Older Versions of Windows
  
  You Will Need:
    
  - [Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/).
  - [MobaXterm](https://mobaxterm.mobatek.net/download.html)
      
  ### Get and Run The NeatSeq-Flow Docker Container 
  
<img align="left" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Kitematic.png" width="50">
     
Click on the Kitematic Icon


&nbsp;
 


***
  
<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Get_Container.png" width="550">

  1. In the search bar type 'NeatSeq'
  2. Click on the "CREATE" button.
  
&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**Note: It Will Take Some Time to Download!!!** 


<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Download_Container.png" width="550">

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

***

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Container_Running.png" width="550">


  1. If in the 'CONTAINER LOGS' the line "*** Running /bin/bash" appears, the container is up and running.
  2. This information [computer_name_or_IP **:** port_number] will be used in the next step.
  
&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**IMPORTANT: Don't Close This Window As Long as You Are Using NeatSeq-Flow**

***

  <img align="left" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/MobaXterm.png" width="50">
     
Click on the MobaXterm Icon

&nbsp;

***

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/MobaXterm_Setup.png" width="550">


  1. Click on the "Session" button.
  2. Click on the "SSH" button.
    - Edit the "Remote host" tab to the "computer_name_or_IP" found in the "Kitematic" window.
    - Click on the "Specify username" check box.
    - Edit the "Specify username" tab to "sgeadmin".
    - Edit the "Port" tab to the "port_number" found in the "Kitematic" window.
  3. Click on the "OK" button.
  
  
&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

**IMPORTANT: The "port_number" Changes Every Time You Restart The Container, You Will Need to Update the SSH Session Settings**

***