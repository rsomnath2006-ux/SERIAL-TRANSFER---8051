# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**

Serial port transfer a character A:
<img width="948" height="156" alt="image" src="https://github.com/user-attachments/assets/08d21f44-ed23-461c-8970-3577403859d8" />

Serial port to Transfer a Message:
<img width="955" height="187" alt="Screenshot 2025-11-11 083744" src="https://github.com/user-attachments/assets/11db5178-7859-4426-9dbd-6ad1c6d15bc7" />


**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
