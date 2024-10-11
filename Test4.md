# Task 4:
# 1. Write a script to perform the above whole steps like Emulator creation , launching virtual device and Performing Task 2 [ Task 1 can be skipped ]

#!/bin/bash

 Constants
EMULATOR_NAME="DemoAndroid14"
SDK_PATH="C:/Users/sunny/AppData/Local/Android/Sdk"
AVD_PATH="$HOME/.android/avd"

 Step 1: Create an Android Virtual Device (AVD)
echo "Creating AVD..."
$SDK_PATH/emulator/emulator -avd $EMULATOR_NAME -no-snapshot-load &

 Wait for the emulator to start
echo "Waiting for the emulator to boot..."
adb wait-for-device

 Step 2: Launch the emulator
echo "Launching the emulator..."
$SDK_PATH/emulator/emulator -avd $EMULATOR_NAME &

 Step 3: Perform Task (Open Firefox in the emulator)
echo "Opening Firefox in the emulator..."
adb shell am start -n org.mozilla.firefox/.App

echo "Emulator setup complete. You can now use it for testing."

# 2. Push the code to Github along with Video and Screenshots.

   1. All the videos and phots has been post on my github having .md file
   First of all the header task is done in Readme.md file where i have create a step of android studio setup
   2. Task 1 in Task1.md file(Launched firefox and surf google.com and Lambdatest.com)
   3. Task 2 in Task2.md file(Created test.sh on my machine and transfered to Emulator sd card and changed mode)
   4. Task 3 in Task3.md file(Video of all the Process like  launching virtual device and Firefox Expolration and Script permission changing)
   5. Task 4 in Task4.md file (Shell scripting code for all the process like launching virtual device etc.)
   
