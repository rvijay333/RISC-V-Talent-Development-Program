# RISC-V TALENT DEVELOPMENT PROGRAM

### This RISC-V Internship is based on RISC-V architecture and uses open-source tools to teach students about VLSI Design and RISC-V. The instructor and guide for this internship is KUNAL GHOSH sir, Founder of VLSI SYSTEM DESIGN.

---

## Details

### Name: R . VIJAY
### College: New Horizon College Of Engineering
### Email ID: rvj151003@gmail.com
### GitHub Profile: [rvijay333](https://github.com/rvijay333)
### LinkedIN Profile: [R Vijay](https://www.linkedin.com/in/r-vijay-5085022a4)

---


<details>
<summary><h2><strong>TASK-1</strong></h2></summary>

## Description
This is the TASK 1.  
The code is first typed in the *leafpad editor*.  

The C code is run in the RISC-V compiler using the -O1 optimization flag. It is seen here that at the main block, the number of instruction sets is *15*.

Similarly, we run the C code in the RISC-V compiler using the -Ofast optimization flag. It can be seen that the number of instructions has reduced to *12 instruction sets*, which indicates that the processing speed increases.

### Example: 
- *Main ending address* = 101B0  
- *Main starting address* = 10184  
  Subtracting them:  
  101B0 - 10184 = 2C  
  2C ÷ 4 = 0B (11 instructions) using -Ofast.

Similarly, when we repeat the process using -Ofast, the instructions reduce, indicating a faster way.

---

## Screenshots Task 1
<details>
  <br>
  
![ Screenshot 1](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/VirtualBox_vsdworkshop_code_sumoneton.png)
  
![ Screenshot 2](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/VirtualBox_vsdworkshop_codeofast.png)

![ Screenshot 3](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/VirtualBox_vsdworkshop_main_ofast.png)

![ Screenshot 4](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/VirtualBox_vsdworkshop_main_sumoneton.png)

</details>

</details>


<hr>
<details>
  <summary><h2><strong>TASK-2</strong></h2></summary>

## Description
In this task we understand the way to debug the code.
we use specific commands to , check the values stored in our registers and pointers . This hepls us to manage and understand the functioning of the code .
we also compile and get the output of our code in risc_v compiler .

- *the initial stack pointer value is* = 3FFFFFFB50
- *the subtracted value is 16(decimal)*
- *the final value stored in stack pointer is* = 3FFFFFFB50-10(*hexa-decimal*)
- = 3FFFFFF40 *as shown below*

  
## Screenshots Task 2
<details>
  <br>
  
![ Screenshot 1](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/VirtualBox_vsdworkshop_output_riscv_task2.png)

![ Screenshot 1](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/task2_riscv_11_01_24.png)

</details>
---

<h2>Write a simple c program :</h2>
<h3>C program to calculate area of a circle</h3>

<details>
  <br>

