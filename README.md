ATtiny84-Blink-all-Pinouts
==========================

Blink an LED on each pinout of the ATtiny84 using Arduino IDE

/*
  This sketch turns on an LED on for 0.2 seconds, then off for 0.5 seconds 
  for each useable pinout on the ATtiny84 - there are 11 useable.

  To use, make sure you configure the ARduino software and hardware to use as an ISP.
  
  ATtiny Pin 1: 5V
  ATtiny Pin 2: myPin 0
  ATtiny Pin 3: myPin 1
  ATtiny Pin 4: RESET  
  ATtiny Pin 5: myPin 2
  ATtiny Pin 6: myPin 3
  ATtiny Pin 7: myPin 4
  ATtiny Pin 8: myPin 5
  ATtiny Pin 9: myPin 6
  ATtiny Pin 10: myPin 7  
  ATtiny Pin 11: myPin 8
  ATtiny Pin 12: myPin 9  
  ATtiny Pin 13: myPin 10
  ATtiny Pin 14: myPin GND 
 */
 
// declare pins
int myPins[] = {0,1,2,3,4,5,6,7,8,9,10,11,12};
int i =0;

void setup() 
{                
    pinMode(myPins[0], OUTPUT);
    pinMode(myPins[1], OUTPUT);
    pinMode(myPins[2], OUTPUT);
    pinMode(myPins[3], OUTPUT);
    pinMode(myPins[4], OUTPUT);
    pinMode(myPins[5], OUTPUT);
    pinMode(myPins[6], OUTPUT);
    pinMode(myPins[7], OUTPUT);
    pinMode(myPins[8], OUTPUT);
    pinMode(myPins[9], OUTPUT);
    pinMode(myPins[10], OUTPUT);
    pinMode(myPins[11], OUTPUT);
    pinMode(myPins[12], OUTPUT);
}

// the loop routine runs over and over again forever:
void loop() 
{
  i = 0;   //reset i so that for loop repeats
  for (i=0; i<11;i++)
  {
    digitalWrite(myPins[i], HIGH);   // turn the myPins[#] on
    delay(200);                      // wait for 200 milliseconds
    digitalWrite(myPins[i], LOW);    // turn the myPins[#} off
    delay(200);
  }
}
