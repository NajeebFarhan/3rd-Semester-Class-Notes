# Addressing Mode
The operation field of an instruction specifies the operation to be performed.  
The way operands are chosen during program execution depends on the **addressing mode**.  
An addressing mode specifies the rule for interpreting or modifying the address field of an instruction **before** the operand is actually referenced.

Computers use addressing modes for two main purposes:

1. To give the programmer flexibility by providing facilities such as:
    
    - Pointers to memory
        
    - Counters for loop control
        
    - Indexing of data
        
    - Program relocation
        
2. To reduce the number of bits required in the address field of an instruction.
    

Most addressing modes modify the address field of the instruction.  
There are also two addressing modes that do **not** need an address field:

- **Implied mode**
    
- **Immediate mode**

---
## Implied mode
In this mode, the operand is specified **implicitly**.  
The definition of the instruction itself tells the CPU which operand to use.

For example, the instruction **“Complement Accumulator”** is an implied mode instruction because the operand (the accumulator register) is already implied in the instruction — there’s no need to mention it explicitly.

Zero-address instructions in a **stack-organized computer** are also implied mode instructions, because the operands are implicitly assumed to be on the **top of the stack**.


---
## Immediate mode

In this mode the operand is specified in the instruction itself. in other words an immediate mode instruction has an operand field rather than an address field

--- 
## Register mode

In this mode the operands are in registers that reside within the CPU. The particular register is selected from a register field in an instruction.

---
## Register Indirect mode

In this mode the instruction specifies a register in the CPU whose contents give the address of the operand in memory. In other words the selected register contains the address of the operand rather than the operand itself.

---
## Auto increment and auto decrement mode

This is similar to the register indirect mode except that the register is incremented or decremented after(or before) its value is used to access memory

---
## Direct address mode

In this mode the effective address is equal to the address part of the instruction. The operand reside in memory and its address given directly by the address field of the instruction. 

**_note_**
The effective address is defined to be the memory address obtain from the computation dictated by the given addressing mode. The effective address is the address of the operand in a computational type instruction. It is the address where control branches in response to a branch type instruction.

---
## Indirect address mode

In this mode the address field of the instruction gives the address where the effective address is stored in memory. 
    A few address modes require that the address field of the instruction to be added to the content of a specific register in the CPU. 
	Effective Address = Address part of instruction + content of CPU register

---
## Relative address mode

In this mode the content of the program counter(PC) is added to the address part of the instruction in order to obtain the effective address. 
	Effective address = Program Counter + Address part of the instruction

---
## Index Addressing mode
In this mode the content of an index register is added to the address part of the instruction to obtain the effective address. The index register is a special CPU register that contains an index value.

---
## Base Register Addressing mode
In this mode the content of base register is added to the address part of the instruction to obtain the effective address.

---
**Q.** Find out the effective or calculate the effective address and content of accumulator for the addressing modes: Direct address, immediate mode, indirect address, relative address, index address, register address, register indirect, auto increment, auto decrement address mode
![[IMG_20250811_141346588.jpg|400]]
**Ans:**

| Addressing modes          | Effective address | Content of Accumulator(AC) |
| ------------------------- | ----------------- | -------------------------- |
| Direct Addressing mode    | 500               | 800                        |
| Immediate Addressing mode | 201               | 500                        |
| Indirect Addressing mode  | 800               | 300                        |
| Relative Addressing mode  | 702               | 325                        |
| Index Addressing mode     | 600               | 900                        |
| Register Addressing mode  | -                 | 400                        |
| Register Indirect mode    | 400               | 700                        |
| Auto increment            | 399               | 450                        |
|                           |                   |                            |

**Note on auto increment and auto decrement**:
the auto increment note is the same as the register increment note except that $R1$ is incremented to 401 after the execution of the instruction. 
the auto decrement mode decrements R1 to 399 prior to the execution of the instruction

---
**Q.** An instruction is stored at location 300 with its address field of location 301. The address field of the instruction has the value 250 and processor register contains 200. Evaluate the effective address if addressing mode is direct, immediate, indirect, relative, and register addressing mode.


\* The next instruction to be located is at 302

---
**Q.** A relative branch mode type of instruction is stored in memory at address 300, the branch is made to an address 450.
a) what should be the value of relative address 
b) Determine the value of PC before the instruction fetch and after fetch, and after the execution.



Q) A relative branch mode type instruction has taken branch to an address 750. The branch instruction is of 4 bytes and it has relative address value(offset value) 400. Then what is the starting address of the instruction in memory? Assume that the system has byte addressable memory organisation.