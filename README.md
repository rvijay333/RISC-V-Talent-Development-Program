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
<details>
  <br>



![OUTPUT WAVEFORMS](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/task4.png)
</details>

#### * Output Waveform interpretation * 
<details>
  <br>



![OUTPUT WAVEFORM INTERPRETATION](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/TASK_4_interpretation.png)
</details>
___
___
</details>


<hr>


<details>
  <summary><h2><strong>TASK-5</strong></h2></summary>

# Flip-Flop Simulation with Selection Indicators on VSDSquadron Mini

## Overview
This project demonstrates how to simulate four types of flip‑flops (SR, JK, T, and D) on the VSDSquadron Mini board, which is based on the CH32V00x RISC-V microcontroller. The user can select which flip‑flop to operate by pressing one of four dedicated buttons. Two additional input buttons feed the flip‑flop’s binary inputs (S, R, J, K, T, or D), and the outputs **Q** and **~Q** are shown on two LEDs. Additionally, four extra indicator LEDs light up to show which flip‑flop is currently selected, and two more LEDs display which input buttons are pressed.

### Features
- **4 Flip‑Flop Modes**: SR, JK, T, D
- **Selection Indicators**: Each flip‑flop mode has a dedicated LED.
- **Input Indicators**: Two LEDs show which input buttons are currently pressed.
- **Output LEDs**: Always show **Q** and **¬Q** for every flip‑flop type.
- **GPIO-Based**: Entirely uses GPIO pins for inputs and outputs—no extra multiplexers needed.

### Components Required

| Component                   | Quantity | Purpose/Description                                |
|-----------------------------|----------|----------------------------------------------------|
| VSDSquadron Mini Board      | 1        | The RISC-V microcontroller development board.      |
| Push Buttons                | 6        | 4 for flip‑flop selection, 2 for input bits.         |
| LEDs                        | 8        | 2 for input indicators, 2 for outputs, 4 for flip‑flop selection. |
| Resistors (330 Ω)           | 8        | Current-limiting for each LED.                     |
| Breadboard                  | 1        | For prototyping and wiring.                        |
| Jumper Wires                | ~20      | For making connections.                            |
| USB-C Cable                 | 1        | To power and program the VSDSquadron Mini.         |

## Circuit Connections

### Power & Ground
- **VSDSquadron Mini 3.3 V** → Breadboard’s top (red) power rail.
- **VSDSquadron Mini GND** → Breadboard’s bottom (blue) ground rail.

### Flip‑Flop Selection Buttons (active low)
- **SR** → PD0  
- **JK** → PD1  
- **T** → PD2  
- **D** → PD3  
*Each button’s other terminal connects to ground.*

### Input Buttons (active low)
- **BTN_IN1** → PD4  
- **BTN_IN2** → PD5  
*Each button’s other terminal connects to ground.*

### Input Indicator LEDs (active high) on Port D
- **LED_IN1** anode → PD6 → (330 Ω resistor) → GND  
- **LED_IN2** anode → PD7 → (330 Ω resistor) → GND

### Output LEDs (active high) on Port C
- **LED_OUT1 (Q)** anode → PC0 → (330 Ω resistor) → GND  
- **LED_OUT2 (¬Q)** anode → PC1 → (330 Ω resistor) → GND

### Selection Indicator LEDs (active high) on Port C
- **LED_SEL_SR** anode → PC2 → (330 Ω resistor) → GND  
- **LED_SEL_JK** anode → PC3 → (330 Ω resistor) → GND  
- **LED_SEL_T** anode → PC4 → (330 Ω resistor) → GND  
- **LED_SEL_D** anode → PC5 → (330 Ω resistor) → GND

## Working Principle
1. **Selection**: Press one of the four flip‑flop selection buttons. The corresponding selection LED lights up.
2. **Input**: Provide binary inputs by pressing BTN_IN1 (in1) and BTN_IN2 (in2). The input indicator LEDs show which buttons are pressed.
3. **Processing**: The `ProcessFlipFlop` function applies the logic for SR, JK, T, or D flip‑flops to determine the new state **Q**.
4. **Outputs**: Two LEDs always display **Q** and **¬Q**, regardless of flip‑flop type.
5. **Visual Feedback**: After a short delay, the selection resets so the user can choose another flip‑flop type.

## Truth Tables (Summary)

### SR Flip‑Flop
| S | R | Action             | Q (New)     |
|---|---|--------------------|-------------|
| 0 | 0 | No change          | Q stays same|
| 0 | 1 | Reset Q to 0       | Q = 0       |
| 1 | 0 | Set Q to 1         | Q = 1       |
| 1 | 1 | Invalid (No change) | Q stays same|

### JK Flip‑Flop
| J | K | Action                | Q (New)     |
|---|---|-----------------------|-------------|
| 0 | 0 | No change             | Q stays same|
| 0 | 1 | Reset (Q = 0)         | Q = 0       |
| 1 | 0 | Set (Q = 1)           | Q = 1       |
| 1 | 1 | Toggle (Q = ~Q)       | Q toggles   |

