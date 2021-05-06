# Değişken_LED_Kontrolü

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117266092-916d8f00-ae5d-11eb-8376-765ecdacb03d.png)

## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117266133-9b8f8d80-ae5d-11eb-9fbf-d2a088bc837b.png)
![image](https://user-images.githubusercontent.com/53540561/117266154-a0544180-ae5d-11eb-8407-6689d96edad4.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <deney_iki_a.h>

int x1 = pin_b0;
int x2 = pin_b1;
int x3 = pin_b2;
int x4 = pin_b3;
int x5 = pin_b4;
int x6 = pin_b5;
int x7 = pin_b6;
int x8 = pin_b7;

void main()
{
   output_b(0);

   while(TRUE)
   {
      output_toggle(x1);
      delay_ms(100);
      output_toggle(x2);
      delay_ms(100);
      output_toggle(x3);
      delay_ms(100);
      output_toggle(x4);
      delay_ms(100);
      output_toggle(x5);
      delay_ms(100);
      output_toggle(x6);
      delay_ms(100);
      output_toggle(x7);
      delay_ms(100);
      output_toggle(x8);
      delay_ms(100);
   }

}
```
