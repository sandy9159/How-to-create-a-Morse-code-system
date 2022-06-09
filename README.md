# How-to-create-a-Morse-code-system

![image](https://user-images.githubusercontent.com/19898602/172843405-e3d7b275-f148-426b-b9fa-4880cd34118d.png)


Morse Code, either of two systems for representing letters of the alphabet, numerals, and punctuation marks by an arrangement of dots, dashes, and spaces. The codes are transmitted as electrical pulses of varied lengths or analogous mechanical or visual signals, such as flashing lights. 

One of the systems was invented in the United States by American artist and inventor Samuel F.B. Morse during the 1830s for electrical telegraphy. This version was further improved by American scientist and businessman Alfred Lewis Vail, Morse’s assistant and partner. 

Soon after its introduction in Europe, it became apparent that the original Morse Code was inadequate for the transmission of much non-English text, since it lacked codes for letters with diacritic marks. 

To remedy this deficiency, a variant called the International Morse Code was devised by a conference of European nations in 1851. This newer code is also called Continental Morse Code.


![image](https://user-images.githubusercontent.com/19898602/172843596-14cdbbd6-1a4a-410b-9663-07e81f905fa0.png)


# Material Required

> 1	10K resistor (R1) 

> 1	22K resistor (R2) 

> 4	100nF capacitor (C1, C3, C5, C6) 

> 2	100uF capacitor (C2, C4) 

> 1	1n4148 diode (D1) 

> 1	1n5817 Schottky diode (D2) 


Morse code has its origins back to the first telegraph as a method for communicating. Since the only data that could be transferred was either the presence of electrical current or not, all letters and numbers were encoded in such a way that all could be interpreted with either a long pulse or short pulse.

In this series of projects, I will show you how to create a Morse code system that you can use to communicate with others at distance! This project will start with the most basic of systems and you will transmit Morse code via a switch and a transmitter/receiver pair.



# Transmitter Schematic


![image](https://user-images.githubusercontent.com/19898602/172843855-d4b7b8c3-0616-46a0-8336-68f1bcae467a.png)


![image](https://user-images.githubusercontent.com/19898602/172845383-6119e6db-fd3f-4795-b499-e440b467a4d7.png)


# Receiver Schematic


![image](https://user-images.githubusercontent.com/19898602/172845495-9ea338a6-7bb5-4c86-8b56-d6b753e4a024.png)


![image](https://user-images.githubusercontent.com/19898602/172846490-8972caab-aed9-4406-a3ed-c6e83faaa043.png)

Before moving fuurther I would like to tell you something about PCB

Yes PCB are the heart of the electronics based project usually we hesitate to try custom PCB and opt to homemade solutions

like breadboard or Zero PCB earlier I also was in the same boat, I hesitate to try custom PCB my belief was they are much expensive.

but then I came to know about [JLCPCB.COM](https://jlcpcb.com/IAT) and I was totally surprised how low price PCB's are they offering 

there PCB quality is best in market, now I always go with PCB for my project and [JLCPCB.COM](https://jlcpcb.com/IAT) is my trusted 

If you planing to order any PCB for your projects so you can consider [JLCPCB.com](https://jlcpcb.com/IAT) because

I always prefer [JLCPCB.com](https://jlcpcb.com/IAT) for my PCB needs, [JLCPCB.com](https://jlcpcb.com/IAT) have best deals for their customers
$2 for 1-4 Layer PCBs, free SMT assembly monthly.

If you seriously need quality PCB quickly in your hand then you must have to try JLCPCB PCB manufacturing service. They have Special offer of $2 for 1-4 Layer PCBs, free SMT assembly monthly. If new user signup today from this link [JLCPCB.com](https://jlcpcb.com/IAT) you will get welcome coupons from JLCPCB.


![image](https://user-images.githubusercontent.com/19898602/159014034-3c9a50c3-61c3-40d2-836d-9cadc2317d33.png)
![image](https://user-images.githubusercontent.com/19898602/164385177-de123350-4a1f-4d0f-9f38-68ed7dbd5a9f.png)



SMT Assembly service of [JLCPCB.com](https://jlcpcb.com/IAT) is cherry on top now get your PCB fully assembled and save your time and money
Select components for your PCB from there Parts Library of 200k+ in-stock components
they are offering $30 valued New User coupons  & $24 SMT coupons every month
$8.00 setup fee, and $0.0017  per joint

Now no need to order components separately for you PCB and get free from stress of soldering them on PCB just try PCB SMT assembly service and get you PCB with components pre assembled and ready for the project


👉 Try PCBA service of [JLCPCB.com](https://jlcpcb.com/IAT) and save your time and money, get PCB ready for project, 200K+ components in library of [JLCPCB.com](https://jlcpcb.com/IAT) as well as 3rd party         parts to choose from. 
    Assembly will support 10M+ parts from Digikey, mouser
    
👉 $30 valued New User coupons 

👉 $24 SMT coupons every month


For more detials & offers please visit [JLCPCB.com](https://jlcpcb.com/IAT)


# How Does the AM Transmitter/Receiver Work?

The heart of both the transmitter and receiver is the use of premade modules that help dramatically. The reason for using premade modules is due to the difficulty in getting radio transmitters and receivers at that frequency to function correctly. Some problems that can occur include incorrect inductor sizes, PCB tracing issues, proven circuitry, and tuning.

The transmitter itself consists of a switch, a 4093-based oscillator with enable, and the 433Mhz transmitter module. If the switch is open, then the NAND gate U2D outputs 0V which in turn feeds 0V into one of the inputs to the NAND gate U2B. U2B is configured as an inverting Schmitt trigger oscillator where the frequency of the oscillator is determined by the size of C5 and R2. Increasing the value of either of these components decreases the output frequency of U2B and in this circuit, they have been chosen to produce an audible tone near 500Hz. But for the oscillator to oscillate it requires its second input to be connected to VCC and so when the switch is pressed, U2D feeds a voltage of VCC into the second input of U2B. When this happens, U2B outputs the 500Hz tone into U2C and then into the data input on the 433MHz transmitter. So, to summarize, when the switch is not pressed the transmitter transmits nothing and when the switch is pressed it transmits a 500Hz tone.

The receiver consists of a configurable Schmitt trigger input, an inverter, and output buffer. The input Schmitt trigger that takes the signal from the receiver module is used as to prevent noise on the input (RV1 and RV2 can be adjusted to give a clean signal from the receiver). The signal is then buffered with U2B to improve output impedance and this buffered signal is finally fed into a basic driver consisting of U1A, U1B, U1C, U1E, and U1F all in parallel to improve output current capabilities. The final output is fed into C1 to remove the DC offset so the signal can be fed into headphones.


# Construction

Like all electronic projects posted by myself, this circuit is ideal for most circuit construction techniques. These include the use of a custom PCB (design files provided), stripboard, breadboard, and for those who are feeling adventurous, point-to-point. When building this project, the application that the circuit is used in should be considered. For example, if the objective is to have the transmitter/receiver portable, mount the circuit on a single board and use a project enclosure. Powering the circuits can be done with any voltage source about 6V and lower than 30V. The project built here uses 9V batteries that fit nicely to the side of the project base.


# Transmitter Circuit

![image](https://user-images.githubusercontent.com/19898602/172847044-734a2bff-1c26-4129-afc2-67795fb74c68.png)

Receiver Circuit

![image](https://user-images.githubusercontent.com/19898602/172847129-d57dee97-4783-4027-ab41-06433c669b06.png)



