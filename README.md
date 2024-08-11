# Guide-to-Assembling-and-Calibrating-Robot-Legs-with-3D-Printed-Components-and-Servos

Components:
6 Servos
Nails
3D Printed Parts:
Toe
Knee
Hip

Procedure:
Program the Servos:
Setup: Before assembling the robot legs we need to program the servos to bend 90 degree

code:
#include <Servo.h>  // Include the Servo library

Servo myServo;     // Create a Servo object

void setup() {
  myServo.attach(9);  // Attach the servo control to pin 9 (change if needed)
}

void loop() {
  // Sweep from 0 to 180 degrees
  for (int pos = 0; pos <= 90; pos++) {
    myServo.write(pos);            // Set the servo position
    delay(15);                     // Wait for the servo to reach the position
  }

  // Pause at 180 degrees
  delay(1000);

  // Move to 90 degrees
  myServo.write(90);
  delay(1000);  // Wait for the servo to reach 90 degrees

  // Pause at 90 degrees
  delay(1000);

  // Sweep from 180 to 0 degrees
  for (int pos = 90; pos >= 0; pos--) {
    myServo.write(pos);            // Set the servo position
    delay(15);                     // Wait for the servo to reach the position
  }

  // Pause at 0 degrees
  delay(1000);
}

Prepare the Toe Component:
Clean the 3D-printed toe component and ensure it is free of any support material.
Attach a servo to the toe. This servo will control the toe's movement, allowing it to flip by 90 degrees. Secure the servo in place using screws or adhesive.

Assemble the Knee Joint:
Clean and prepare the 3D-printed knee component.
Attach a servo to the knee joint. This servo will manage the bending motion of the knee. Position the servo for effective control of the knee's range of motion and secure it using screws or adhesive.

Install the Hip Joint:
Prepare the 3D-printed hip component.
Attach a servo to the hip joint. This servo will handle the movement of the leg at the hip, allowing for rotation and positioning.

Connect the Components:
Attach the toe to the knee. Align the servo’s output shaft with the toe’s attachment point, ensuring it can move freely.
Connect the knee joint to the hip, ensuring proper alignment and freedom of movement for the servos.

Test the Movement:
Power up the servos and test each joint's movement. Verify that the toe flips correctly, the knee bends as intended, and the hip joint provides the desired range of motion.
Make any necessary adjustments to the servo positions or attachment points to ensure smooth operation.
