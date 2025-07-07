---
title: Pathfinder Mark-III
author: Calvin Hung
description: This project is the PCB for the third edition of my hexapod Pathfinder for the science fair. It will be a significant upgrade from Mk-II, having significantly stronger motors a complex buck converter power control. Additionally, I also want it to feature remote control, and a good inverse kinematics system so that I won't have to hard code in movements.
created_at: 6/18/25
---

# June 18th: Finished the Box Plot

I finally finalized my box plot for the PCB! It's kind of heavily inspired by Aecert Robotics' design, but I got rid of the pressure sensors because I don't see a point in them. Also I'm going to use the Bno055 as the gyro because the one Aecert uses is kind of bad :/.

<img width="572" alt="Screenshot 2025-07-07 at 8 25 38 PM" src="https://github.com/user-attachments/assets/f1a7d65b-e78a-4c17-b261-9371db5360fe" />


**Total time spent: 4hrs**

# June 20th: Made first Schematic :D

The box plot makes wiring so easy! Passives like capacitors are annoying tho (but that's what chatgpt is for). Good thing that datasheets give circuit diagrams though! However, there's a bunch of ERC errors and I don't think the nucleo footprint has nearly enough pins? Finding symbols/footprints was a massive pain too. For example, for stuff like the passives, I kinda don't know what footprint to use because theres so many and I don't want to use the wrong one! Also, for things like the Bno055, all I could find on the internet were symbols of the chip itself - not the breakout board. I ended up having to make my own symbol.

<img width="1082" alt="Screenshot_2025-06-24_at_11 07 03_PM" src="https://github.com/user-attachments/assets/3bae7356-b103-473b-afa5-5decb9b242e3" />

**Total time spent: 3hrs**

# June 25th: Finally fixed my schematic ugh -_-

I finally found the rest of the nucleo footprint(s)! Turns out, theres like 6 diff parts. Although, I'm only using the two that have morpho pins XD. Also thought to clean up the space a little. The buck converter passive circuit was becoming confusing so I just wired it. The servo motor array is the bane of my existence - so annoying to rearrange. A really annoying thing is, each pin has like 5 diff purposes and I can't find any concrete "this pin does specifically PWM/UART/I2C". Despite that, I CAN FINALLY START MAKING THE LAYOUT.

<img width="1046" alt="Screenshot_2025-06-25_at_12 31 23_PM" src="https://github.com/user-attachments/assets/59ac825f-eb48-463f-bfe0-ce90e300f034" />

**Total time spent: 5hrs**

# June 26th: Layout Designing go brrr (SO MANY ERRRORRRRRRSSSSSSS UGHHHH)

The buck converters' passives are sooooo annooyyyiinnnngggggggg. I have to place so many thing so many times. I'm also starting to realize I might not have enough space (maybe it was a bad idea to use chatgpt to find footprints). I'm going to use something like Digikey to find new footprints for everything. Also, the servo --> PWM connections are all over the place (rearranging them is going to be a painnnnnnnn). I genuinely don't think I have enough space for the PCA servo driver Lol. Also, I don't know how to route power because 15 amps is a lot and my trace calculator said it has to be 300 mils...

<img width="927" alt="Screenshot_2025-07-02_at_9 47 05_AM" src="https://github.com/user-attachments/assets/cc634401-a90a-4673-a0dc-f33dd773e183" />

**Total time spent: 3hrs**

# June 27th: Layout Designing go brrr - Take 2

I finally got a more optimized power system!!! Also I found a way to fit everything on the board. Turns out that the footprints that ChatGPT gave me were wayyyy too big to fit. However, I do think that I'm placing things a little close together (in order to fit everything on the board) that there might be like heat interference or smth. Routing is going to be fun!

<img width="826" alt="Screenshot_2025-07-02_at_11 01 49_AM" src="https://github.com/user-attachments/assets/dada1fe8-7ed5-4fbd-a892-f8bbf458a097" />

**Total time spent: 5hrs**

# June 30th: Layout Designing go brrr (fml)

I HATE DRC. IT TEARS APART MY HOPES AND DREAMS. Routing was fun while it lasted, but there. were. so. many. errors.............. I feel like I don't know how big I should make the buck converter traces. My calculator said that they need to be crazy wide (which cannot fit on the VERY small space that I have), but ChatGPT (that I kind of don't trust anymore) reassured me that the short length of the traces would negate damage or something.(Also, I realized I can use pours for the power :O)

<img width="749" alt="Screenshot_2025-07-03_at_10 24 26_AM" src="https://github.com/user-attachments/assets/14aca771-5550-44d0-b59d-7329b6645e56" />
<img width="236" alt="Screenshot_2025-07-02_at_12 29 06_PM" src="https://github.com/user-attachments/assets/287e91bc-00f9-4fa6-979b-e4d407f52030" />

**Total time spent (READ:wasted): 6hrs**

# July 1st: :DDDDDDDDDD FINALLY I'M FREEEEEEEEEEEEEEEEEEEEEEEEE

I went to a cafe and locked in!!! All the DRC errors are now gonnnneeee!!!! I also learned about JLCPCB-specific design rules. However, I'm still concerned on whether the servo voltage pours / vias will be able to carry the current. Prob a few tweaks left, but almost done!

<img width="703" alt="Screenshot_2025-07-03_at_11 26 27_AM" src="https://github.com/user-attachments/assets/d18a839c-7b6f-4bdb-a333-9967df85c84c" />

<img width="244" alt="Screenshot_2025-07-03_at_11 26 54_AM" src="https://github.com/user-attachments/assets/5a576a7e-a9e5-469d-961a-32a098bf0299" />


**Total time spent: 2hrs**

# July 7th: I'M DONE

I think I'm ready. I'm confident with the board and it's ready to be made!

<img width="1120" alt="Screenshot 2025-07-07 at 8 54 44 PM" src="https://github.com/user-attachments/assets/34777e5a-90c3-456e-aa57-8cf8499f46b6" />
<img width="657" alt="Screenshot 2025-07-07 at 8 55 07 PM" src="https://github.com/user-attachments/assets/5ce31f2a-9d6f-49fb-8723-71501eaa0e66" />


**Total time spent: ~3 hrs**



