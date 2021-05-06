# LCD_ile_Kayan_Yazı_Uygulaması

## Devre Şeması
![image](https://user-images.githubusercontent.com/53540561/117267296-cdedba80-ae5e-11eb-8976-6670cfde0fca.png)

## Açıklama
![image](https://user-images.githubusercontent.com/53540561/117267529-0a211b00-ae5f-11eb-9bdb-a9c3181dae76.png)

![image](https://user-images.githubusercontent.com/53540561/117267320-d3e39b80-ae5e-11eb-9f8a-b8bb82c09d10.png)

## Arduino Kodları

BU SADECE 1.ŞIKTIR DİĞER ŞIKLAR RAR İÇERİSİNDEDİR.
```
#include <deney_dort_a.h>
#define LCD_ENABLE_PIN PIN_D0
#define LCD_RS_PIN PIN_D1
#define LCD_RW_PIN PIN_D2
#define LCD_DATA4 PIN_D4
#define LCD_DATA5 PIN_D5
#define LCD_DATA6 PIN_D6
#define LCD_DATA7 PIN_D7

#include <lcd.c>

int x=0;

void main()
{
   lcd_init();

   Printf(lcd_putc,"\f Sifreyi giriniz:");
   
   while(TRUE)
   
   {    
      if(input(pin_a1))
      {    
         while(input(pin_a1));
         
         x++;
        
         if(x==3)
         {
            
            Printf(lcd_putc,"\fHosgeldiniz \nDoguhan Culhacioglu");
            
            tekrar:
         
            for(int i=0; i<16; i++)
    
            {
               lcd_send_byte(0,0x1E);
               delay_ms(100);
    
            }        
            goto tekrar;
           
         }
    
      }
   }
}

```
