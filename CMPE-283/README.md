<h1>CMPE 283 Assignments for Fall 2021</h1>
<h3>By Sumeet Gupta and Kajal Dhanotia</h3>

<h2>Assignment 1</h2>

<h3>Work done by Kajal:</h3>
Me along with Sumeet worked together to complete CMPE 283 Assignment. First, I created the GitHub repository and forked linux repository from torvalds:master. I then retrieved the .c file provided and began editing four remaining structs. I referred to the Intel SDM for doing this.

<h3>Work done by Sumeet:</h3>
I worked with Kajal for this assignment. On my machine, I retrieved the .c file edited by Kajal and added definitions for the different capability info regions. I also added four remaining rdmsr VM feature code. I also created a Ubuntu 20.04.3 VM on my laptop through VMWare Workstation. 

<h3>Steps followed:</h3>
1. Download and install vmware workstation on laptop.<br>
2. Create an Ubintu 20.02.3 virtual machine (4 GB RAM and 100 GB Hark Disk)<br>
3. Retrieve the starter .c file and makefile from canvas.<br>
4. Add capability structs based on info from SDM and make calls to rdmsr and report_capability in the .c file<br
                                                                                                                 <br>
                                                                                                                 <br>
<h3>Output Screenshots:</h3>

Pinbased control Output:<br>
![image](https://user-images.githubusercontent.com/38569308/141735854-90103e4d-440a-4a45-a303-3a35eb1a3653.png)
<br>

Primary Procbased control output:<br>
![image](https://user-images.githubusercontent.com/38569308/141735969-e3806d65-53d4-4378-97f1-23e492b2b2eb.png)
<br>

Secondary Procbased control output:<br>
![image](https://user-images.githubusercontent.com/38569308/141736059-170ce8de-a38d-476b-8df4-e662fdfc8dbc.png)
<br>

Exit controls output:<br>
![image](https://user-images.githubusercontent.com/38569308/141736132-98e4a443-cc86-453b-8e49-d6e96f82382b.png)
<br>

Entry controls output:<br>
![image](https://user-images.githubusercontent.com/38569308/141736188-9d0d7c5e-37cd-432e-9a63-932bf0a082a9.png)

<br>

