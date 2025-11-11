# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character R**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='R';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Serial port to Transfer a Message"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**

**(i)	Serial port transfer a character R**
<img width="1919" height="1079" alt="Screenshot 2025-11-11 082749" src="https://github.com/user-attachments/assets/89f3d28e-7f6c-4050-a590-60103c6ac429" />

**(ii)	Serial port to Transfer a Message**
<img width="1918" height="1079" alt="Screenshot 2025-11-11 093847" src="https://github.com/user-attachments/assets/6489cbc3-17f7-47cd-9eb8-6826fa218ee1" />



**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
