# Arduino Traffic Light with LCD Counter Display
This project demonstrates how to create a simple traffic light system using an Arduino board and an LCD display to show the time left for each signal.

Components and Supplies: 
1. Alphanumeric LCD, 16 x 2
2. 5 mm LED: Yellow
3. 3 mm LED: Green
4. Arduino UNO
5. Breadboard
6. 1k ohm Resistor
7. Jumper wires
8. 5 mm LED: Red
9. Tools and Libraries
10. LiquidCrystal.h Library
11. Arduino IDE
    
Project Description:
The project simulates a traffic light system with three signals: red, yellow (blue in this project), and green. The LCD display shows the time remaining for each signal change.


Circuit Diagram : 
https://github.com/Rajat22UEE/Arduino-Traffic-light/issues/1#issue-2306843806

Video demostration : 
https://github.com/Rajat22UEE/Arduino-Traffic-light/issues/2#issue-2306860473

# Here the code :

#include <LiquidCrystal.h>

int red = 9;
int yellow = 8;
int green   = 7;
int backlight = 6; // PWM pin for backlight control

LiquidCrystal lcd(11, 10, 5, 4, 3, 2); 

void setup(){
  
  pinMode(red, OUTPUT);
  pinMode(yellow,   OUTPUT);
  pinMode(green, OUTPUT);
    lcd.begin(16, 2);

    // Set initial brightness
    analogWrite(backlight, 128); // Adjust value between 0 (off) to 255 (full brightness)

    lcd.setCursor(0,   0);
    lcd.print("   Turning On   ");
    lcd.setCursor(0, 1);
    lcd.print("   Traffic  Light ");
    delay(2000);
  lcd.clear();
lcd.setCursor(0, 0);
     lcd.print("     SYSTEM");
    lcd.setCursor(0, 1);
    lcd.print("        ON");
    delay(1500);
  lcd.clear();

    
}
void loop(){
   lcd.begin(16, 2);
  lcd.setCursor(0, 0);
    lcd.print("Stop Red Light ");
     lcd.setCursor(0, 1);
    lcd.print("15 Second");
  digitalWrite(red,   HIGH);
    delay(1000);
 
lcd.setCursor(0, 1);
    lcd.print("14 Second");
   digitalWrite(red, HIGH);
    delay(1000); 
  lcd.setCursor(0, 1);
    lcd.print("13   Second");
  digitalWrite(red, HIGH);
    delay(1000);
lcd.setCursor(0,   1);
    lcd.print("12 Second");
  digitalWrite(red, HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
    lcd.print("11 Sec");
  digitalWrite(red, HIGH);
     delay(1000);
     lcd.setCursor(0, 1);
    lcd.print("10 Sec");
   digitalWrite(red, HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
     lcd.print("09 Sec");
  digitalWrite(red, HIGH);
    delay(1000);
     

lcd.setCursor(0, 1);
    lcd.print("08 Second");
  digitalWrite(red,   HIGH);
    delay(1000);
lcd.setCursor(0, 1);
    lcd.print("07 Second");
   digitalWrite(red, HIGH);
    delay(1000);
lcd.setCursor(0, 1);
    lcd.print("06   Second");
  digitalWrite(red, HIGH);
    delay(1000);

lcd.setCursor(0,   1);
    lcd.print("05 Second");
  digitalWrite(red, HIGH);
    delay(1000);
lcd.setCursor(0,   1);
    lcd.print("04 Second");
  digitalWrite(red, HIGH);
    delay(1000);
lcd.setCursor(0,   1);
    lcd.print("03 Second");
  digitalWrite(red, HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
    lcd.print("02 Second");
  digitalWrite(red,   HIGH);
    delay(1000);
lcd.setCursor(0, 1);
    lcd.print("01 Second");
   digitalWrite(red, HIGH);
    delay(1000);
lcd.clear();
digitalWrite(red,   LOW);




lcd.setCursor(0, 0);
lcd.print("On Yellow Light");
     lcd.setCursor(0, 1);
    lcd.print("05 Second");
  digitalWrite(yellow,   HIGH);
delay(1000);
  digitalWrite(yellow, LOW);
delay(500);
lcd.setCursor(0,   1);
    lcd.print("04 Second");
  
  digitalWrite(yellow, HIGH);
delay(1000);
   digitalWrite(yellow, LOW);
delay(500);
lcd.setCursor(0, 1);
    lcd.print("03   Second");
  
  digitalWrite(yellow, HIGH);
delay(1000);
  digitalWrite(yellow,   LOW);
delay(500);
  lcd.setCursor(0, 1);
    lcd.print("02 Second");
   
  digitalWrite(yellow, HIGH);
delay(1000);
  digitalWrite(yellow, LOW);
delay(500);
   lcd.setCursor(0, 1);
    lcd.print("01 Second");
  
  digitalWrite(yellow,   HIGH);
delay(1000);
  digitalWrite(yellow, LOW);
delay(500);
  lcd.setCursor(0,   1);
    lcd.print("01 Second");
  
lcd.setCursor(0, 0);
    lcd.print("GoGo   Green Light");
lcd.setCursor(0, 1);
    lcd.print("20 Second");
  digitalWrite(green,   HIGH);
    delay(1000);

lcd.setCursor(0, 1);
    lcd.print("19 Second");
   digitalWrite(green, HIGH);
    delay(1000);

lcd.setCursor(0, 1);
     lcd.print("18 Second");
  digitalWrite(green, HIGH);
    delay(1000);

lcd.setCursor(0,   1);
    lcd.print("17 Second");
  digitalWrite(green, HIGH);
    delay(1000);

lcd.setCursor(0,   1);
    lcd.print("16 Second");
  digitalWrite(green, HIGH);
    delay(1000);
   
   lcd.setCursor(0, 1);
    lcd.print("15 Second");
  digitalWrite(green,   HIGH);
    delay(1000);
 
lcd.setCursor(0, 1);
    lcd.print("14 Second");
   digitalWrite(green, HIGH);
    delay(1000); 
  lcd.setCursor(0, 1);
     lcd.print("13 Second");
  digitalWrite(green, HIGH);
    delay(1000);
lcd.setCursor(0,   1);
    lcd.print("12 Second");
  digitalWrite(green, HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
    lcd.print("11 Sec");
  digitalWrite(green,   HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
    lcd.print("10 Sec");
   digitalWrite(green, HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
     lcd.print("09 Sec");
  digitalWrite(green, HIGH);
    delay(1000);
     

lcd.setCursor(0, 1);
    lcd.print("08 Second");
  digitalWrite(green,   HIGH);
    delay(1000);
lcd.setCursor(0, 1);
    lcd.print("07 Second");
   digitalWrite(green, HIGH);
    delay(1000);
lcd.setCursor(0, 1);
    lcd.print("06   Second");
  digitalWrite(green, HIGH);
    delay(1000);

lcd.setCursor(0,   1);
    lcd.print("05 Second");
  digitalWrite(green, HIGH);
    delay(1000);
lcd.setCursor(0,   1);
    lcd.print("04 Second");
  digitalWrite(green, HIGH);
    delay(1000);
lcd.setCursor(0,   1);
    lcd.print("03 Second");
  digitalWrite(green, HIGH);
    delay(1000);
     lcd.setCursor(0, 1);
    lcd.print("02 Second");
  digitalWrite(green,   HIGH);
    delay(1000);
lcd.setCursor(0, 1);
    lcd.print("01 Second");
   digitalWrite(green, HIGH);
    delay(1000);
lcd.clear();
digitalWrite(green,   LOW);


  lcd.setCursor(0, 0);
lcd.print("Of Yellow Light");
    lcd.setCursor(0,   1);
    lcd.print("05 Second");
  digitalWrite(yellow, HIGH);
delay(1000);
   digitalWrite(yellow, LOW);
delay(500);
lcd.setCursor(0, 1);
    lcd.print("04   Second");
  
  digitalWrite(yellow, HIGH);
delay(1000);
  digitalWrite(yellow,   LOW);
delay(500);
lcd.setCursor(0, 1);
    lcd.print("03 Second");
   
  digitalWrite(yellow, HIGH);
delay(1000);
  digitalWrite(yellow, LOW);
delay(500);
   lcd.setCursor(0, 1);
    lcd.print("02 Second");
  
  digitalWrite(yellow,   HIGH);
delay(1000);
  digitalWrite(yellow, LOW);
delay(500);
  lcd.setCursor(0,   1);
    lcd.print("01 Second");
  
  digitalWrite(yellow, HIGH);
delay(1000);
   digitalWrite(yellow, LOW);
delay(500);
  
}




