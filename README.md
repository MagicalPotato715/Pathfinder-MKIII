
 ****PATHFINDER: MARK III****

-----

About: This is the PCB for the third generation of my project, Pathfinder. The goal for Pathfinder is to make a hexapod walking robot that is able to traverse in diverse and rugged terrain where conventional vehicles (e.g., cars, rovers) prove inefficient. The third generation of Pathfinder (Mark III) will feature significant upgrades from its predecessor (Mark II), including improved motors for speed and weight-bearing, an onboard 7.4V LiPo battery for tetherless power, an accelerometer, and an NRF chip for wireless communication.

Why: I began Pathfinder after my physics teacher encouraged me to join my school's science fair. I had always had an idea for a spider robot that I kept at the back of my mind, but this pushed me to bring it to life. Over the next few weeks, I poured hours every day into learning more about mechanical and electrical engineering. I also sought mentorship from the UC Berkeley Engineering Department and got connected with a Mech E & EECS graduate student.  Mark I of Pathfinder, a simple prototype/proof of concept, was churned out after 2 weeks, just in time for my district's science fair to win me 2nd place. Mark II was developed a few weeks later for the regional science fair. Mark III, the model this PCB is for, will be the culmination of my work over an entire year to be entered into next season's science fair.

(Note: The CAD model was created and fine-tuned over the course 3+ months that were before Highway began, so I didn't record the process in the journals.)

---

**In Depth: How It Works** (for all yall nerds out there)

- **PCB**
  - The PCB is, in essence, a servo driver. It is supposed to be placed on top of a Nucleo F446RE board, taking advantage of its Morpho pins that expose the MCU. The power comes in from a 7.4V 2S LiPo battery connected to the onboard XT60 (just a connector).
  - **Servos** Since the potential ampage could go up to ~10-15A, a pour is used to connect the battery to the 3 buck converters. Each buck converter steps down the battery power from 7.4V to 6V at 5A for 6 servos (two legs). This connection from the buck converters to the servo rails is led by another set of pours. The servos receive PWM input from 15 pins on the right morpho pins and 3 on the left.
  - **Power** The VIN from the XT60 is also connected to the F446RE's onboard VIN pin (it already has a regulator to step down to 3.3V). This power then comes out of the 3.3V pin and is fed to the NRF Chip and the Accelerometer.
  - **Accelerometer** The accelerometer used is the BNO055, an "INTELLIGENT ABSOLUTE ORIENTATION SENSOR, 9-AXIS SENSOR FUSION" (aka gyroscope & accelerometer and prob 9 other things). The BNO055 uses I2C and is connected to SDA & SCL. There is also a manual reset button connected to RST on the BNO055 just for funsies.
  - **NRF Chip** This is going to be used to communicate with the hand-held controller (to be made later). The NRF Chip is the NRF24L01_Breakout. NRF24L01_Breakout uses SPI and thus the MISO, MOSI, CSN, SCK, and CE pins on the F446RE (used on the left morpho pins).
  
- **Body**
  In-depth desc WIP
---

<img width="582" alt="Screenshot 2025-07-08 at 11 14 32 AM" src="https://github.com/user-attachments/assets/6af9664e-34e3-4e4b-9147-ffd7b350b66f" />

<img width="839" alt="Screenshot 2025-07-08 at 11 05 50 AM" src="https://github.com/user-attachments/assets/50314f48-1d56-455b-9535-cbf208bb406e" />

<img width="490" alt="Screenshot 2025-07-08 at 11 06 36 AM" src="https://github.com/user-attachments/assets/ebce3c79-0d38-490b-83f8-eb5f56c57008" />

<img width="820" alt="Screenshot_2025-05-13_at_6 30 04_PM" src="https://github.com/user-attachments/assets/9e708280-c7e5-4113-b357-b55002ef5db7" />

|Component|Quantity|Model|Lowest Price|Link|
|---|---|---|---|---|
|LED|2|VLMR233T2V2-GS08|$0.35|[Link](https://www.aliexpress.com/item/1005008128628087.html?spm=a2g0o.productlist.main.1.3248724bxQyiaJ&algo_pvid=fe447d84-fd13-4e27-8b43-c86227a91054&algo_exp_id=fe447d84-fd13-4e27-8b43-c86227a91054-0&pdp_ext_f=%7B%22order%22%3A%22-1%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.35%210.35%21%21%212.50%212.50%21%40212e520f17525897623118806eb6dd%2112000043902875398%21sea%21TW%216187826129%21ABX&curPageLogUid=l7TbgfaGIsM2&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|Button|2 (1x20pcs)|TL1240NQ1JBLK|$1.27|[Link](https://www.aliexpress.com/item/1005003938985112.html?spm=a2g0o.productlist.main.1.4ec72c6f97uelG&algo_pvid=776e63b0-ad1a-4770-b3bd-8e8a47c59f00&algo_exp_id=776e63b0-ad1a-4770-b3bd-8e8a47c59f00-0&pdp_ext_f=%7B%22order%22%3A%22467%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%212.54%211.27%21%21%212.54%211.27%21%402140f54217525901711175058e53bd%2112000027515313621%21sea%21TW%216187826129%21ABX&curPageLogUid=cPSFccWMC2Xx&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|Servo Motor|18 (5x4pcs)|MG996R|$6.9|[Link](https://www.aliexpress.com/item/1005007032811340.html?spm=a2g0o.productlist.main.1.723942Xa42Xahr&algo_pvid=9b9e645d-9469-4d2a-b561-26204b6bf4cc&algo_exp_id=9b9e645d-9469-4d2a-b561-26204b6bf4cc-0&pdp_ext_f=%7B%22order%22%3A%22876%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21TWD%21150.51%21105.30%21%21%214.96%213.47%21%40212a70c017525889078702858e6fc3%2112000039159590615%21sea%21TW%216187826129%21ABX&curPageLogUid=3yZqtCc75vJ0&utparam-url=scene%3Asearch%7Cquery_from%3A#nav-review)|
|10uF Capacitor|7 (1x100pcs)|0805W106K250CC|$0.6|[Link](https://www.aliexpress.com/item/1626652703.html?spm=a2g0o.productlist.main.1.48fb6316RMeZBk&algo_pvid=e693861e-0391-4f51-8de6-32cd16f941e8&algo_exp_id=e693861e-0391-4f51-8de6-32cd16f941e8-0&pdp_ext_f=%7B%22order%22%3A%22290%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.60%210.60%21%21%210.60%210.60%21%402102f22c17525900041745529e7ed1%2165044401121%21sea%21TW%216187826129%21ABX&curPageLogUid=cULtsx9Twjzu&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|10k Resistor|5 (1x100pcs)|CR0805-JW-103ELF|$0.35|[Link](https://www.aliexpress.com/item/1005006269805332.html?spm=a2g0o.productlist.main.1.31e33be6PMcjLK&algo_pvid=54fac39b-245b-4873-a9c8-e36e2fd5a510&algo_exp_id=54fac39b-245b-4873-a9c8-e36e2fd5a510-0&pdp_ext_f=%7B%22order%22%3A%22883%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.46%210.35%21%21%213.30%212.51%21%40212e532617525903439675817ef045%2112000036544486825%21sea%21TW%216187826129%21ABX&curPageLogUid=AMuzMQYTT7uu&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|500 Resistor|2 (1x100pcs)|CR0805-FX-4990ELF|$0.35|[Link](https://www.aliexpress.com/item/1005006269805332.html?spm=a2g0o.productlist.main.2.1d257f6fZB1phL&aem_p4p_detail=202507150740589457957524426840000094648&algo_pvid=39ad91cb-3682-4b56-ba16-048ebdbe6b9a&algo_exp_id=39ad91cb-3682-4b56-ba16-048ebdbe6b9a-1&pdp_ext_f=%7B%22order%22%3A%22883%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.46%210.35%21%21%213.30%212.51%21%402102f0c917525904583394282ef078%2112000036544486825%21sea%21TW%216187826129%21ABX&curPageLogUid=TxMcy0VHgfnU&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=202507150740589457957524426840000094648_1)|
|NRF Board|1|NRF24L01_Breakout|$0.58|[Link](https://www.aliexpress.com/item/1005005642753224.html?spm=a2g0o.productlist.main.5.4aff40c4RsUgXs&algo_pvid=a47926ac-95d7-409f-a2e3-a6df124167e6&algo_exp_id=a47926ac-95d7-409f-a2e3-a6df124167e6-4&pdp_ext_f=%7B%22order%22%3A%22409%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.73%210.58%21%21%210.73%210.58%21%40212e532617525905225245131ef08b%2112000033857271479%21sea%21TW%216187826129%21ABX&curPageLogUid=S6MbdsWU3KA5&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|Schottky Resistor|3 (1x10pcs)|MBR1045S|$2.1|[Link](https://www.aliexpress.com/item/1005007449896177.html?spm=a2g0o.productlist.main.1.18f4590dj3cxnX&algo_pvid=86db1fb7-5252-4c6d-83fd-b3bd29ae29d4&algo_exp_id=86db1fb7-5252-4c6d-83fd-b3bd29ae29d4-0&pdp_ext_f=%7B%22order%22%3A%22-1%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%212.10%212.10%21%21%2115.00%2115.00%21%402141122217525905785477306e7a9b%2112000040801110649%21sea%21TW%216187826129%21ABX&curPageLogUid=bN9sxmJgOcgS&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|Buck Converter|3 (1x5pcs)|RT8289GSP|$2.26|[Link](https://www.aliexpress.com/item/1005006319216009.html?spm=a2g0o.productlist.main.1.488d7bbflR8Hqu&algo_pvid=5c03986f-db2c-4932-8ac0-08d611764161&algo_exp_id=5c03986f-db2c-4932-8ac0-08d611764161-0&pdp_ext_f=%7B%22order%22%3A%223%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%212.40%212.26%21%21%2117.10%2116.07%21%402102f0cc17525907096627257e531b%2112000036745251401%21sea%21TW%216187826129%21ABX&curPageLogUid=wGhDPPpYZM8X&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|47uF Capacitor|6 (1x10pcs)|6TAB47M|$4.38|[Link](https://www.aliexpress.com/item/1005007643113867.html?spm=a2g0o.productlist.main.4.3db3rvLnrvLnvG&algo_pvid=82d2b297-2ddc-4624-9069-19ffb25af219&algo_exp_id=82d2b297-2ddc-4624-9069-19ffb25af219-3&pdp_ext_f=%7B%22order%22%3A%22-1%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%214.38%214.38%21%21%2131.27%2131.27%21%402140f53817525908036584702e4b36%2112000041630471825%21sea%21TW%216187826129%21ABX&curPageLogUid=b2OKnqTq9Hd5&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|38k Resistor|3 (1x100pcs)|CR0805-FX-3832ELF|$0.35|[Link]([https://www.digikey.tw/en/products/detail/bourns-inc/CR0805-FX-3832ELF/3784908](https://www.aliexpress.com/item/1005006269805332.html?spm=a2g0o.productlist.main.1.2d99e8a9Y1xpCE&algo_pvid=5cdcca38-1b66-4097-a40b-18c0ca8f6b01&algo_exp_id=5cdcca38-1b66-4097-a40b-18c0ca8f6b01-0&pdp_ext_f=%7B%22order%22%3A%22883%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.46%210.35%21%21%213.30%212.51%21%400b1bf20817525912714461950e34dc%2112000036544486825%21sea%21TW%216187826129%21ABX&curPageLogUid=isIKNlrJEL5x&utparam-url=scene%3Asearch%7Cquery_from%3A))|
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



