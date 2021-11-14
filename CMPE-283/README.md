<h1>CMPE 283 Assignments for Fall 2021</h1>
<h3>By Sumeet Gupta and Kajal Dhanotia</h3>

<h2>Assignment 1</h2>

<h3>Kajal's Contribution:</h3>
Me along with Sumeet worked together to complete CMPE 283 Assignment. First, I created the GitHub repository and forked linux repository from torvalds:master. I then retrieved the .c file provided and began editing four remaining structs. I referred to the Intel SDM for doing this.

<h3>Sumeet's Contribution:</h3>
I worked with Kajal for this assignment. On my machine, I retrieved the .c file edited by Kajal and added definitions for the different capability info regions. I also added four remaining rdmsr VM feature code. I also created a Ubuntu 20.04.3 VM on my laptop through VMWare Workstation. 

<h3>Steps followed:</h3>
1. Download and install vmware workstation on laptop.
2. Create an Ubintu 20.02.3 virtual machine (4 GB RAM and 100 GB Hark Disk)
3. Retrieve the starter .c file and makefile from canvas.<br>
4. Add capability structs based on info from SDM and make calls to rdmsr and report_capability in the .c file
