#include <Wire.h>
#include <Adafruit_PWMServoDriver.h>

Adafruit_PWMServoDriver pwm = Adafruit_PWMServoDriver();

int servoMin = 150;
int servoMax = 600;
int servoMid = 375;

void setup() {
  
  pwm.begin();
  pwm.setPWMFreq(60);

  pwm.setPWM(0, 0, servoMid);  // Base Servo
  pwm.setPWM(1, 0, servoMid);  // Limb Servo
  pwm.setPWM(2, 0, servoMid);  // Hand Servo
  pwm.setPWM(3, 0, servoMid);  // Gripper Servo
}

void loop() {
  //Rotates the arm to face the boxes
  pwm.setPWM(0, 0, servoMin);
  delay(1000);
  //The limb bends to pick the boxes
  pwm.setPWM(1, 0, servoMin);
  delay(1000);
  //The hand further lowers to get closer to the box
  pwm.setPWM(2, 0, servoMin);
  delay(1000);
  //Gripper grabs the box
  pwm.setPWM(3, 0, servoMin);
  delay(1000);

  //Base faces towards the drop zone
  pwm.setPWM(0, 0, servoMax);
  delay(500);
  //The limb lowers in the drop zone
  pwm.setPWM(1, 0, servoMax);
  delay(500);
  //Gripper opens and drops the package at the drop zone
  pwm.setPWM(3, 0, servoMid);
  delay(500);
}
