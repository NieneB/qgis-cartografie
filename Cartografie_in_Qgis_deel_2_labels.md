

## Labels

Voeg nog een keer de gemeenten grenzen toe aan het project en zet de oude laag uit. We gaan kijken naar de gemeenten naam labels! 

1. Selecteer de **Simple fill** van de gemeenten polygonen en zet de **Fill style** op: **No Brush**.
2. Zet de **Stroke color** op grijs. De **Stroke width** op 1 pixel en de **Stroke style** op **Dot line**. 
3. De **Join style** op **Round**

Speel met deze waarden als je wilt, zodat je mooie subtiele gemeenten grenzen hebt. 

4. Ga naar de Label tab! Dit is de tweede tab aan de linkerzijde op het **Layer styling** paneel. 

![](./img/tabs.png)

1. Verander de **No labels** naar **Single labels**
2. Zet de **Label with** op de kolom naam met de gemeente naam. 

Nu kunnen we de labels gaan stylen. 

3. Verander het font!
4. Zet de kleur op wit. 
5. Verander de grootte naar 8. 

### Labels Stijlen op aantal inwoners

1. Klik op het extra menu icoontje naast **Size**.

![](./img/size_menu.png)

2. Ga naar **Assistant**

Hier kunnen we de grootte van het font laten afhangen van een waarde in de data!

3. Zet de **Source** op aantal inwoners. 
4. Door op de blauwe pijltjes te drukken berekend het programma de max en min waarden van het aantal inwoners voor je! 
5. De Output zijn de font grootte waarder waartussen hij de data waarden gaan interpoleren. Zet deze van 5 tot 16. 

![](.img/curve.png)

6. Zelfs de curve van de interpolatie kan je aanpassen! 

7. Ga naar de tab **Placement**
![](./img/placement.png)

8. Zet dezelfde settings in. 
9. Ga naar de tab **Rendering**

![](./img/rendering.png)

De **Label z-index** zorgt voor de hierarchy waarmee de labels gerenderd worden. Klik op het extra menu knop ernaast en ga naar de  **Assistant**.
Ook hier kunnen we de z-index afhankelijk maken van het aantal inwoners. 
Let op de curve! De data is niet mooi verdeeld. Het is dus handig om deze handmatig aan te passen:

![](./img/curve_2.png)

We hebben alsnog een probleem met de labeling van Amsterdam. Omdat er meerdere polygonen zijn die deze naam bevatten kan Qgis niet kiezen welke hij wel of niet moet renderen. 
Om af te dwingen dat bepaalde labels áltijd aanwezig zijn kunnen we naar het edit menu gaan van **Data Defined > Always show**

10. Klik op de menu knop en ga naar edit.

![](./img/data_Defined.png)

Voer in:

        "gm_naam" = 'Amsterdam'

Nu is de label Amsterdam altijd zichtbaar! Je resultaat zal er nu ongeveer zo uit zien: 


![](./img/slechte_labels.png)

Niet echt mooi of optimaal. Een reden hiervoor is, is dat de gemeenten data set totaal niet goed ontworpen is om labels van te maken! 

*Uitdaging*: speel met de settings tot je wel tevreden bent! 


## Labels 2

7. Ga naar de tab **Placement**
![](./img/placement.png)

8. Zet de **Placement** op **Using Perimeter(curved)**
9. **Allowed Positions** op **Right of line**
10. Vink de **Line orientation dependent position** aan.
11. Zet **Repeat** op 1000 **Map Units**
