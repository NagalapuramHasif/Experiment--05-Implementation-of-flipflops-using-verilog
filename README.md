![Screenshot 2023-11-26 210428](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/40d36dd0-e6c8-4ff5-94b4-be147a63ce37)![Screenshot 2023-11-26 170739](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/504fe32a-8b20-4a25-a770-ea30b4f91185)# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.


 ![Screenshot 2023-11-26 165020](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/62b45373-c9e0-4e2f-8db1-6ffc8bde7910)

This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![Screenshot 2023-11-26 164934](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/b934cb7d-fb85-4e87-916e-a4f7c5523f71)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-26 164713](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/93f749a0-7e7c-4305-a146-313de6567d6f)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
![OIP](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/729ec212-e4fb-4820-a683-35c67877d6c1)


 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![Screenshot 2023-11-26 204625](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/ddabed5e-a68f-4375-b00d-517d5a887d69)

![Screenshot 2023-11-26 204555](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/fc60be2f-9268-4450-8ddb-ffd0a9fc86d5)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D
![OIP](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/a5644edb-7bc7-4f0e-bc43-fc216529e281)




Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

 ![Screenshot 2023-11-22 142451](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/1fac9377-83ee-4e22-9b0e-fcc47315b0d6)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![Screenshot 2023-11-26 210428](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/9b118dbf-b02b-46e0-867f-7e2563cde17c)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State
 ![Screenshot 2023-11-22 143128](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/676e56d8-d98e-4d66-9ba4-41658c30a204)

 


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
![OIP](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/0a960aee-0529-4672-a860-5dc8b2413453)

 

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![Screenshot 2023-11-26 170613](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/89b958ce-8a76-458c-a2f3-21aa324e4213)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.
![Screenshot 2023-11-26 170739](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/a7ff9365-8ea9-4628-acdb-d5c8e213424b)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State

![Screenshot 2023-11-26 170613](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/878f1c3d-674c-4945-856c-2815754c013d)


![download](https://github.com/NagalapuramHasif/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365567/b9e062a3-3096-4ee1-9df6-afad4d5da80f)


From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 
