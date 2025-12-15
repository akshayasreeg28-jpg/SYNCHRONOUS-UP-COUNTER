### SYNCHRONOUS-UP-COUNTER

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
1.Open Quartus Prime software.
2. Create a new project using New Project Wizard.
3. Select Empty Project and choose device.
4. Create a new Verilog HDL file.
5. Write the up counter and dowm counter code.
6. Save file and set as top-level entity.
7. Compile the project to verify errors.
8. Observe output using RTL Viewer / Simulation.



**PROGRAM**
UP COUNTER
module expp6(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule

DOWN COUNTER
module exp6(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule


Developed by:Akshaya Sree G RegisterNumber:25018408


**RTL LOGIC UP COUNTER**
<img width="1920" height="1020" alt="exp6 de" src="https://github.com/user-attachments/assets/4c6f69ff-99dc-4df8-8ad2-f4b1d73504b1" />
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/9a3505cc-25d8-41f4-a05a-7297be94a776" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1920" height="1020" alt="exp 6 1 de" src="https://github.com/user-attachments/assets/5790d1c8-133a-4f02-854f-614502061bac" />
<img width="1920" height="1020" alt="Screenshot 2025-12-15 132925" src="https://github.com/user-attachments/assets/f1d8ca9a-9c3f-4b11-b986-481577f5b96a" />

**TRUTH TABLE**
<img width="673" height="719" alt="image" src="https://github.com/user-attachments/assets/1bfb0873-f4e7-4262-91d3-b64e68914d7c" />

**RESULTS**
 Thus 4 bit synchronous up counter and validate functionality is verified.
