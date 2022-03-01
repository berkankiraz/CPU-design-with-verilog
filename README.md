# CPU-design-with-verilog


Calculate arithmetic mean of three 8-bit positive integers, 𝐴, 𝐵 and 𝐶 as 𝐷 = 
(𝐴+𝐵+𝐶)/3. 𝐷 is a 8-bit positive integer.



DESIGN REQUIREMENTS
1) Your TOP module should look exactly like Figure-1. Don't use any other elements or
submodules except these three given submodules.
2) An example Register Block (RB) is given in Figure-2. Just like in this schematic, you should design
your ALU operations as submodules.
3) CU must only contain output registers and state registers, there should be no other registers
within this design.
4) Reset and clock inputs are common for CU and RB. Reset should be designed as asynchronous
active-1.
5) You may use "dont_touch" constraint with your output registers.
6) CU must be a Moore type machine.
7) CU should begin working when "start" signal is high. Then, it will keep "busy" signal high until
the result is calculated.
8) State transition branches in your CU should only use the ALU signals Carry-Out (CO) and Zero
(Z) as branching conditions. ex: if(CO), if(!Z).
9) When designing the ALU, you must use submodules just as given in Figure-3. If you need to use
combinational assignments, use them within AND, XOR, ADD or Shift blocks.
10) RTL's must be consistent with the figures given, thus you must use the exact signal names given
in figures.
11) Your ALU must perform:
 AND, when InsSel == '00',
 XOR, when InsSel == '01',
 ADD, when InsSel == '10',
 Shift, when InsSel == '11'.
For ADD, carry-out bit should be assigned to CO output. Shift should perform a circular left-shift
(MSB will move to LSB), and CO will hold the old MSB. CO should be 0 for AND and XOR
operations. Z signal should be 1 only when the ALU output is zero, will be 0 otherwise. 