![C_program](https://github.com/user-attachments/assets/0eab6427-aa44-4487-9d2d-4c11e178ad2e)

</details>

<h2>Compilation using Spike :</h2>
<h3>O1-</h3>

<details>
  <br>

![Screenshot from 2025-01-13 22-28-19](https://github.com/user-attachments/assets/bc0543d2-31ba-4945-a2de-293e1026e0e8)
</details>
 


<h3>object dump for O1 -</h3>

<details>
  <br>

![o1objdump](https://github.com/user-attachments/assets/27b338d4-a331-439f-a3ec-8ca6b8a2f123)
</details>
 

<h3>Ofast -</h3>
<details>
  <br>

![Screenshot from 2025-01-13 22-23-00](https://github.com/user-attachments/assets/a7b45986-028d-4570-aaa0-ac8397133fc3)
</details>



<h3>Object dump for Ofast -</h3>
<details>
  <br>

![ofastobjdump](https://github.com/user-attachments/assets/e145d3c3-599f-49b0-aafb-b3d46b0b62b1)
</details>
</details>
<hr>

<details>
  <summary><h2><strong>TASK-3</strong></h2></summary>

<h2>RISC-V Instructions</h2>

<h2>RISC-V uses six basic instruction formats:</h2></p>
<p><h3><u>1. <ins>R-Type:</ins></u></h3> For register-register operations (e.g., add, sub).</p>
<p><h3><u>2. <ins>I-Type:</ins></u></h3> For immediate operations and loads (e.g., addi, ld).</p>
<p><h3><u>3. <ins>S-Type:</ins></u></h3> For store instructions (e.g., sd).</p>
<p><h3><u>4. <ins>B-Type:</ins></u></h3> For branch instructions (e.g., beq, bne).</p>
<p><h3><u>5. <ins>U-Type:</ins></u></h3> For instructions like lui and auipc.</p>
<p><h3><u>6. <ins>J-Type:</ins></u></h3> For jump instructions (e.g., jal).</p>

<h2>Each format has fixed fields:</h2>

<p><h3>1. <ins>opcode:</ins></h3> Identifies the instruction type.</p>
<p><h3>2. <ins>funct3 and funct7</ins>:</h3> Further specify the instruction.</p>
<p><h3>3. <ins>rd, rs1, rs2</ins>:</h3> Register destinations and sources.</p>
<p><h3>4. <ins>imm:</ins>/h3> Immediate values (encoded differently depending on the format).</p>

<h2>Each instruction's binary code is derived by filling in the fields based on the instruction's format. For example:</h2>

ld a2, 1800(gp):
        Type: I-Type
        Fields:
            opcode[6:0]: 0000011 (Load instruction).
            rd[11:7]: 01010 (a2).
            funct3[14:12]: 011 (Load double-word).
            rs1[19:15]: 00100 (gp).
            imm[31:20]: 011100000000 (1800 in decimal).
        Final binary: 01110000000000100011010110000011
        Hexadecimal: 0x7081b603
'''
<p>Then we need to identify the opcode, funct3, and funct7 values for each instruction.</p>
<p>Decode the immediate value formats for I-Type, S-Type, and J-Type instructions.</p>

<h2>RISC-V uses register aliases (x0 to x31), but their corresponding numbers are encoded in the instruction:</h2>

       x10 is a0 (binary: 01010).
       x11 is a1 (binary: 01011).
       x2 is sp (binary: 00010), and so on.
<h2>The objdump file : </h2>
<details>
  <br>

![ofastobjdump](https://github.com/user-attachments/assets/679d6c42-d7d2-4d02-924c-4e30c569544d)
</details>


<h2> This has the following RISC-V instructions - </h2>
<p>1. ld</p>
<p>2. lui</p>
<p>3. addi</p>
<p>4. sd</p>
<p>5. jal</p>
<p>6. ret (pseudo-instruction for jalr x0, ra, 0)</p>
<p>7. auipc</p>
<p>8. beqz (pseudo-instruction for beq)</p>
<p>9. j (jump instruction)</p>
<p>10. sub</p>
<p>11. li (pseudo-instruction for addi x, x0, imm)</p>
<p>12. lw</p>
<p>13. jalr</p>
<p>14. bne</p>
<p>15. call (pseudo-instruction for jal)</p>

<h2> The 32-bit pattern for the above instructions are :</h2>

| #  | Instruction   |         32-bit pattern           | Opcode   | Funct3  | Funct7   | Imm/Offset           |
|----| ------------- | -------------------------------- | -------- | ------- | -------- | -------------------- |
| 1  | ld            | 01110000000000100011010110000011 | 0000011  | 011     | -        | 1800                 |
| 2  | lui           | 00000000001000010100110101101111 | 0110111  | -       | -        | 0x21000              |
| 3  | addi          | 11111111111100010000100100010011 | 0010011  | 000     | -        | -1 (Immediate)       |
| 4  | sd            | 00000000000101000011010010010011 | 0100011  | 011     | -        | Offset from rs1      |
| 5  | jal           | 00110100000000000000000011101111 | 1101111  | -       | -        | Offset to label      |
| 6  | ret           | 00000000000000000000000001100111 | 1100111  | 000     | -        | (Uses ra)            |
| 7  | auipc         | 11111111111100000110101000101111 | 0010111  | -       | -        | Upper Immediate      |
| 8  | beqz          | 00000000110100000110010011100011 | 1100011  | 000     | -        | Relative Offset      |
| 9  | j             | 00001100000000000000000011001111 | 1101111  | -       | -        | Offset to jump       |
| 10 | sub           | 01000000101001010000010110110011 | 0110011  | 000     | 0100000  | (From rs1 and rs2)   |
| 11 | li            | 11111111111100000000100010010011 | 0010011  | 000     | -        | -1 (Immediate)       |
| 12 | lw            | 00000000000101001000010010000011 | 0000011  | 010     | -        | Load address offset  |
| 13 | jalr          | 00000000000001000000000011100111 | 1100111  | 000     | -        | Indirect jump offset |
| 14 | bne           | 00000000000100000001010011100011 | 1100011  | 001     | -        | Relative Offset      |
| 15 | call          | 00000000000000000000000011101111 | 1101111  | -       | -        | Offset to function   |

----
</details>
</details>
<hr>

<details>
  <summary><h2><strong>TASK-4</strong></h2></summary>

#### Following are the differences between standard RISCV ISA and the Instruction Set given in the reference repository:  
  
|  **Operation**  |  **Standard RISCV ISA**  |  **Hardcoded ISA**  |  
|  :----:  |  :----:  |  :----:  |  
|  ADD R6, R2, R1  |  32'h00110333  |  32'h02208300  |  
|  SUB R7, R1, R2  |  32'h402083b3  |  32'h02209380  |  
|  AND R8, R1, R3  |  32'h0030f433  |  32'h0230a400  |  
|  OR R9, R2, R5  |  32'h005164b3  |  32'h02513480  |  
|  XOR R10, R1, R4  |  32'h0040c533  |  32'h0240c500  |  
|  SLT R1, R2, R4  |  32'h0045a0b3  |  32'h02415580  |  
|  ADDI R12, R4, 5  |  32'h004120b3  |  32'h00520600  |  
|  BEQ R0, R0, 15  |  32'h00000f63  |  32'h00f00002  |  
|  SW R3, R1, 2  |  32'h0030a123  |  32'h00209181  |  
|  LW R13, R1, 2  |  32'h0020a683  |  32'h00208681  |  
|  SRL R16, R14, R2  |  32'h0030a123  |  32'h00271803  |
|  SLL R15, R1, R2  |  32'h002097b3  |  32'h00208783  |   
  

#### * Output Waveform of various instructions * 
</details>
  <br>

<details>
<summary><h2><strong>TASK-1</strong></h2></summary>




</details>











  

![OUTPUT WAVEFORMS](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/task4.png)
</details>
___
</details>
<hr>
