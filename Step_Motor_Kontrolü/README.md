# Step_Motor_Kontrolü

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117269190-bd3e4400-ae60-11eb-848f-f782b3e94331.png)

## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117269284-d34c0480-ae60-11eb-951a-8261386d62c2.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <182101019.h>
#define ileri pin_a0
#define geri pin_a1

unsigned int8 adim []={0b00001000,0b00001100,0b00000100,0b00000110,0b00000010,0b00000011,0b00000001,0b00001001};
int1 durum=0,kontrol=0;
int16 hiz=200,i=0 ;

void main()
{
   output_b(0b00000000);
   
   while(TRUE)
   {
      if(input(ileri))
      {
         durum=false;
         kontrol=true;
      }
    
      if(input(geri))
      {
         durum=true;
         kontrol=true;
      }
      
      if(kontrol)
      {
         if(durum)
         {
            if(i==8) 
            i=-1;
            i++;
            output_b(adim[i]);
            delay_ms(hiz);
         }
         else
         {
            if(i==0)
            i=8;
            i--;
            output_b(adim[i]);
            delay_ms(hiz);
         }
      }
      
   }
}
```
