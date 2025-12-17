# Vaja3 ADC trigger timer conversion NUCLEO

Pinout mikroporcesorja iz CubeMX:  
<img width="550" height="515" alt="Posnetek zaslona 2025-12-10 095827" src="https://github.com/user-attachments/assets/ec7d8638-d58b-4d68-80c9-ca029a20f056" />  
  
TIM2 configuration-parameter settings:  
<img width="1920" height="1025" alt="Posnetek zaslona 2025-12-10 095925" src="https://github.com/user-attachments/assets/69b728ac-fe0a-446d-9c95-c03b20d506e5" />  

ADC configuration-parameter settings:  
<img width="1920" height="1023" alt="Posnetek zaslona 2025-12-10 095950" src="https://github.com/user-attachments/assets/f839552a-35f3-4a97-a39f-e7d2ae68e786" />  

Videoposnetek delovanja:  
<a href="https://video.ctrlgrid.com/watch.php?v=guHVn1TAqdj">Posnetek delovanja</a>    

Fotografija vezave:  
![PXL_20251210_090030876](https://github.com/user-attachments/assets/c648c4c9-dfd2-42c4-9d87-c63f1b312fc1)  

Odgovori na vprašanja:  
1. Koliko je vseh ADC pretvornikov? 3.  
2. V Clock Configuration spremenimo APB1 Timer clocks (MHz) na 16 MHz (pritisnemo ENTER). Kaj opazite? CubeIDE avtomatsko prilagodi ostale.
3. V razdelku TIM2, pod Timers, bi radi časovniku spremenili frekvenco na 1 kHz, zato moramo prej določeno 
frekvenco ABP1 Timer Clock preskalirati v polju Prescaler (PSC – 16 bit value). Koliko znaša ta vrednost? 15999
4. Branje vrednosti želimo prikazati z utripanjem zelene LED diode na Nucleo ploščici. Uporabite metodo 
TogglePin iz HAL knjižnice in zapišite ukaz: (pomagajte si z vajo0a). Ukaz: HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5);  
  
Komentar:  
Vse deluje kot predvideno.


