About: This is the PCB for the third generation of my project, Pathfinder. The goal for Pathfinder is to make a hexapod walking robot that is able to traverse in diverse and rugged terrain where conventional vehicles (e.g., cars, rovers) prove inefficient. The third generation of Pathfinder (Mark III) will feature significant upgrades from its predecessor (Mark II), including improved motors for speed and weight-bearing, an onboard 7.4V LiPo battery for tetherless power, an accelerometer, and an NRF chip for wireless communication.

Why: I began Pathfinder after my physics teacher encouraged me to join my school's science fair. I had always had an idea for a spider robot that I kept at the back of my mind, but this pushed me to bring it to life. Over the next few weeks, I poured hours every day into learning more about mechanical and electrical engineering. I also sought mentorship from the UC Berkeley Engineering Department and got connected with a Mech E & EECS graduate student.  Mark I of Pathfinder, a simple prototype/proof of concept, was churned out after 2 weeks, just in time for my district's science fair to win me 2nd place. Mark II was developed a few weeks later for the regional science fair. Mark III, the model this PCB is for, will be the culmination of my work over an entire year to be entered into next season's science fair.

(Note: The CAD model was created and fine-tuned over the course 3+ months that were before Highway began, so I didn't record the process in the journals.)

---

**In Depth: How It Works** (for all yall nerds out there)

- **PCB**
  The PCB is, in essence, a servo driver. It is supposed to be placed on top of a Nucleo F446RE board, taking advantage of its Morpho pins that expose the MCU.
- **Body**
  In depth desc WIP
---

<img width="582" alt="Screenshot 2025-07-08 at 11 14 32 AM" src="https://github.com/user-attachments/assets/6af9664e-34e3-4e4b-9147-ffd7b350b66f" />

<img width="839" alt="Screenshot 2025-07-08 at 11 05 50 AM" src="https://github.com/user-attachments/assets/50314f48-1d56-455b-9535-cbf208bb406e" />

<img width="490" alt="Screenshot 2025-07-08 at 11 06 36 AM" src="https://github.com/user-attachments/assets/ebce3c79-0d38-490b-83f8-eb5f56c57008" />

<img width="820" alt="Screenshot_2025-05-13_at_6 30 04_PM" src="https://github.com/user-attachments/assets/9e708280-c7e5-4113-b357-b55002ef5db7" />

|Component|Quantity|Model|Lowest Price (unit)|Link|
|---|---|---|---|---|
|LED|2|VLMR233T2V2-GS08|$0.51|[Link](https://www.digikey.tw/en/products/detail/vishay-semiconductor-opto-division/VLMR233T2V2-GS08/3025490)|
|Button|2|TL1240NQ1JBLK|$0.98|[Link](https://www.digikey.tw/en/products/detail/e-switch/TL1240NQ1JBLK/1805479)|
|Servo Motor|18|MG996R|$4.2|[Link](https://tw.shp.ee/tT3prQu)|
|10uF Capacitor|7|0805W106K250CC|$0.04|[Link](https://tw.shp.ee/vY3ZYgh)|
|10k Resistor|5|CR0805-JW-103ELF|$0.1|[Link](https://www.digikey.tw/en/products/detail/bourns-inc/CR0805-JW-103ELF/3593155)|
|500 Resistor|2|CR0805-FX-4990ELF|$0.1|[Link](https://www.digikey.tw/en/products/detail/bourns-inc/CR0805-FX-4990ELF/3784987?s=N4IgjCBcpgnAHLKoDGUBmBDANgZwKYA0IA9lANogAMIAugL7EBMV8ArMiGpFnkaRRAAWWLAAEAeQAWAW1x1iABwAuUEAFUAdgEtlE9AFl8mXAFcATvhCMQAWiGduvAsTKRKAZjZgPTEMQ8RJj8GenogA)|
|NRF Board|1|NRF24L01_Breakout|$1|[Link](https://tw.shp.ee/tFocrzP)|
|Schottky Resistor|3|MBR1045S|$1.07|[Link](https://www.digikey.tw/en/products/detail/smc-diode-solutions/MBR1045S/5993230?s=N4IgTCBcDaILICEBKBGADAFgKwGUQF0BfIA)|
|Buck Converter|3|RT8289GSP|$4.11|[Link](https://www.digikey.tw/en/products/detail/richtek-usa-inc/RT8289GSP/2546068?s=N4IgTCBcDaIEoBUAcYkE4QF0C%2BQ)|
|47uF Capacitor|6|6TAB47M|$1.66|[Link](https://www.digikey.tw/en/products/detail/panasonic-electronic-components/6TAB47M/4833040?s=N4IgjCBcpgnAHLKoDGUBmBDANgZwKYA0IA9lANogAMIAugL7EBMVALEtCGpFnkaRRCsA7AAIArQDE6xAA4AXKCACqAOwCW8gPLoAsvky4ArgCd8IRiBbCOqDDgLEykSgDYAdAGZRANRkgFJTVNHX1DU3N6SyZBAAUtAGUAYQBBWLp6IA)|
|38k Resistor|3|CR0805-FX-3832ELF|$0.1|[Link](https://www.digikey.tw/en/products/detail/bourns-inc/CR0805-FX-3832ELF/3784908)|
|Developement Board|1|Nucleo F446RE|$14.85|[Link](https://www.digikey.tw/en/products/detail/stmicroelectronics/NUCLEO-F446RE/5347712)|
|10uH Inductor|3|EXL1V0505-100-R|$0.69|[Link](https://www.digikey.tw/en/products/detail/eaton-electronics-division/EXL1V0505-100-R/13912336)|
|XT60 Connector|1|XT60-F|$1.57|[Link](https://tw.shp.ee/Gx2Y8iE)|
|0.1uF Capacitor|3|0603B104K250SD|$1.7|[Link](https://tw.shp.ee/weARm6H)|
|Accelerometer|1|BNO055|$38.46|[Link](https://tw.shp.ee/19Ezxnb)|
|Female Headers|2|PPPC192LFBN-RC|~2.05|[Link](https://www.digikey.tw/en/products/detail/sullins-connector-solutions/PPPC192LFBN-RC/810258)|
|Male Headers|18|TS-103-G-A|$1.27|[Link](https://www.digikey.tw/en/products/detail/samtec-inc/TS-103-G-A/1105459)|
|PCB Board|1| |$101.71|JLCPCB Order|

Total Components Price: ~$195.17
PCB Price: $101.71
Total Price: ~$297.08



