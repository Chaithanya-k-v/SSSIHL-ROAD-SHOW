# SSSIHL Road show
The main focus of the project focused on converting high level logic descriptions to a physical chip design suitable for the manufacturing and release to the market.We use RISC-V architecture to build this package.<br />
1. Open the ubuntu software from the oracle virtual box in windows <br /> <br />
![Screenshot 2024-12-13 100311](https://github.com/user-attachments/assets/1e43c276-b44b-4370-8dfc-cf3b2faac189) <br />
2. Open the terminal and Enter sudo apt install gedit <br /> Then after the execution of the command enter the password as : vsdiat <br />
![image](https://github.com/user-attachments/assets/22dedc56-cdb7-4fe2-b1ab-eb38ace7ef85)<br />
3. Create a file called hello.c and enter  the following code  <br />  <br />
![image](https://github.com/user-attachments/assets/dc4c1eaa-562c-4503-bb5d-09311979c8dc)<br />
4. Now type gcc and enter the file name Eg:hello.c <br /> and then enter the command ./a.out to execute the code <br /><br />
![image](https://github.com/user-attachments/assets/2b3422c1-e714-4896-8db3-a3116115e1e8)<br />
5. After the execution enter the command "riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o hello.o hello.c" and execute<br />
6. Now enter the following command "riscv64-unknown-elf-objdump -d hello.o" to see the following output<br />
![image](https://github.com/user-attachments/assets/36fee32a-dc81-4431-8c1d-6ce3abb6de86)<br />
7. Now change directory to openlane flow directory using the command "cd Desktop/work/tools/openlane_working_dir/openlane"<br />
8. Enter the command docker<br />
9. After the execution of the above enter the command ./flow.tcl -interactive to see the following<br />
![image](https://github.com/user-attachments/assets/02a97152-e0a1-4933-bd7b-5d02d132d0f5)<br />
10. Then enter the command "package require openlane 0.9".After execution enter the command "prep -design picorv32a" to get the following output.<br />
![image](https://github.com/user-attachments/assets/821211e1-742e-46e7-a6fb-da36abaedf17)<br />
Here we get to know about how many cell have been used and what is the distance between the source and the drain. In the above we see the number of cell are 14876 and distance is 130nm<br />
![image](https://github.com/user-attachments/assets/b8fc2379-c271-488e-9c0d-c4f5ca76bae6)<br />
11. Enter the following command "run_floorplan"<br />
![image](https://github.com/user-attachments/assets/4a811e73-ad25-4bf5-8da8-63aaf000ffd3)<br />
12. Enter the command "eog designs/picorv32a/runs/13-12_06-24/results/floorplan/picorva32a.floorplan.def.png" and execute <br />
![Screenshot 2024-12-14 202743](https://github.com/user-attachments/assets/8c822e76-536e-4d57-852d-0119ec4513c9)<br />
13. Enter the command "run_placement" and execute .<br />
![Screenshot 2024-12-13 140732](https://github.com/user-attachments/assets/388b5d3b-03af-43af-a235-36f8d3b368cf).<br />

14. Then enter the command "eog designs/picorv32a/runs/13-12_06-47/results/placement/picorva32a.placement.def.png"<br />
![Screenshot 2024-12-13 140851](https://github.com/user-attachments/assets/7e8730c0-d4b4-4fcf-bde1-b296d42c1ed4)<br />
15.Enter the command "run_cts" and execute<br />
16.Enter the command "run_routing" and execute<br />

##Summary of the RISC-V and VLSI workshop
The above workshop helped us to understand the fundamentals of the RISC-V architecture and its significance in VLSI chip design. It included practical designing and Fabrication which gave the insights on the chip designing.
