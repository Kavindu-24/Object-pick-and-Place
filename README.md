Smooth Dual Servo Motor Control via Serial Commands using Arduino

🧩 Description:
This Arduino sketch allows precise and smooth control of two servo motors using serial commands. The servos respond to commands ('1' to '5') sent over the Serial Monitor, executing predefined sequences for each command. Each movement is executed slowly for mechanical safety and visual clarity using the moveServoSlowly() function.

Additionally, the sketch initializes a TCS3200/TCS230 color sensor (though not fully used in this version) for potential integration with color-based decision-making in the future.

🚀 Features:
Control two servos (servo1 and servo2) smoothly using serial commands

Supports five unique motion sequences

Gradual movement using a custom stepping function

Basic setup for a color sensor (TCS3200-compatible)

Easily extendable for robotic grippers, pick-and-place arms, or object sorting

🛠️ Hardware Requirements:
Arduino Uno (or compatible board)

2x Servo Motors

TCS3200/TCS230 Color Sensor (optional, currently not active in code)

Serial connection via USB

🎮 Serial Commands:
Command	Description
'1'	Initial positioning (grip open/close)
'2'	Pick-and-place sequence with delay
'3'	Alternative positioning (lift and return)
'4'	Return to default state
'5'	Extended motion sequence with grip adjustment

🧠 How It Works:
Each servo movement uses the moveServoSlowly() function, which interpolates between the current and target angle in 1-degree steps with a short delay, creating smooth motion. The servo angles are tracked with global variables to ensure consistent movement updates.
