# arduino-potentiometer-controlling-servo-using-transistor
this is the first task for electric engineer 
first thing i have done here is connected the arduino to the board i used the (5v) pin to connect the (+) to supplay the power 
secend i uconnected the (GND) pin to (-) to close the sircuit 
3rd thing i have done is connect (~9) pin to the 5 servo motor that connected to the borad for the signals 
4rd i connet the servo motor to board and it have 3 part right for signal and mid for power and in the left for ground
5th now i have all the arduino connected and servo i need to connect transistor to controll the value of the servo motor 
i added the potentiometer to contrull the value we want and it also have 3 part from the left we have ground and mid we have signal connected to (A1) pin and right is power 

and now for the code :- 
#include <Servo.h> //accesses the Arduino Servo Library

Servo myservo;  // creates servo object to control a servo

int val;    // variable to read the value from the analog pin
void setup()
{
  myservo.attach(9);  // ensures output to servo on pin 9
}

void loop() 
{ 
  val = analogRead(1);            // reads the value of the potentiometer from A1 (value between 0 and 1023) 
  val = map(val, 0, 1023, 0, 90);     // converts reading from potentiometer to an output value in degrees of rotation that the servo can understand 
  myservo.write(val);                  // sets the servo position according to the input from the potentiometer 
  delay(15);                           // waits 15ms for the servo to get to set position  
} 
 
 
 the link :- https://www.tinkercad.com/things/laku4H4CDMD-start-simulating/editel?lessonid=EHD2303J3YPUS5Z&projectid=OIYJ88OJ3OPN3EA&collectionid=OIYJ88OJ3OPN3EA#/lesson-viewer
