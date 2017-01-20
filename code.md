#include <Servo.h>
Servo myservo; // insert the Servo.h library
// create servo object to control servo
int potpin = 0;
int val; // connect potentiometer to digital pin0
// variable value to read value from analog pin
void setup() {
  myservo.attach(9);
} //Attach the servo on pin 9 to the servo object.
void loop() {
  val = analogRead(potpin);
  //(value between 0 and 1023)
  val = map(val, 0, 1023, 0, 179);
  //between 0 and 180)
  myservo.write(val);
  //scaled value
  delay(15);
}