### T Flip‑Flop
| T | Action       | Q (New)     |
|---|--------------|-------------|
| 0 | No change    | Q stays same|
| 1 | Toggle Q     | Q = ~Q      |

### D Flip‑Flop
| D | Action       | Q (New)     |
|---|--------------|-------------|
| 0 | Q = 0        | Q = 0       |
| 1 | Q = 1        | Q = 1       |

### CIRCUIT DIAGRAM 

<details>
  <br>

![CIRCUIT DIAGRAM](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/flip_flops_using_vsd_squadron_mini.png)
</details>

</details>




<hr>

<details>
  <summary><h2><strong>TASK-6</strong></h2></summary>

  The program is : Implementation of flip flops (SR , JK , T and D ) using VSD Squadron mini .
  
  # Principle :
  The system uses a microcontroller to simulate basic flip‑flop circuits. It reads which flip‑flop mode to use (SR, JK, T, or D) through dedicated selection buttons and shows the selected mode using indicator LEDs. Two additional buttons provide binary input values. The microcontroller processes these inputs using the logic of the selected flip‑flop—setting, resetting, toggling, or directly assigning the output state (Q). The result is then shown on two output LEDs (one displaying Q and the other its inverse, ~Q), while extra LEDs indicate which input buttons are active. Essentially, the project combines user inputs and simple digital logic to mimic the behavior of flip‑flops, with visual feedback provided by LEDs.
  <hr>
   <h4>Program :</h4> 

  ```c //
#include <ch32v00x.h>
#include <debug.h>

// -------------------- Pin Definitions --------------------
// Flip-Flop Selection Buttons (active low)
#define BTN_SR   GPIO_Pin_0  // SR flip-flop select
#define BTN_JK   GPIO_Pin_1  // JK flip-flop select
#define BTN_T    GPIO_Pin_2  // T flip-flop select
#define BTN_D    GPIO_Pin_3  // D flip-flop select

// Input Buttons (active low)
#define BTN_IN1  GPIO_Pin_4  // Input for S/J/T/D
#define BTN_IN2  GPIO_Pin_5  // Input for R/K (used for SR/JK)

// Input Indicator LEDs on Port D (active high)
#define LED_IN1  GPIO_Pin_6  // Indicates BTN_IN1 pressed
#define LED_IN2  GPIO_Pin_7  // Indicates BTN_IN2 pressed

// Output LEDs on Port C (active high)
#define LED_OUT1 GPIO_Pin_0  // Displays Q
#define LED_OUT2 GPIO_Pin_1  // Displays ¬Q

// Selection Indicator LEDs on Port C (active high)
#define LED_SEL_SR GPIO_Pin_2  // Indicates SR flip-flop selected
#define LED_SEL_JK GPIO_Pin_3  // Indicates JK flip-flop selected
#define LED_SEL_T  GPIO_Pin_4  // Indicates T flip-flop selected
#define LED_SEL_D  GPIO_Pin_5  // Indicates D flip-flop selected

// Flip-Flop Type Enumeration
typedef enum {
    FF_NONE = 0,
    FF_SR,
    FF_JK,
    FF_T,
    FF_D
} FlipFlopType;

// Global Variables
volatile FlipFlopType selectedFF = FF_SR;  // Default flip-flop is SR
volatile uint8_t Q = 0;  // Holds the current flip-flop output

// -------------- Function Prototypes --------------
void GPIO_Config(void);
uint8_t ReadButton(GPIO_TypeDef* port, uint16_t pin);
void SetLED(GPIO_TypeDef* port, uint16_t pin, uint8_t state);
void ProcessFlipFlop(FlipFlopType ffType, uint8_t in1, uint8_t in2);
void UpdateOutputLEDs(uint8_t Q);
void ShowSelectedFF(FlipFlopType ffType);
void Delay_Ms(uint32_t ms);  // Using framework's delay function
void Delay_Init(void);       // Using framework's delay function

// ------------------- Exception Handlers -------------------
void NMI_Handler(void) __attribute__((interrupt("WCH-Interrupt-fast")));
void HardFault_Handler(void) __attribute__((interrupt("WCH-Interrupt-fast")));
void NMI_Handler(void) {}
void HardFault_Handler(void) { while(1); }

// ---------------- GPIO Configuration ---------------
void GPIO_Config(void)
{
    GPIO_InitTypeDef GPIO_InitStructure = {0};

    // Enable clocks for Port D and Port C
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE);
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC, ENABLE);

    // Configure selection and input buttons (Port D) as input with pull-up
    GPIO_InitStructure.GPIO_Pin = BTN_SR | BTN_JK | BTN_T | BTN_D | BTN_IN1 | BTN_IN2;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU;
    GPIO_Init(GPIOD, &GPIO_InitStructure);

    // Configure input indicator LEDs (Port D) as output push-pull
    GPIO_InitStructure.GPIO_Pin = LED_IN1 | LED_IN2;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOD, &GPIO_InitStructure);

    // Configure output LEDs (Port C) as output push-pull
    GPIO_InitStructure.GPIO_Pin = LED_OUT1 | LED_OUT2;
    GPIO_Init(GPIOC, &GPIO_InitStructure);

    // Configure selection indicator LEDs (Port C) as output push-pull
    GPIO_InitStructure.GPIO_Pin = LED_SEL_SR | LED_SEL_JK | LED_SEL_T | LED_SEL_D;
    GPIO_Init(GPIOC, &GPIO_InitStructure);
}

// ----------- Read Button State (Active Low) -----------
uint8_t ReadButton(GPIO_TypeDef* port, uint16_t pin)
{
    return (GPIO_ReadInputDataBit(port, pin) == Bit_RESET) ? 1 : 0;
}

// ----------------- LED Control -----------------
void SetLED(GPIO_TypeDef* port, uint16_t pin, uint8_t state)
{
    if(state)
        GPIO_WriteBit(port, pin, Bit_SET);
    else
        GPIO_WriteBit(port, pin, Bit_RESET);
}

// ---------------- Flip-Flop Logic --------------
void ProcessFlipFlop(FlipFlopType ffType, uint8_t in1, uint8_t in2)
{
    switch(ffType)
    {
        case FF_SR:
            if(in1 && !in2)
                Q = 1;
            else if(!in1 && in2)
                Q = 0;
			else if(in1 && in2)
			    Q=!Q;	
            break;
        case FF_JK:
            if(in1 == 0 && in2 == 0) { }
            else if(in1 && !in2) { Q = 1; }
            else if(!in1 && in2) { Q = 0; }
            else if(in1 && in2) { Q = !Q; }
            break;
        case FF_T:
            if(in1)
                Q = !Q;
            break;
        case FF_D:
            Q = in1;
            break;
        default:
            break;
    }
}

// ------------- Update Output LEDs --------------
void UpdateOutputLEDs(uint8_t Q)
{
    SetLED(GPIOC, LED_OUT1, Q);
    SetLED(GPIOC, LED_OUT2, !Q);
}

// --- Show Selected Flip-Flop Indicator LED ---
void ShowSelectedFF(FlipFlopType ffType)
{
    SetLED(GPIOC, LED_SEL_SR, 0);
    SetLED(GPIOC, LED_SEL_JK, 0);
    SetLED(GPIOC, LED_SEL_T, 0);
    SetLED(GPIOC, LED_SEL_D, 0);

    switch(ffType)
    {
        case FF_SR: SetLED(GPIOC, LED_SEL_SR, 1); break;
        case FF_JK: SetLED(GPIOC, LED_SEL_JK, 1); break;
        case FF_T:  SetLED(GPIOC, LED_SEL_T, 1); break;
        case FF_D:  SetLED(GPIOC, LED_SEL_D, 1); break;
        default: break;
    }
}

// ------------------- Main ----------------------
int main(void)
{
    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_1);
    SystemCoreClockUpdate();
    Delay_Init();  // Use framework's delay initialization
    GPIO_Config();

    // Set default state and selection
    selectedFF = FF_SR;
    Q = 0;
    SetLED(GPIOD, LED_IN1 | LED_IN2, 0);
    SetLED(GPIOC, LED_OUT1 | LED_OUT2 | LED_SEL_SR | LED_SEL_JK | LED_SEL_T | LED_SEL_D, 0);
    ShowSelectedFF(selectedFF);

    while(1)
    {
        if(ReadButton(GPIOD, BTN_SR)) { selectedFF = FF_SR; }
        else if(ReadButton(GPIOD, BTN_JK)) { selectedFF = FF_JK; }
        else if(ReadButton(GPIOD, BTN_T)) { selectedFF = FF_T; }
        else if(ReadButton(GPIOD, BTN_D)) { selectedFF = FF_D; }
        
        ShowSelectedFF(selectedFF);

        uint8_t in1 = ReadButton(GPIOD, BTN_IN1);
        uint8_t in2 = (selectedFF == FF_SR || selectedFF == FF_JK) ? ReadButton(GPIOD, BTN_IN2) : 0;
        SetLED(GPIOD, LED_IN1, in1);
        SetLED(GPIOD, LED_IN2, in2);

        ProcessFlipFlop(selectedFF, in1, in2);
        UpdateOutputLEDs(Q);

        Delay_Ms(100);
    }
}

 ```



#### * CIRCUIT CONNECTIONS * 
<details>
  <br>



![CIRCUIT CONNECTIONS](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/flip_flops_using_vsd_squadron_mini.png)
</details>

#### * IMAGE 1 * 
<details>
  <br>



![IMAGE 1](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/TASK6_1.jpeg)
</details>

#### * IMAGE 2 * 
<details>
  <br>



![IMAGE 2](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/TASK6_2.jpeg)
</details>

#### * IMAGE 3 * 
<details>
  <br>



![IMAGE 3](https://github.com/rvijay333/RISC-V-Talent-Development-Program/blob/main/TASK6_3.jpeg)
</details>


[VIDEO LINK](https://drive.google.com/file/d/1s8N6XZwIr4PlNXRCMQaYny9uJnWqKaPh/view?usp=sharing)
</details>
<hr>

_ _ _
