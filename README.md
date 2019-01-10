
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
- [Contact](#contact)

***

## Install on Windows
  **[Read more on Docker for Windows](https://docs.docker.com/docker-for-windows/install/)**
  ### For Windows 10
  
  You Will Need (Download and Install):
    
  - [Docker for Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows). 
  - [Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/).
  - [MobaXterm](https://mobaxterm.mobatek.net/download.html)

  ### For Older Versions of Windows
  
  You Will Need (Download and Install):
    
  - [Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/).
  - [MobaXterm](https://mobaxterm.mobatek.net/download.html)
      
  ### Get and Run The NeatSeq-Flow Docker Container 
  
<img align="left" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Kitematic.png" width="50">
     
Click on the Kitematic Icon


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

**IMPORTANT: Don't Close This Window As Long as You Are Using NeatSeq-Flow!!!!!**

***

  <img align="left" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/MobaXterm.png" width="50">
     
Click on the MobaXterm Icon


***

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/MobaXterm_Setup.png" width="550">


  1. Click on the "Session" button.
  2. Click on the "SSH" button.  
     - Edit the "Remote host" tab to the "computer_name_or_IP" found in the "Kitematic" window.
     - Click on the "Specify username" check box.
     - Edit the "Specify username" tab to "sgeadmin".
     - Edit the "Port" tab to the "port_number" found in the "Kitematic" window.
  3. Click on the "OK" button.
  4. Enter the password "sgeadmin", **Note That You Will Not See a Typing Feedback**
  
&nbsp;

&nbsp;


**IMPORTANT: The "port_number" Changes Every Time You Restart The Container, You Will Need to Update the SSH Session Settings**

**Note: For 'root' user the password is 'root'**

***

## Install on Mac

  You Will Need (Download and Install):
  - [Docker for Mac](https://hub.docker.com/editions/community/docker-ce-desktop-mac). 
  - [Docker Toolbox](https://docs.docker.com/toolbox/overview/)
  **[Read more on Docker for Mac](https://docs.docker.com/docker-for-mac/install/)**

**IMPORTANT!!! Getting the NeatSeq-Flow Container on Mac Is Similar To [Windows](#get-and-run-the-neatseq-flow-docker-container), However it was NOT Tested Yet!!!**

***

## Running a Test Work-Flow

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Commandline.png" width="450">


### In the Terminal Connected to The Container as 'sgeadmin', Type:


&nbsp;

&nbsp;

&nbsp;

  1. Create New Directory for the Tutorial
       ```
         mkdir Tutorial
         cd Tutorial
       ```
  2. Download the **Tutorial Work-Flow Parameter file**:
        ```
            wget https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Tutorial_Parameter_file.yaml
        ```
        
  3. Download the **Tutorial Work-Flow Sample file**
        ```
           wget https://raw.githubusercontent.com/bioinfo-core-BGU/neatseq-flow-tutorial/master/Samples_conda.nsfs
        ```
        
  4. Run **NeatSeq-Flow GUI**:
        ``` 
          NeatSeq_Flow_GUI.py
        ```
  5.Load a Work-Flow Parameter File
   
   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-GUI/master/doc/Load_WorkFlow_parameter_file.gif" width="650">
      
   - In the 'Work-Flow' Tab click on the 'Load WorkFlow' button, then choose the work-flow's parameter file 'Tutorial_Parameter_file.yaml' and click open.
  6. Run the Work-Flow
   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Generate_scripts.gif" width="650">
   
   
   **In the 'Run' Tab:**
    1. Choose the conda environment of which NeatSeq-Flow installed in:
      - Click on the "Search" button next to the "Conda environment to use" field and wait until at least 2 conda environments are found. If an error occurs try again.
      - Select from the "Conda environment to use" drop-down menu the "NeatSeq_Flow Tutorial" environment.
   
   
   2. Generate the Work-Flow scripts:
   
      - Select the Sample file.
      - Select the Work-Flow parameter-file.
      - Choose the Project Directory to generate the Work-Flow scripts in (the default is to use the Current Working Directory )
      - Click on the 'Generate scripts' button.

   3. To run the Work-Flow click on the 'Run scripts' button
   
   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Run_scripts.gif" width="650">  
   
   4. It is possible to monitor the Work-Flow progress by clicking the 'Run Monitor' button
   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Run_Monitor.gif" width="650">
   
   


# Contact
Please contact Liron Levin at: [levinl@post.bgu.ac.il](mailto:levinl@post.bgu.ac.il)
