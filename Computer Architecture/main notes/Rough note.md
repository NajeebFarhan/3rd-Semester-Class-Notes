# Immediate Mode

In this mode the operand is specified in the instruction itself. in other words an immediate mode instruction has an operand field rather than an address field

# Register Mode

In this mode the operands are in registers that reside within the CPU. The particular register is selected from a register field in an instruction.

# Register Indirect Mode

In this mode the instruction specifies a register in the CPU whose contents give the address of the operand in memory. In other words the selected register contains the address of the operand rather than the operand itself.

# Auto increment and auto decrement mode

This is similar to the register indirect mode except that the register is incremented or decremented after(or before) its value is used to access memory

# Direct address mode

In this mode the effective address is equal to the address part of the instruction. The operand reside in memory and its address given directly by the address field of the instruction. 


**_note_**
The effective address is defined to be the memory address obtain from the computation dictated by the given addressing mode. The effective address is the address of the operand in a computational type instruction. It is the address where control branches in response to a branch type instruction.

# Indirect address mode

In this mode the address field of the instruction gives the address where the effective address is stored in memory. 
    A few address modes require that the address field of the instruction to be added to the content of a specific register in the CPU. 
	Effective Address = Address part of instruction + content of CPU register

# Relative address mode

In this mode the content of the program counter(pc) is added to the address part of the instruction in order to obtain the effective address. 