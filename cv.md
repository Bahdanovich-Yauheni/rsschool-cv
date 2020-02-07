1. Bahdanovich Yauheni;
2. bahdanovich.yauheni@gmail.com, +375292415583;
3. My goal is to acquire skills and knowledge of javascript development, but what is more importaint - I want to find out, will I be able to pass through this 5-months marathon?
4. I've made several simple projects on Arduino platform;
5.     #include <Wire.h> 
    #include <LiquidCrystal_I2C.h>
    LiquidCrystal_I2C lcd(0x27,16,2);  // set the LCD address to 0x27 for a 16 chars and 2 line display
    int res = 0;
    int timer = 0;
    int btn = 0;
    int n = 0;
    void setup()
    { pinMode(A3, INPUT);
      pinMode(6, INPUT); 
      pinMode(8, OUTPUT);
      pinMode(9, OUTPUT);
      lcd.init();                      
  
      // Print a message to the LCD.
      lcd.backlight();
      lcd.setCursor(4,0);
      lcd.print("Timer, s");
      digitalWrite(8, HIGH);
     }
    
    void loop() {
    res = analogRead(A3);
    timer = 10 * res - 6900;
    lcd.setCursor(6,1);
    lcd.print(timer);
    delay(10);
    n = n + 1;
    if (n == 100){
      n = 0;
      lcd.clear();
      lcd.setCursor(4,0);
      lcd.print("Timer, s");}
    btn = digitalRead(6);
    if (btn == 1)
     {for (int i=timer; i >=0; i-- ){
      lcd.setCursor(6,1);
      lcd.print(i);
      delay(990);
      digitalWrite(9, HIGH);
      delay(10);
      digitalWrite(9, LOW);
    lcd.clear();
      lcd.setCursor(4,0);
      lcd.print("Timer, s");
      if (i == 1)
      {digitalWrite(8, LOW);
      delay(1000);     
      digitalWrite(8, HIGH);}
      }
     }
    }
6. I have expirience of a man, who learned computer science in the Univercity on a technical speciality, that wasn't connected with programming;
7. Higher education (Gomel State Technical University named after Sukhoi);
8. My English level is B1.