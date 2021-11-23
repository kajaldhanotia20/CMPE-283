<h1>CMPE 283 Assignments</h1>
<h3>By Sumeet Gupta and Kajal Dhanotia</h3>

<h2>Assignment-01</h2>

<h3>Work done by Sumeet (015252003):</h3>
I worked with Kajal for this assignment. On my machine, I retrieved the .c file edited by Kajal and added definitions for the different capability info regions by referring Intel SDM. I also added four remaining rdmsr VM features code. I then created an Ubuntu 20.04.3 VM on my laptop through VMWare Workstation. I installed required packages onto it but I faced multiple issues on the VM while executing make command. The make modules command ran for one entire night probably because of low RAM of thr VM. We then later decided to work on Google Cloud for the assignment.<br>

<h3>Work done by Kajal (015210884):</h3>
Me along with Sumeet worked together to complete CMPE 283 Assignment. First, I created the GitHub repository and forked linux repository from torvalds:master. I then retrieved the .c file provided in canvas and began writing code for the four remaining structs. I referred to the Intel SDM for doing this. The references are mentioned below. After which, I started working on Google Cloud Platform. I made GCP N2 type VM instance with nested virtualization enabled and worked on below mentioned steps.<br>

<h3>Steps followed:</h3>
1. Retrieve the starter .c file and Mekefile from canvas. <br>
2. Add the remaining code sections to the file.(struct, definitions and vm features)<br>


| MSR Name |	MSR Index |	Description |	References |
| :--- | :--- | :--- | :--- |
| IA32_VMX_PINBASED_CTLS |	0x481 |	This MSR is used for pinbased controls if no true controls capability |	SDM volume 3C, section 24.6.1 |
| IA32_VMX_PROCBASED_CTLS |	0x482 |	This MSR is used for primary procbased controls if no true controls capability |	SDM volume 3C, section 24.6.2 |
| IA32_VMX_PROCBASED_CTLS2 |	0x48B |	This MSR is used for secondary procbased controls if available |	SDM volume 3C, section 24.6.2 |
| IA32_VMX_EXIT_CTLS |	0x483 |	This MSR is used for exit controls if no true controls capability |	SDM volume 3C, section 24.7.1 |
| IA32_VMX_ENTRY_CTLS |	0x484 |	This MSR is used for entry controls if no true controls capability |	SDM volume 3C, section 24.8.1 |

<br>

3. Create a GitHub repo, fork the torvalds:master repo and create a folder CMPE 283 inside the linux repo.<br>
4. Upload the edits .c file and Makefile to the folder to get started with building the kernel.<br>
5. Create a GCP account and set up a VM compute instance.<br>
6. Create an N2 type- Ubuntu 20.04.3 virtual machine (15 GB RAM, 4 vcpus and 100 GB HDD) in Las Vegas region. Make sure the nested virtualization is enabled on the machine. <br>
7. Clone the github repo created in the VM instance.<br>
8. Run the ```make``` command.Running this command initially gave us a lot of package dependency errors.<br>
9. Install the packages by ```apt-get install <package name>```. To name a few, we had to install flex, bison, binutils, libelf and libssl.<br> 
10. Had to run ```make oldconfig``` and ```make prepare``` in order to build the entire kernel in the cloned source code repo.<br>
11. The ```make modules``` and ```make``` command then ran successfully. It took about 1.5 hours for it to complete.<br>
12. Copy all the modules built to the boot location. (strip debugging information)<br>
13. Run the ```make install``` command to install the kernel on the system.<br>
14. Reboot the VM so the the newly installed kernel boots up.<br>
15. Run the ```make``` command in the root directory. (the output screenshot is attached below). Include the MODULE_LICENSE line in the cmpe283-1.c file.<br> 
16. Run the ```sudo insmod cmpe283-1.ko``` command to insert modules in the kernel.<br>
17. Run the ``` dmesg ``` command to display the output printed on the system message buffer console.<br>
  
<h3>Output Screenshots:</h3>
<ul>
<li>Final make command output with timestamp and kernel version:<br>

![image](https://user-images.githubusercontent.com/38569308/141919965-c990c13b-0442-4e74-9efe-8784bfa29f96.png)

<br>
  <li>Pinbased control Output:<br>
    
![image](https://user-images.githubusercontent.com/38569308/141735854-90103e4d-440a-4a45-a303-3a35eb1a3653.png)
    
<br>
  </li>
  
<li>Primary Procbased control output:<br>
  
![image](https://user-images.githubusercontent.com/38569308/141735969-e3806d65-53d4-4378-97f1-23e492b2b2eb.png)
  
  <br></li>

<li>Secondary Procbased control output:<br>
  
![image](https://user-images.githubusercontent.com/38569308/141736059-170ce8de-a38d-476b-8df4-e662fdfc8dbc.png)
  
  <br></li>

<li>Exit controls output:<br>
  
![image](https://user-images.githubusercontent.com/38569308/141736132-98e4a443-cc86-453b-8e49-d6e96f82382b.png)
  
  <br></li>

<li>Entry controls output:<br>
  
![image](https://user-images.githubusercontent.com/38569308/141736188-9d0d7c5e-37cd-432e-9a63-932bf0a082a9.png)

  <br></li>
  
  
  ---------------------------------------------------------------------------------------------------------------------------------------
  
<h2>Assignment-02-Instrumentation via hypercall</h2>

Assignment 02 Documentation and files present in repo- https://github.com/kajaldhanotia/linux.git
  
  
