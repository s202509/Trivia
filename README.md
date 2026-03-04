# Trivia
## Inngangur: 

Friðrik, Lára og Stefán er hópurinn okkar og hugmyndin okkar var að hafa skemmtilegt trivia spil þar sem maður fer í gegnum skóg og stoppar til að svara spurningum fyrir verðlaun eða refsingu. 
 

## Leik reglur 

1. Yngstur byrjar  

2. Allir byrja á byrjunar reit og fyrstur að loka reit vinnur. 

3. Þarft að lenda nákvæmlega á lokareitnum. 

4. Þú ýtir á bláa takkan til að kasta teningnum. 

5. Ef þú lendir á grænum reit þá dregurðu grænt spil. 

6. Ef þú lendir á rauðum reit þá dregurðu rautt spil. 

7. Gulir reitir gera ekki neitt. 

8. Hægt er að fá spilapeninga frá grænum spilum sem vernda þig frá rauðum spilum. 

9. Það er nokkrar leiðir sem hægt er að taka á leiðinni að lokareitnum. 

10. Þegar þú dregur spil, dregur manneskjan til hægri við þig spilið fyrir þig.

## Myndir

Hérna er mynd af pappírsfrumgerð okkar 
![mynd](image.png)

Hérna eru myndir af spilinu okkar að innan og utan


Innan
![mynd](spil_neðan)


Utan
![mynd](spil_ofan)

Hérna mynd af spilaleikmunum okkar
![mynd](spilahlutir)

Hérna er mynd af lóðunnini okkar
![mynd](lodun)
## Myndband
"https://youtu.be/-wqDhJdIqfo"

## Hönnunarskrá
Hérna er svr fyrir lokið
![mynd](Bordspil_lok(235x400).svg)

Hérna eru 3d kallarnir okkar
![mynd](gamepieces1)
![mynd](gamepieces2)
![mynd](gamepieces3)
![mynd](gamepieces4)

Hérna eru spilapeningarnir okkar
![mynd](spilap)

## Kóðinn
***
# https://wokwi.com/projects/441804604337655809
from machine import Pin
import neopixel
from time import sleep_ms
from random import randint  # til að geta unnið með random
import time
from buzzer_music import music
from time import sleep

# LEDPixel tenging ( IN )
# S digital pinni
# V 5V
# G GND

pin = Pin(8, Pin.OUT)
np = neopixel.NeoPixel(pin, 24)	# 8 x RGB Leds
takki1 = Pin(10, Pin.IN, Pin.PULL_UP)

# breytur
brightness = 53                # birtustig frá 0 - 255

# búum til liti með RGB litakerfi.
red   =  [ brightness, 153, 2]    # red
          # ekkert ljós
song = '0 B4 1 50;1 D5 1 50;2 B5 1 50;3 A5 4 50;8 F#5 1 50;12 E5 1 50;15 B4 1 50;18 E5 6 50;7 G#5 1 50;9 G#5 1 50;10 F#5 1 50;0 B3 1 50;1 D4 1 50;2 B4 1 50;3 A4 4 50;8 F#4 1 50;12 E4 1 50;15 B3 1 50;18 E4 6 50;7 G#4 1 50;9 G#4 1 50;10 F#4 1 50;0 B6 1 50;1 D7 1 50;2 B7 1 50;3 A7 4 50;8 F#7 1 50;12 E7 1 50;15 B6 1 50;18 E7 6 50;7 G#7 1 50;9 G#7 1 50;10 F#7 1 50;0 B5 1 50;1 D6 1 50;2 B6 1 50;3 A6 4 50;8 F#6 1 50;12 E6 1 50;15 B5 1 50;18 E6 6 50;7 G#6 1 50;9 G#6 1 50;10 F#6 1 50;18 E5 6 50;18 E4 6 50;18 E7 6 50;18 E6 6 50;18 E5 6 50;18 E4 6 50;18 E3 6 50;18 E2 6 50;0 B4 1 50;1 D5 1 50;2 B5 1 50;3 A5 4 50;8 F#5 1 50;12 E5 1 50;15 B4 1 50;18 E5 6 50;7 G#5 1 50;9 G#5 1 50;10 F#5 1 50;0 B3 1 50;1 D4 1 50;2 B4 1 50;3 A4 4 50;8 F#4 1 50;12 E4 1 50;15 B3 1 50;18 E4 6 50;7 G#4 1 50;9 G#4 1 50;10 F#4 1 50;0 B2 1 50;1 D3 1 50;2 B3 1 50;3 A3 4 50;8 F#3 1 50;12 E3 1 50;15 B2 1 50;18 E3 6 50;7 G#3 1 50;9 G#3 1 50;10 F#3 1 50;0 B5 1 50;1 D2 1 50;2 B2 1 50;3 A2 4 50;8 F#2 1 50;12 E2 1 50;15 B5 1 50;18 E2 6 50;7 G#2 1 50;9 G#2 1 50;10 F#2 1 50'


#One buzzer on pin 0
mySong = music(song, pins=[Pin(12)])

while True:
    if takki1.value() == 0:
        randomLed = randint(0, 23)
        # stjórnum öllum 8 leds í einu með að nota fill
        np.fill([0, 0, 0])     # ekkert ljós
         
        # led 1  
        np[randomLed] = red		        # eða np[0] = [255, 0, 0] 
        np.write()              # kveikjum á led 1

        
        time.sleep_ms(50)
    else: 
        print(mySong.tick())
        sleep(0.04)
 *     

    

        



## Samþykki fyrir birtingu verkefnis á vef

Ég gef hér með samþykki mitt fyrir því að verkefnið verði birt opinberlega á vefsvæði Tækniskólans (t.d. tskoli.is og tolvubraut.is).

Með undirritun staðfesti ég að:

1. Ég veiti leyfi til að verkefnið og tilheyrandi myndir/skjöl/hlutar af verkefninu sé aðgengilegt almenningi á netinu.
2. Réttur til að draga samþykki til baka: Ég er upplýst/ur um að ég get hvenær sem er dregið samþykki mitt til baka með því að senda skriflega tilkynningu til tskoli@tskoli.is.
3. Réttur til að gleymast: Ef samþykki er dregið til baka mun Tækniskólinn fjarlægja verkefnið af vefsvæði sínu án ástæðulausrar tafar (samkvæmt rétti einstaklings til að gleymast, sbr. 17. gr. persónuverndarlaga).
4. Tækniskólinn ber ábyrgð á meðferð persónuupplýsinga samkvæmt gildandi persónuverndarlögum.
