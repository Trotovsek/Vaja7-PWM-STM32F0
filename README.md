# Vaja7-PWM-STM32F0
CUBE MX

b) V levem Pinout oknu razširite nabor možnosti za časovnik TIM1. Clock Source nastavite kot Internal
Clock. Prvi kanal aktivirajte kot PWM Generation CH1. Kateri pin ste omogočili? PA8. Kaj se
izpiše poleg pina? TIM1_CH1.



d) V Configuration kliknemo TIM1 gumb. Vrednost Prescaler v zavihku Parameter Settinngs določite tako,
da bo časovnik delal s frekvenco 1 MHz. Koliko je vrednost Perscaler? 16.


e) Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika. Koliko znaša
sedaj? 10 kHz.

f) Pulse (16 bits value) nastavite na 50. Kaj pomeni ta parameter? Namig – največja vrednost je lahko 100
odstotkov (znak za odstotek v polja ne pišemo). To pomeni da nastavimo duty cycle na 50% saj je to polovica counter period, ki je 100.

Kyle v5

b) Poiščite prenastavljeni parameter Pulse (ki je 50) v vaši kodi in prepišite ukaz, ki ga je generiral CubeMX:
  sConfigOC.Pulse = 50;



c) V kodi spremenite vrednost širine pulza na 25 %. Zapišite popravljeni ukaz v kodi:
  sConfigOC.Pulse = 25;


Ponovno naložite program in s telefonom posnamite signal na zaslonu osciloskopa.
Zapišite kaj počnejo ukazi v 1.,2. in 3. vrstici (v user code begin 3):
1. v prvi vrstici v register spreminja vrednost duty cycla, ki ga razbere iz spremenljivke dutyCycle

2. spremnljivko dutycycle poveča za 10

3.  ko duty cycle pride do 90 se ponovno postai na vrednost 10.


Komentar: program deluje brez težav. osciloscop ni bilo potrebno nastavljati sam ima fukncijo avto scale, ki vrednosti nastavi sam. signal je lep brez popačenja.
