# Arduino-clock-with-BigBenChime
Clock , Alarm, Timer, Temperature, Humidity, year, month, day, day of week, 

display mode cycle: clock  hh:mm, timer Tmmm, temperature nn:nc, relative_humidity nn:n%
timer display cycle will be skipped if timer=0
setting mode: timer Tmmm, alarm_hour hh, alarm_minute mm, year Y_yy, month M_mm, day D_dd, hour hh:, minute :mm, quarter_chime c, brightness
maximum timer 999 minutes
a R-2R resistor ladder is used to preform the DAC function 
Big ben tone is downloaded from https://www.parliament.uk/about/living-heritage/building/palace/big-ben/anniversary-year/downloads/.
converted to adpcm and decode to 16bit unsigned pcm sound when playing. However only the 7 MSB is output to the DAC due to the limited number of Arduino I/O pin

hour side switch for increment
minute side switch for change setting mode
press both switch for setting to zero on current set item
set alarm_hour = 24 to turn off alarm clock, 
press any switch to stop alarm during display mode
press increment switch to scroll Ahhmm Cyyyy-mmm-dd ddd during display mode
chime work from 07:00 to 22:55, set chime=0 to turn off, 1 to turn on 4th quarter, 2 to turn on all quarters, 3 to turn on all quarters plus hour counting strick
hardware list:
1. Arduino nano https://item.taobao.com/item.htm?spm=a1z09.2.0.0.4c232e8dg181aU&id=561096743971&_u=nlf344u6f54

2. AHT10 temp and humidity sensor, https://item.taobao.com/item.htm?spm=a1z09.2.0.0.593e2e8dkvZHBR&id=602466803728&_u=nlf344ue07b

3. 4-digit display w/TM1637, https://item.taobao.com/item.htm?spm=a1z09.2.0.0.593e2e8dkvZHBR&id=576752165735&_u=nlf344ub8f2

4. passive buzzer,

5. 2x micro switch

6. KA2209 amplifier https://item.taobao.com/item.htm?spm=a1z09.2.0.0.593e2e8dkvZHBR&id=567005009031&_u=nlf344uffc7

7. C9013 NPN transistor

8. 1N4007 diode

9. 470u 10v electrolyte capacitor

10. 100u 10v electrolyte capacitor

11. 1K ohm resistor

12. 10k ohm resistor x6

13. 15k ohm resistor

14. 20k ohm resistor x8

15. 1M ohm resistor
