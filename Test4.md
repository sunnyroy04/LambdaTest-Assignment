# LambdaTest-Assignment

## Task 4

### 1. Write a Script to Perform the Whole Steps

#### Emulator Creation, Launching Virtual Device, and Performing Task 2 (Task 1 can be skipped)

```bash
#!/bin/bash

# Constants
EMULATOR_NAME="DemoAndroid14"
SDK_PATH="C:/Users/sunny/AppData/Local/Android/Sdk"
AVD_PATH="$HOME/.android/avd"

# Step 1: Create an Android Virtual Device (AVD)
echo "Creating AVD..."
$SDK_PATH/emulator/emulator -avd $EMULATOR_NAME -no-snapshot-load &

# Wait for the emulator to start
echo "Waiting for the emulator to boot..."
adb wait-for-device

# Step 2: Launch the emulator
echo "Launching the emulator..."
$SDK_PATH/emulator/emulator -avd $EMULATOR_NAME &

# Step 3: Perform Task (Open Firefox in the emulator)
echo "Opening Firefox in the emulator..."
adb shell am start -n org.mozilla.firefox/.App

echo "Emulator setup complete. You can now use it for testing."
