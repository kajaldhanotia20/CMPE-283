<h1>CMPE 283 Assignment-01</h1>
<h3>By Sumeet Gupta and Kajal Dhanotia</h3>

<h2>Assignment 1</h2>

<h3>Work done by Kajal (015210884):</h3>
Me along with Sumeet worked together to complete CMPE 283 Assignment. First, I created the GitHub repository and forked linux repository from torvalds:master. I then retrieved the .c file provided and began editing four remaining structs. I referred to the Intel SDM for doing this. I started working on google cloud. I made GCP VM instance and worked on below mentioned steps.

<h3>Work done by Sumeet(015252003):</h3>
I worked with Kajal for this assignment. On my machine, I retrieved the .c file edited by Kajal and added definitions for the different capability info regions by referring Intel SDM. I also added four remaining rdmsr VM feature code. I also created an Ubuntu 20.04.3 VM on my laptop through VMWare Workstation. I faced multiple issues on VMWare Workstation while executing make command but then we later decided to work on GCP VM instance.

<h3>Steps followed:</h3>
1. Download and install vmware workstation on laptop. <br>
2. Create an Ubuntu 20.04.3 virtual machine (4 GB RAM and 100 GB Hard Disk) <br>
3. Retrieve the starter .c file and makefile from canvas. <br>
4. Study about the controls that are used in assignment.
| MSR Name |	MSR Index |	Description |	References |
| :--- | :--- | :--- | :--- |
| IA32_VMX_PINBASED_CTLS |	0x481 |	This MSR is used for pinbased controls if no true controls capability |	SDM volume 3C, section 24.6.1 |
| IA32_VMX_PROCBASED_CTLS |	0x482 |	This MSR is used for primary procbased controls if no true controls capability |	SDM volume 3C, section 24.6.2 |
| IA32_VMX_PROCBASED_CTLS2 |	0x48B |	This MSR is used for secondary procbased controls if available |	SDM volume 3C, section 24.6.2 |
| IA32_VMX_EXIT_CTLS |	0x483 |	This MSR is used for exit controls if no true controls capability |	SDM volume 3C, section 24.7.1 |
| IA32_VMX_ENTRY_CTLS |	0x484 |	This MSR is used for entry controls if no true controls capability |	SDM volume 3C, section 24.8.1 |

5. Add capability structs based on info from SDM and make calls to rdmsr and report_capability in the .c file<br>
6. In the directory of the .c file and makefile, call ‘make’. <br>
7. Call ‘sudo insmode ./cmpe283-1.ko’ to load the file. <br>
8. Use command dmesg show the result message. <br>
<h3>Output Screenshots:</h3>

<ul>
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

