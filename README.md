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

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: SANTHOSH V

RegisterNumber: 24005918
*/

   module exp11 (out, clk, rstn);
   
  input clk, rstn;
  
   output reg [3:0]out;
   
   always @ (posedge clk)
   
   begin
   
   if(!rstn)
   
   out<=0;
   
   else
   
  out <= out+1;
  
   end
   
  endmodule

**RTL LOGIC UP COUNTER**
![{90FEC478-2F66-434F-9684-DAA519FD7277}](https://github.com/user-attachments/assets/539464ca-8d1f-4159-8f6b-6cd5026165c1)

**TIMING DIAGRAM FOR IP COUNTER**
![{C9F7C501-FBF6-4398-947C-9E84FE10BF7A}](https://github.com/user-attachments/assets/5b4ffa9b-35e0-468c-9d33-1673634c5399)

**TRUTH TABLE**

![{6E425B37-2FC5-44E7-8177-60A38C4E7EB7}](https://github.com/user-attachments/assets/3a70d236-4b21-4813-927e-adf66f9a00c2)

**RESULTS**
            Thus the 4 bit synchronous up counter is implemented correctly and
 program code is successfully executed
