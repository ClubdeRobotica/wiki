## page was renamed from nuevo_contenido
== Formulas para PWM en PIC ==

'''Para CCS'''

El ciclo de tiempo sera : (1/clock)*4*t2div*(period+1)

period : 0 a 255

Para 4mhz:
 *(1/4000000)*4*1*(127+1) = 128us o '''7.81 KHz'''
 *(1/4000000)*4*4*(127+1) = 512us o '''1.95 KHz'''
 *(1/4000000)*4*16*(127+1)= 2 ms  o '''488.28 Hz'''

'''Para SDCC'''

PWM period = [(PR2) + 1]*4*TOSC*(TMR2 prescale value)

PWM duty cycle =(CCPR1L:CCP1CON<5:4>)*TOSC*(TMR2 prescale value)

== Pagina generadora de codigo ==

 [[http://www.micro-examples.com/public/microex-navig/doc/097-pwm-calculator.html|Generador de codigo para PWM]]

== Rutina de Incremento de PWM ==


||[[attachment:Rutina_aumento_pwm]]||

Dudas:
 * Tosc = 1/Fosc ??
 * Obtener por calculo (CCPR1L:CCP1CON<5:4>)

---------
||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:VRTD_PWM_1.jpg||width=300}} ||
