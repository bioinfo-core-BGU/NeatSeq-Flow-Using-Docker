
<img align="left" src="https://raw.githubusercontent.com/levinbgu/NeatSeq-Flow_Docker/master/logo.png" width="200">

NeatSeq-Flow-Using-Docker
===============================

&nbsp;  


## Running the NeatSeq-Flow Platform on Windows/Mac Using a Docker Container

### For more information about **"NeatSeq-Flow"** see the full documentation on **[Read The Docs](http://neatseq-flow.readthedocs.io/en/latest/)**


## Table of Contents    
- [Install on Windows](#install-on-windows)
  - [For Windows 10](#for-windows-10)
  - [For Older Versions of Windows](#for-older-versions-of-windows)
  - [Get and Run The NeatSeq-Flow Docker Container](#get-and-run-the-neatseq-flow-docker-container)
- [Install on Mac](#install-on-mac)
- [Running a Test Work-Flow](#running-a-test-work-flow)
- [Setting The Cluster Parameters](#setting-the-cluster-parameters)
- [Contact](#contact)

***

## Install on Windows
  **[Read more on Docker for Windows](https://docs.docker.com/docker-for-windows/install/)**
  ### For Windows 10

  You Will Need (Download and Install):

  - [Desktop Docker for Windows](https://desktop.docker.com/win/stable/amd64/Docker%20Desktop%20Installer.exe).
  - [WSL Update](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi).
  - [MobaXterm](https://mobaxterm.mobatek.net/download.html)

  ### For Older Versions of Windows

  You Will Need (Download and Install):

  - [Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/).
  - [MobaXterm](https://mobaxterm.mobatek.net/download.html)

  ### Get and Run The NeatSeq-Flow Docker Container

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/cmd1.png" width="550">

  1. In the Windows search bar type 'cmd'
  2. Click on the "Command Prompt" icon.

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

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/cmd2.png" width="550">

  1. Type in the terminal: 
&nbsp;
**docker pull levinl/neatseq-flow**
&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;


**Note: It Will Take Some Time to Download!!!**
&nbsp;

&nbsp;

&nbsp;


Click on the Docker Descktop Icon
<img align="left" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Docker.png" width="50">
***
&nbsp;


<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Docker1.png" width="550">

&nbsp;

1. Click on the images tab
2. Click on the RUN button next to the "levinl/neatseq-flow" image.
3. Click on the down arrow
&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;


<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Docker2.png" width="550">
&nbsp;

&nbsp;

1. Type 22 in the localhost port next to the 22/tcp container port
2. Click on the "+"
3. Type 49190 in the localhost port next to the 49190/tcp container port
4. Click on the Run button.

&nbsp;

&nbsp;


<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Docker3.png" width="550">
&nbsp;

&nbsp;

1. Click on the "Containers/Apps" Tab
2. Click on the Available Container

&nbsp;

&nbsp;

&nbsp;

&nbsp;

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Docker4.png" width="550">
&nbsp;

&nbsp;

Wait till you see **"Starting Flexx event loop."** in the terminal LOGS. 
&nbsp;

**Note:** it could take a couple of minutes!

&nbsp;

&nbsp;

&nbsp;

&nbsp;


***
### Connect to the Docker container using SSH


  <img align="left" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/MobaXterm.png" width="50">

Click on the MobaXterm Icon


***


<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/MobaXterm_Setup.png" width="550">


Click on the "Session" button.
  1. Click on the "SSH" button.  
  2. Edit the "Remote host" tab to "localhost".
     - Click on the "Specify username" check box.
  3. Edit the "Specify username" tab to "sgeadmin".
  4. Click on the "OK" button.
  5. Enter the password "sgeadmin", **Note That You Will Not See a Typing Feedback**
  6. It is now possible to transfer files to and from the container to be used by NeatSeq-Flow.
  
**Note:** For 'root' user the password is 'root'

**IMPORTANT:** It is possible to add users (google: 'add users in linux'), however you need to login as root for that

&nbsp;

**IMPORTANT:** It is Possible to change the password after you log in(google: 'change user password in linux')
&nbsp;

&nbsp;

***
### Connect to the NeatSeq-Flow GUI using a web browser

<img align="right" src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/NeatSeq_Flow_login.png" width="550">

1. Open a web browser and type: localhost:49190 .
2. In the Login page fill in the 'User Name' field with "sgeadmin"
3. Fill in the 'Password' field with "sgeadmin" 

**IMPORTANT:** You can login as any available user defined in the container

&nbsp;

&nbsp;

&nbsp;

&nbsp;


## Install on Mac

  You Will Need (Download and Install):
  - [Docker for Mac](https://hub.docker.com/editions/community/docker-ce-desktop-mac).
  - [Docker Toolbox](https://docs.docker.com/toolbox/overview/)

  **[Read more on Docker for Mac](https://docs.docker.com/docker-for-mac/install/)**

**IMPORTANT!!! Getting the NeatSeq-Flow Container on Mac Is Similar To [Windows](#get-and-run-the-neatseq-flow-docker-container), However it was NOT Tested Yet!!!**

***

## Running a Test Work-Flow

### In the [Terminal](#connect-to-the-docker-container-using-ssh) Connected to The Container as 'sgeadmin', Type:


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

  4. Login to the [NeatSeq-Flow GUI](#connect-to-the-neatseq-flow-gui-using-a-web-browser)

  5. Load a Work-Flow Parameter File

   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Load_WorkFlow_parameter_file.gif" width="650">

   - In the 'Work-Flow' Tab click on the 'Load WorkFlow' button, then choose the work-flow's parameter file 'Tutorial_Parameter_file.yaml' and click open.
  6. Run the Work-Flow
   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Generate_scripts.gif" width="650">


   **In the 'Run' Tab:**

   1. Generate the Work-Flow scripts:

      - Select the Work-Flow parameter-file.
      - Select the Sample file.
      - Choose the Project Directory to generate the Work-Flow scripts in.
      - Click on the 'Generate scripts' button.

   2. To run the Work-Flow click on the 'Run scripts' button

   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Run_scripts.gif" width="650">  

   4. It is possible to monitor the Work-Flow progress by clicking the 'Run Monitor' button
   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Run_Monitor.gif" width="650">



### For more information about **"NeatSeq-Flow"** see the full documentation on **[Read The Docs](http://neatseq-flow.readthedocs.io/en/latest/)**

## Setting The Cluster Parameters

  **Make Sure That the Cluster Settings are as Follows:**

  <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/Cluster_settings.gif" width="650">

  - In The 'Cluster' Tab:
    1. Change the 'Executor' 'Value' to SGE
    2. Change the 'Qsub_path' 'Value' to /opt/sge/bin/lx-amd64/
    3. Change the 'Qsub_q' 'Value' to all.q

## Setting The Available CPUs and Memory For The Container

   <img src="https://raw.githubusercontent.com/bioinfo-core-BGU/NeatSeq-Flow-Using-Docker/master/doc/CPU_and_Memory_settings.png" width="650">

   Click the whale icon in the status bar and choose 'settings'
   - Click on advanced tab on the left.
   - Change the number of cpus and the amount of memory you want to be available to the container.
   - Click on the 'Apply' button

  **IMPORTANT!! Restart the Container for the changes to take place**

  To see how many CPUs and Memory available to the container, Type in the command-line:

  ```
    ###### CPU info:######
    lscpu
    ###### Memory info:######
    free -m

  ```



# Contact
Please contact Liron Levin at: [levinl@post.bgu.ac.il](mailto:levinl@post.bgu.ac.il)
