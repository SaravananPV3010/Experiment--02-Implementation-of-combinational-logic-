# Implementation-of-combinational-logic-gates

 
## Aim:

#### To implement the given logic function verify its operation in Quartus using Verilog programming.

#### F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

#### F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
#### Hardware – PCs, Cyclone II , USB flasher

#### Software – Quartus prime


## Theory:
####      A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
 
## Procedure:
#### 1. Create a New Project:

##### Open Quartus and create a new project by selecting "File" > "New Project Wizard."
##### Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
#### 2. Create a New Design File:

##### Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
##### Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
#### 3. Write the Combinational Logic Code:

##### Open the newly created Verilog or VHDL file and write the code for your combinational logic.
#### 4. Compile the Project:

##### To compile the project, click on "Processing" > "Start Compilation" in the menu.
##### Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
#### 5. Analyze and Fix Errors:

##### If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
##### Review and fix any issues in your code if necessary.
##### View the RTL diagram.
##### 6. Verification:

##### Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
##### Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
##### Give the Input Combinations according to the Truth Table amd then simulate the Output waveform
## Program:
#### Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
#### Developed by: SARAVANAN PARTHIBAN VIJAYALAKSHMI
#### RegisterNumber:  23002149

##### Logic Function F1
```
module ex02(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire w1,w2,w3,w4,w5;
assign w1=(~A)&(~B)&(~C)&(~D);
assign w2=(A) &(~B)&(~D);
assign w3=(~B)& (C) &(~D);
assign w4=(~A)& (B) & (C) & (D);
assign w5=(B) & (~C)&(D);
assign F1=w1|w2|w3|w4|w5;
endmodule
```
##### Logic Function F2
```
module ex02ii(W,X,Y,Z,F2);
input W,X,Y,Z;
output F2;
wire a1,a2,a3,a4;
assign a1=(X)&(~Y)&(Z);
assign a2=(~W)&(X)&(Y);
assign a3=(W)&(~X)&(Y);
assign a4=(W)&(X)&(Y);
assign F2=a1|a2|a3|a4;
endmodule
```


## Output:
### Logic Function F1 - 
### RTL:
![Screenshot 2023-11-27 203821](https://github.com/SaravananPV3010/Experiment--02-Implementation-of-combinational-logic-/assets/139754526/0d29e176-e30c-409c-b0a1-38dfd5c95435)

### TruthTable:
![image](https://github.com/SaravananPV3010/Experiment--02-Implementation-of-combinational-logic-/assets/139754526/1273658d-48d1-4895-b623-71b91ebc6c54)

### WaveForm:
![image](https://github.com/SaravananPV3010/Experiment--02-Implementation-of-combinational-logic-/assets/139754526/8cc1a6c0-e55a-4ac4-a931-b5361d635848)

### Logic Function F2 -
### RTL:
![image](https://github.com/SaravananPV3010/Experiment--02-Implementation-of-combinational-logic-/assets/139754526/325026dd-6ac7-46b9-9f4d-20ae73d9767d)

### TruthTable:
![image](https://github.com/SaravananPV3010/Experiment--02-Implementation-of-combinational-logic-/assets/139754526/0595245c-f070-4153-afe1-a846f6a93249)

### WaveForm:
![image](https://github.com/SaravananPV3010/Experiment--02-Implementation-of-combinational-logic-/assets/139754526/94e77539-be6b-41b6-a9e3-0ac4825ecc47)



## Result:
##### Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
