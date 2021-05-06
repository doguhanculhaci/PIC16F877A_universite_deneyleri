# 7-Parçalı_Ekran(Segment_Display)_ile_0-9_Sayıcı

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117266674-2c666900-ae5e-11eb-9e24-97ab813d35b0.png)

## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117266703-34260d80-ae5e-11eb-8d15-efe3e231172d.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <deney_uc_a.h>

void main()
{

int rakam[10]={0x3F , 0X06 , 0X5B , 0X4F , 0X66 , 0X6D , 0X7C , 0X07 , 0X7F , 0X6F};

output_b(0);

   while(TRUE)
   {
      for (int i=0; i<=9; i++)
      {
      output_b(rakam[i]);
      delay_ms(1000);
      }
   }
}

```
