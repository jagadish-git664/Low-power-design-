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

Trepn Profiler:
Multiple cpus used at the same time utilized activity based profiling and limit the frequency and volage and save power using DVFS.

Battery power : battery power switching low and high over period of time , an effective algorithm to clock gate can save dynamic power over period of time there by improving batter performance and battery life . This can result less heat produced and more number of operations can be performed

![image](https://user-images.githubusercontent.com/73343230/127779180-c69928ae-b2e9-407b-b9c4-b9084a0e0483.png)

Running CPU at low power mode:

 ![image](https://user-images.githubusercontent.com/73343230/127779198-30a5fa2e-7cca-4a02-9839-6cb12d9a2717.png)


System level and software activity drive low power device level activity for any low power system 
Low power technique has to show benefit at system level , else the low power technique technique   used may be worth the engineering time spent for the same. 

Shutting down systems when not in use or reduce the voltage dynamically can reduce the power consumption of a system . 



Generic bus essential view of SOC system 
Fundamentals of low power design and power management:

![image](https://user-images.githubusercontent.com/73343230/127779216-0d90e333-3293-43c8-b327-d752213e86d5.png)


Voltage playing primary role in deciding the power of a system. 

Power consumption break down :
Power of a h/w resource is not constant and is purely scenario or mode dependant i.e based on the hardware that is utilized on the particular instant of time , the power utilized changes so in any way the activity of that particual module which is ‘more’ active than other’s helps us compute power in an efficient manner. 
In VLSI the standard power consumption estimation uses acivity based power profiling by dumping VCD files out of Netlist to the measure accurate active dynamic and static power consumption across devices that is in operation . 

![image](https://user-images.githubusercontent.com/73343230/127779238-eb94ac06-e4ad-4b0e-b42e-72fb3b905fe4.png)


Low power design vs Power management :

Module operandi for designing any low power application can be stated as below:

![image](https://user-images.githubusercontent.com/73343230/127779260-f20d87c2-a205-4a6b-821c-206d7e287be7.png)


![image](https://user-images.githubusercontent.com/73343230/127779267-2892ae31-d56e-4f45-8633-33d73018bc3f.png)


![image](https://user-images.githubusercontent.com/73343230/127779270-a5283e42-30a1-4d16-946d-3019b72b24c4.png)



Trying to solve one issue other might be affected. 

![image](https://user-images.githubusercontent.com/73343230/127779293-3a19de11-b768-4269-939d-381f0311cf71.png)

Classical example will be while trying to add more power switches in the design which is used to power the domain when default power domain is shut off , the leakage current by power switch can add significant contributon and while the power switches oprating , the dynamic power of these power switches may be significant contributor. 

Voltage control is the primary means for low power management: 


![image](https://user-images.githubusercontent.com/73343230/127779391-0b2119bf-8191-4260-bb02-af65c953b34e.png)


![image](https://user-images.githubusercontent.com/73343230/127779399-0c8c7ef1-b2e9-4257-919a-56a2e10bbb8c.png)


Multi VDD: Dividing voltage w.r.t frequencies . Dividing higher voltage for higher frequencies and lower voltage for lower frequencies.

MTCMOS power gating: Similar to MultVDD , switching of power or ground using header/footer switches . These switches are having higher vt gate 

![image](https://user-images.githubusercontent.com/73343230/127779411-d5c0335f-d1be-4af2-b066-95e5f5d0f39b.png)


DVS enable to operate the logic w.r.t the frequency and hence power saving.  This can be done by level shifting the output signals. However the down shifting can result in over drive and can damage the gate . 

![image](https://user-images.githubusercontent.com/73343230/127779418-ec339d0f-c404-49e5-99b9-cd232968b7c5.png)


Standby technique can be used to lower the voltage of the state just enough to make sure to retain the state without loosing the data . 
There by saving the power when in idle . 



![image](https://user-images.githubusercontent.com/73343230/127779426-d86bfa81-944f-40cd-8d8e-2d8ce48e5c6c.png)



STATE RETENTION TECHNIQUE AND UPF :
![image](https://user-images.githubusercontent.com/73343230/127779433-f9d640dd-a6ab-44e1-9d4e-ff980855ca89.png)

![image](https://user-images.githubusercontent.com/73343230/127779439-7eee5712-3e88-406d-b2a8-a8dbea442147.png)

Some questionnnere 🥇
![image](https://user-images.githubusercontent.com/73343230/127779443-9a57ac4c-3a36-4304-8fc7-733c9f179a25.png)
![image](https://user-images.githubusercontent.com/73343230/127779459-b995a918-f5f8-4c4a-a800-bc907d0a4b07.png)
![image](https://user-images.githubusercontent.com/73343230/127779466-14064e59-770c-41eb-85be-268edba42730.png)
![image](https://user-images.githubusercontent.com/73343230/127779469-a090f6a1-ee7a-4e0e-9531-77c16983a69e.png)
 
Ans is 2 Clock gating 
 
Answer to this is 3 . 

DAY3

Dynamic power intent verification 
![image](https://user-images.githubusercontent.com/73343230/127779496-d922e3d9-8021-44e2-951e-2dc5f5dd0928.png)


![image](https://user-images.githubusercontent.com/73343230/127779502-cbdb7971-c661-4fef-8f64-53aab70c6195.png)


Power states defined for functional blocks , based on modes , the functional blocks can operate any of the mode for power / performance criteria  . 


Some of the modes :


![image](https://user-images.githubusercontent.com/73343230/127779512-7d7e16eb-f474-4498-9f39-07b1791c9dd1.png)


![image](https://user-images.githubusercontent.com/73343230/127779518-db853f3b-0511-48ff-9289-001909a82321.png)


![image](https://user-images.githubusercontent.com/73343230/127779525-1fe3cdfb-60fb-47e7-8153-4033e7df841c.png)


Transition from one mode to other, need exhaustive verification 

![image](https://user-images.githubusercontent.com/73343230/127779533-933d9261-0815-4675-b0bb-5e39511b7d05.png)


![image](https://user-images.githubusercontent.com/73343230/127779536-3b9ee16b-befa-4f98-8f98-56daa7314559.png)


Taking to next level , for transition from Normal to Stand-By , there are intermediate steps like highlighted below. 
Nomal -> save -> VDD =0.7v -> Stand-By 



![image](https://user-images.githubusercontent.com/73343230/127779542-94f88cca-fa7c-47c5-b57c-d7ca8dd75a95.png)


![image](https://user-images.githubusercontent.com/73343230/127779546-782fa7d2-f7d2-4306-9733-469f8403bdf5.png)


![image](https://user-images.githubusercontent.com/73343230/127779548-128f5cdf-e31e-4ff6-899e-0ce08c11f40e.png)


![image](https://user-images.githubusercontent.com/73343230/127779555-d5f4e439-4b4c-44d8-b4c9-7c6102c223e2.png)


Power analysis is an estimation of power dissipation, both dynamic and static, of the chip in various operating modes. IR drop analysis deals with the chip's current draw and the associated voltage drop across the power grid, power switches, etc. Since gate delay depends greatly on the applied voltage, it is very important to make sure that a sudden current draw does not reduce the voltage and slow down the gate to the point of circuit failure.

Static power analysis is the calculation of leakage power. A cell dissipates leakage power when voltage is applied even if it is not switching. As the process geometry shrinks, leakage power is becoming a greater percentage of a chip's overall power dissipation. It is something that we cannot ignore. Dynamic power consists of power dissipated inside a cell (mostly due to short-circuit current during switching) and power dissipated to charge/discharge net capacitance. Dynamic power is a function of voltage, toggle rate, and net loading.

Static IR drop analysis is a first-order approximation. It uses the total power dissipation to calculate a constant current draw. This current is then multiplied by the equivalent resistance of the power network to arrive at the voltage drop. As we know, a circuit does not draw constant current. Current draw increases when a cell is switching. (See dynamic power above.) When a group of cells is switching at the same time, it draws a lot of current at that moment in time. Dynamic IR drop analysis deals with the voltage drop of these current surges.

For power analysis, each cell's power dissipation has been characterized in the library (.lib) file. For leakage power, the EDA tool simply adds up the leakage power of each cell. (Note: Leakage power is usually state dependent, so there is a bit of work here.) For dynamic power, the EDA tool either estimates net capacitance before P&R or calculates net capacitance after P&R. The designer has to provide the toggle rate. This can be based on educated guess, experience, simulation, or emulation. The accuracy of the power analysis depends directly on the accuracy of net capacitance and toggle rate.

Power analysis must be considered very early in the design cycle. Typically, 80% of a chip's power is determined at the RTL stage. After that, a design team can only impact 20% of the power. Here are some of the questions that a design team should answer at the architectural stage:

- Which voltage supply should we use?
- Can we achieve lower power with more than one voltage supply?
- Do we have inactive blocks that we can shut off to reduce leakage power?
- If we shut off blocks, are there registers that we have to retain the state?
- Do we have blocks that can run at slower rate in certain modes? Can we reduce the voltage during those modes?

![image](https://user-images.githubusercontent.com/73343230/127779568-3d1f7ad2-7eda-44bd-95b2-d075aac82294.png)

![image](https://user-images.githubusercontent.com/73343230/127779573-f029b5a1-21ac-4f99-b549-d321fe0ebdf4.png)

![image](https://user-images.githubusercontent.com/73343230/127779576-1522c11a-514c-48bc-be1b-abc33e2529b1.png)









