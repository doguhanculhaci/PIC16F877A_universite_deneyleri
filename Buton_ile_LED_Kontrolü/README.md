# Buton_ile_LED_Kontrolü

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117265642-1d32eb80-ae5d-11eb-8c7c-ca28cdd2ceef.png)

## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117265603-11472980-ae5d-11eb-8da0-6723c528423a.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <deney_bir_a.h>

void main()
{
  int DogCul1 = pin_a1;
  
  int DogCul2 = pin_b1;
  int DogCul3 = pin_b2;

   while(TRUE)
   {
      if (input(DogCul1) == 0)
     {
       output_high(DogCul2);
       output_low(DogCul3);
     }
     else
     {
       output_low(DogCul2);
       output_high(DogCul3);
     }
   }

}
```
