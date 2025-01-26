# LambdaTest-Assignment

## Task 2: Prefer using Command Line Terminal/PowerShell

### 1. On Your Machine, Create a File Named test.sh
- Created the file **test.sh** on my device at `C:\Users\sunny\Desktop`.

#### Create the New Script:
- The following steps were followed to create the **test.sh** file:
  1. Opened PowerShell or terminal.
  2. Created a new file **test.sh** using the commands:
     - `echo '#!/bin/bash' > test.sh`
     - `echo 'echo "Hi from Android!"' >> test.sh`

### 2. Push the Script to the Emulator

#### Step 1: Open PowerShell
- Opened PowerShell and navigated to the Android SDK platform-tools directory by running the command:
  - `cd C:\Users\sunny\AppData\Local\Android\Sdk\platform-tools`

#### Step 2: Start Emulator
- Started the emulator using the following command (replacing **DemoAndroid14** with the emulator name):
  - `emulator -avd DemoAndroid14`

#### Step 3: Push the **test.sh** Script to the Emulator
- Pushed the **test.sh** file to the emulator by using the **adb push** command:
  - `adb push C:\Users\sunny\Desktop\test.sh /data/local/tmp/`

### 3. Execute the Script on the Emulator
- After pushing the script, executed it on the emulator with the following command:
  - `adb shell sh /data/local/tmp/test.sh`

- The output displayed on the emulator was:  
  `Hi from Android!`
