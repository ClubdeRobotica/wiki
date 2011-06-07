## page was renamed from nuevo_contenido
== Formulas para PWM en PIC ==

El ciclo de tiempo sera : (1/clock)*4*t2div*(period+1)

period : 0 a 255

Para 4mhz:
 *(1/4000000)*4*1*(127+1) = 128us o '''7.81 KHz'''
 *(1/4000000)*4*4*(127+1) = 512us o '''1.95 KHz'''
 *(1/4000000)*4*16*(127+1)= 2 ms  o '''488.28 Hz'''

PWM period = [(PR2) + 1]*4*TOSC*(TMR2 prescale value)

PWM duty cycle =(CCPR1L:CCP1CON<5:4>)*TOSC*(TMR2 prescale value)

---------
PWM frequency is defined as 1 / [PWM period]. 
When TMR2 is equal to PR2, the following three events occur on the next increment cycle: 
 * TMR2 is cleared 
 * The CCP1 pin is set (exception: if PWM duty cycle = 0%, the CCP1 pin will not be set) 
 * The PWM duty cycle is latched from CCPR1L into CCPR1H

--------

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:VRTD_PWM_1.jpg||width=300}} ||
