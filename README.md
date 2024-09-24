# EXPERIMENT--01-ALP-FOR-8086
```
Name : SUDHIR KUMAR
Roll no : 212223230221
Date of experiment : 13-08-2024
```
## Aim: To Write and execute ALP on fundamental arithmetic and logical operations
## Components required: 8086  emulator 
## Theory 
Running The Emulator (emu8086) Intro 8086 Microprocessor Emulator, also known as EMU8086, is an emulator of the program 8086 microprocessor. It is developed with a built-in 8086 assembler. This application is able to run programs on both PC desktops and laptops. This tool is primarily designed to copy or emulate hardware. These include the memory of a program, CPU, RAM, input and output devices, and even the display screen. There are instructions to follow when using this emulator. It can be executed into one of the two ways: backward or forward. There are also examples of assembly source code included. With this, it allows the programming of assembly language, reverse engineering, hardware architecture, and creating miniature operating system (OS). The user interface of 8086 Microprocessor Emulator is simple and easy to manage. There are five major buttons with icons and titles included. These are “Load”, “Reload”, “Step Back”, “Single Step”, and “Run”. Above those buttons is the menu that includes “File”, “View”, “Virtual Devices”, “Virtual Drive”, and “Help”. Below the buttons is a series of choices that are usually in numbers and codes. At the leftmost part is an area called “Registers” with an indication of either “H” or “L”. The other side is divided into two, which enables users to manually reset, debug, flag, etc. What is 8086 emulator emu8086 is an emulator of Intel 8086 (AMD compatible) microprocessor with integrated 8086 assembler and tutorials for beginners. Emulator runs programs like the real microprocessor in step-by-step mode. it shows registers, memory, stack, variables and flags.


 ## Running the Emulator :
1.	Download and install emu8086 (www.emu8086.com) It is usually installed in C:\EMU8086 subfolder in the “Windows” directory
2.	  Run  emu8086 icon (on the desktop or in the c:\EMU8086 folder of window) It has green color 
 
 
3.		write the code for the appropriate program for ADDITION,SUBTRACTION, MULTIPLICATION,  DIVISION operations 

4.	 Compile the program and check for the errors 
5.	Run (once there is no syntax error) 

6.	Click OK to see/view the output of your program on the Emulator screen. 


7.	After running the program, another menu screen will be displayed, where you have the option to “View” symbol table,
8.	 


![image](https://user-images.githubusercontent.com/36288975/189273263-d65baae9-4b8f-4723-afb3-c0ffa4052b04.png)











9.	Click on emulate to start emulation 








![image](https://user-images.githubusercontent.com/36288975/189273273-9bb36ec1-e2e8-4892-8d35-37707332bfdc.png)








10.	If no errors are found click on run the program and check the status of various flags in the flags tab as shown below 






![image](https://user-images.githubusercontent.com/36288975/189273277-113a2a33-4a40-4ff8-95a5-ecd3a1f504fe.png)







## Programs for arithmetic  operations
### Addition of 8 bit ALP 
```
org 100h  

mov al, 25h    
mov bl, 13h    
add al, bl     
mov [02375h], al

ret
```

### Output  
![362518433-0e5a104a-d447-4aa8-b451-cd06f6043031](https://github.com/user-attachments/assets/798124b1-a535-44f7-9deb-d20d0711559b)
 
### Subtraction of 8 bit numbers  ALP 
```
org 100h  

mov al, 25h    
mov bl, 13h    
sub al, bl     
mov [2375h], al

ret            

```
### Output  

![362527352-eae4339b-24a4-4fd3-8593-0fe32dd8502c](https://github.com/user-attachments/assets/86edac06-3ee9-40bf-99af-481598eff5f9)

### Multiplication ALP
```
org 100h

mov ax, 4101h  
mov [6000h], ax
mov bx, 2218h  
mov ax, [6000h]
mul bx         

mov [5008h], ax

ret
```
### Output  

![362527713-abc0a116-5a86-4645-b86a-5713488848db](https://github.com/user-attachments/assets/3432ea23-1272-447b-8818-d62cbe622351)

### Division ALP
```
org 100h            

mov ax, 0b161h      
mov dx, 0           

mov [2000h], 0a415h 
mov bx, [2000h]     
div bx              

mov [1121h], ax     

ret                 
```
### Output  

![362528014-0f88b600-6fb8-4414-b601-288381ec42d7](https://github.com/user-attachments/assets/0f8e81b3-458c-49c7-beab-7e353c94b26b)

## Logical Operations :
### OR ALP :
```
org 100h

mov ax, 0A23h
mov si, 0b13h
or ax, si

ret
```
### Output 

![362530622-7a252420-c435-4de8-bd94-032128a4b573](https://github.com/user-attachments/assets/f36e3a39-e8cb-41d1-8fb5-57bd7a20172d)

### AND ALP :
```
org 100h

mov di, 0532h 
mov cx, 0A23h
mov dx, 0b13h
and cx, dx   
mov [0007h], cx

ret
```
### Output 

![362530808-18173478-49de-483c-84a2-3fdff781932c](https://github.com/user-attachments/assets/972c7b42-f7f0-4a17-aa36-4fd7fe6007f3)

### NOT ALP :
```
org 100h

mov ax, 0A32h  
not ax         
               
mov [0008h], ax

ret
```
### Output

![362530955-7a453c92-cc40-4017-94cb-7bdedff3cbc1](https://github.com/user-attachments/assets/cb3226bc-32df-49bc-a46e-6f373a59c90d)

### NAND ALP :
```
org 100h 

mov ax, 0A32h  
mov bx, 0B13h  
and ax, bx     
not ax         
mov [0008h], ax

ret
```
### Output

![362532760-9dde0de5-7fcf-4a1d-93ea-7ea467925a8c](https://github.com/user-attachments/assets/88737397-2e5e-43c0-891c-715f9c88c4ac)

### NOR ALP :
```
org 100h

mov ax, 0A45h  
mov bx, 0C30h  
or ax, bx      
not ax         
mov [0020h], ax

ret
```
### Output

![362533927-f34814dd-1578-4239-aa6c-39422be6c6f0](https://github.com/user-attachments/assets/f22678be-ccb7-4bb6-8557-8c6f2d963a9a)

### XOR ALP :
```
org 100h
mov ax, 0A32h  
mov bx, 0B13h  
xor ax, bx     
               
mov [0028h], ax

ret
```
### Output

![362534166-2facb33a-a5ad-431c-bfa8-8182d3ae9c69](https://github.com/user-attachments/assets/0121f1ec-69f9-48a5-9edc-0fb244b942be)

## Result :
Thus, Assembly Language Program for fundamental arithmetic and logical operations are exected succesfully.







