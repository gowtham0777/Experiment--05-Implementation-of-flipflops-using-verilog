Developed by: GOWTHAM ADITYA R<br>
Refrence number:212223050018

# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.


![image](https://github.com/gowtham0777/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152005396/cd429828-4cb3-4cb7-adc0-c6b011806049)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://github.com/gowtham0777/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152005396/b6d820b0-235b-4498-bdb6-85207abbc261)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State



By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/gowtham0777/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152005396/5c983882-47e0-4d6a-8f16-f89b1a1529ec)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://github.com/gowtham0777/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152005396/f70c256f-30e3-4211-949a-a57072cd27ae)


![image](https://github.com/gowtham0777/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152005396/bb262c5c-eeba-462d-9072-550ca304a3d8)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/gowtham0777/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152005396/dd2af425-dcfe-4e76-8ec0-b65935316d60)

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
1.Using nand gates and wires construct sr flip flop.
2.Repeat same steps to construct JK,D,T flipflops.
3.Find Rtl logic and timing diagram for all flipflops.
4.end the program
### PROGRAM 
~~~
SR Flip-Flop:
module SR_flipflop(S,R,clk,Q,Qbar);
input S,R,clk;
output Q,Qbar;
wire X,Y;
nand (X,S,clk);
nand (Y,R,clk);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule
~~~

D Flip-Flop:
~~~
module D_flipflop(D,clk,Q,Qbar);
input D,clk;
output Q,Qbar;
assign Dbar=~D;
wire X,Y;
nand (X,D,clk);
nand (Y,Dbar,clk);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule
~~~

JK Flip-Flop:
~~~
module JK_flipflop(J,K,clk,Q,Qbar);
input J,K,clk;
output Q,Qbar;
wire X,Y;
nand (X,J,clk,Qbar);
nand (Y,K,clk,Q);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule
~~~

T Flip-Flop:
~~~
module T_flipflopo(T,clk,Q,Qbar);
input T,clk;
output Q,Qbar;
wire S,R;
nand (S,T,clk,Qbar);
nand (R,T,clk,Q);
nand (Q,S,Qbar);
nand (Qbar,R,Q);
endmodule
~~~

### RTL LOGIC FOR FLIPFLOPS 
SR Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/66bcad90-56c9-43b7-8923-a5015e376c95)

D Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/dc522977-8f1a-40a9-830e-fadd93b5fe89)

JK Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/a795e649-2c55-4f47-adce-08629c09bb50)

T Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/7cb4418d-db62-45a8-8e1f-5b2f1d6c8be4)

### TIMING DIGRAMS FOR FLIP FLOPS 
SR Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/aeb143e0-8291-4c23-bb2c-1c3f6fa2081d)

D Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/2d4f2f8c-afd3-4c46-8383-9db8b1733e10)

JK Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/d09b394f-dc3a-480c-b746-4e0d6e449b80)

T Flip-Flop:

![image](https://github.com/23012312/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150009714/a84ed532-662a-498a-abb9-c45a65c31ee4)

### RESULTS 
Thus implementation of SR, JK, D and T flipflops using nand gates are done sucessfully.
