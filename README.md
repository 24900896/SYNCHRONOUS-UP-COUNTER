**NAME:SANDEEP**

**REG NO:24900896**

**EX:7**

**IMPLEMENTATION OF SYNCHRONOUS UP COUNTER USING VERILOG HDL CODE**

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* 1.Type the Verilog program in Quartus Prime to implement the 4-bit synchronous up
counter.
2.Compile and run the program to ensure there are no syntax or logical errors.
3.Generate the RTL schematic to visualize the structure of the synchronous counter and
verify the design logic.
4.Create nodes for the clock (CLK), reset, and counter outputs (Q3, Q2, Q1, Q0) to
observe the counting process.
5.Simulate the design for multiple clock cycles and observe the timing diagrams to
confirm that the counter increments its value synchronously at each clock pulse.
*/

**PROGRAM**

![image](https://github.com/user-attachments/assets/06d69d11-c085-4f94-beae-03e241aad012)

**RTL LOGIC UP COUNTER**

![image](https://github.com/user-attachments/assets/52f2c5d1-1c03-4bbd-b124-af5d9f3ccd07)

**TIMING DIAGRAM FOR IP COUNTER**

![999](https://github.com/user-attachments/assets/488c160b-1aa1-42e9-96f3-c1f498516b11)

**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/0300bca0-eae7-4568-8381-49c604010f26)

**RESULTS**
Thus, the 4-bit synchronous up counter was successfully implemented, and its
functionality was validated through simulation. The counter incremented correctly with
each clock pulse, as verified by the truth table and timing diagrams.
