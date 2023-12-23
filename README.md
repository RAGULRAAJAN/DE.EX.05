# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
Create a New Project:
Open Quartus and create a new project by selecting "File" > "New Project Wizard." Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA). 2. Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language. 3. Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic. 4. Compile the Project: To compile the project, click on "Processing" > "Start Compilation" in the menu. Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device. 5. Analyze and Fix Errors:

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. Review and fix any issues in your code if necessary. View the RTL diagram. 6. Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".

Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.
### PROGRAM 
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: RAGUL RAAJAN .T
RegisterNumber: 23007752
### 1.SR FLIP FLOP:
![Screenshot 2023-12-23 071926](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/97b3dcee-8f25-4372-ac75-d295bad8b9e3)
### 2.D FLIP FLOP:
![Screenshot 2023-12-23 072446](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/94ba3130-9833-44c9-89b3-ef3e822aa778)
### 3.JK FLIP FLOP:
![Screenshot 2023-12-23 072559](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/3a2c6afe-11ad-4c9a-bc05-a36a17c8aae3)
### 4.T FLIP FLOP:
![Screenshot 2023-12-23 072715](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/7caf3430-2a03-41c4-9b63-f40a96762e8f)

### RTL DIAGRAM:
### SR FLIP FLOP:
![Screenshot 2023-12-23 072947](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/458da7f4-6bf8-44c9-ac53-3fdf2394dd8c)

### D FLIP FLOP:
![Screenshot 2023-12-23 073000](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/428b9ef2-e40d-4d48-abfe-8deb697f0716)

### JK FLIP FLOP:
![Screenshot 2023-12-23 073011](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/528e49ea-929e-494a-a9b5-15ad8683bfaf)

### T FLIP FLOP:
![Screenshot 2023-12-23 073022](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/1e241661-059b-4c49-b5aa-5370b1332633)

### TRUTH TABLE:

###  SR FLIP FLOP:
![Screenshot 2023-12-23 073310](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/d9a747b0-64b8-459d-85b1-94490db192bd)

### D FLIP FLOP:
![Screenshot 2023-12-23 073410 - Copy](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/4340fbea-cddf-47a4-bb55-f2ab8dfc70ba)

### JK FLIP FLOP:
![Screenshot 2023-12-23 073708](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/6b90369b-4af7-4534-b3f2-f867f1508eee)

### T FLIP FLOP:
![Screenshot 2023-12-23 073501](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/82891beb-b60b-4680-8c9a-f41bce517a35)

### TIMING DIGRAMS FOR FLIP FLOPS 

###  SR FLIP FLOP:
![Screenshot 2023-12-23 074055](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/c5fe9bd9-c21a-4db1-be12-55f702d1edab)

### D FLIP FLOP:
![Screenshot 2023-12-23 074114](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/22173ffb-e3c5-423c-bc43-a40fe0c1875c)

### JK FLIP FLOP:
![Screenshot 2023-12-23 074131](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/ca771aa6-d3de-4e98-9371-631dc0db53b5)

### T FLIP FLOP:
![Screenshot 2023-12-23 074150](https://github.com/RAGULRAAJAN/DE.EX.05/assets/147473144/87a91196-6a87-4c89-ace5-5b3b624bc6fd)

### RESULTS :
Thus, all the FLIP FLOPS are designed and the truth tables are verified using quartus software.
