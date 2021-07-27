# Low power design
Low power design workshop 

The major challenge for the VLSI designer is area, performance, cost and power consumption. In Mobile , IOT dommains increasingly power consumption is being given comparable weight to area and speed considerations as these are battery dependant . Today power is the primary focus  for the competing market in IOT era  and success in the field of personal computing devices,  telecommunication  system  which  demand  high  speed  
computation  and  complex  functionality  with  low  power consumption is has been the prime agenda for these markets. The  motivation  for    power  consumption  reduction  differ  from application  to  application.  In  the  class  of  micro-powered  battery-  operated,  portable  applications,  such  as  cellular  phones  and personal digital assistants, 
the goal is to keep the battery lifetime and weight reasonable and low  packaging cost .

Principles covered in this course are:

Low Power Design vs. Power Management
The basic rules of Power Management
Balancing Density-Delivery-Leakage-Lifetime
Connecting software level activity to device level issues
Voltage Aware Boolean Equations for CMOS
Island ordering and how to shutdown/wakeup complex systems
Rules for verifying low power designs




Economics of Power and Energy

 Power has been a second order convern in chip deisgn next to area and timing . Power budget is one of the most  important design goal of the project. Exceeding the budget can be fatal causing poor reliability due to excessive power density or lesser budgeting than expected or failing to meet required battery life .

Below are the use cases where power will be playing crucial role in terms of device cost and performance. 

Performance 
 - Reducing power overall will improve performance.
Cost 
 - Packaging cost is hightly dependant on the power consumption  . The cost associated with packaging and cooling such devices is prohibitive. Since core power 
consumption must be dissipated through the packaging, increasingly expensive packaging and cooling strategies are required as chip power consumption increases. 
Consequently, there is a clear financial advantage to reducing the power consumed in high performance  systems.
 
Weight 
 - Power is a measure of how fast an amount of work is done.
 - Need to carry the energy (Power * Time) you use in case of portable device. 
 - Energy is heavy for power hunger devices  (Wh/lb) .Lower power means less battery weight

Form Facor 
   -The size and physical form factor are often a natural consequence of a system’s intended use.Dependign on type of technology node  used and affect power.

Functionality 
   - how fast your system is performaning.

Context of use 
  - Optimizing power or energy according to the embedded devices /application that we use , 

Comfort/Safety -
  - Heating issue should be considered while designing the circuit.


 Power vs Energy:
 
 For battery operated devices the diffference is ciritcal . 
 
   Power is defined as the instantaneous draw in the device , while energy refers to the total sum of the V * I over a time T. 
   Energy is directly dependant on the battery capacity which in turn directly affects weight and cost of the system.
   
   ![image](https://user-images.githubusercontent.com/73343230/127182801-fc78470e-1fdf-46bf-8cd6-d26c5c257697.png)

It is also useful to look at the impact of Power v Energy :

As inceate in power increase the heat dissipated which in turn ,  the junction temperature . 
The  associated packaging/cooling cost rises and mainly  the frequency gets limited thereby reducing performance .



Comparing Battery:Parameters deciding cost for a battery

![image](https://user-images.githubusercontent.com/73343230/127183793-b5d75a4c-e1f0-4d7e-8dc9-29935e61a82e.png)


![image](https://user-images.githubusercontent.com/73343230/127184152-cd5175ca-f2f9-4880-9e58-e094f55e2d97.png)


![image](https://user-images.githubusercontent.com/73343230/127184302-1688ea56-0825-45df-9fb2-ea8192168dec.png)


