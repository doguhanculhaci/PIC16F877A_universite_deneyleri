# INT-RB_Kesme_Uygulaması

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117268348-db577480-ae5f-11eb-842d-8a9439ba25d2.png)

![image](https://user-images.githubusercontent.com/53540561/117268370-e3171900-ae5f-11eb-9220-5d73d433f6d0.png)

## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117268516-03df6e80-ae60-11eb-99af-d7659c252677.png)

![image](https://user-images.githubusercontent.com/53540561/117268426-edd1ae00-ae5f-11eb-8621-d778efc92932.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <deney_6_a.h>

#INT_RB
void  RB_isr(void) 
{
   if(input(pin_b4) || input(pin_b5) || input(pin_b6) || input(pin_b7))
   {
      output_high(pin_d7);
      delay_ms(3000);
      output_low(pin_d7);
   }
}

void main()
{
   set_tris_b(0x01);
   output_low(pin_c7);
   enable_interrupts(INT_RB);
   enable_interrupts(GLOBAL);

   while(TRUE)
   {
      //TODO: User Code
   }
}
```
