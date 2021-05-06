# RB0-INT_Harici_Kesme_Uygulaması

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117267790-50767a00-ae5f-11eb-8835-9104a4bc1139.png)

![image](https://user-images.githubusercontent.com/53540561/117267829-59ffe200-ae5f-11eb-9790-1e75b7798b72.png)


## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117267907-6dab4880-ae5f-11eb-8938-210b00e1b3e2.png)

![image](https://user-images.githubusercontent.com/53540561/117267858-61bf8680-ae5f-11eb-9f44-4c2744f2f80d.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <deney_5_a.h>

#INT_EXT
void  dis_kesme(void) 
{
output_high(pin_c7);
delay_ms(3000);
output_low(pin_c7);
}

void main()
{
   enable_interrupts(INT_EXT);
   enable_interrupts(GLOBAL);
   
   ext_int_edge(H_to_L);
   
   while(TRUE)
   {
   
   }
}
```
