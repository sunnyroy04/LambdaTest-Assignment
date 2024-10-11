# Task 2: Prefer using Command line Terminal/PowerShell
# 1. On your machine create a file named test.sh [ Document all the steps performed ]
Created file test.sh in my device at cd C:\Users\sunny\Desktop
# Create the New Script: Use the following commands to create the test.sh file:
echo '#!/bin/bash' > test.sh
echo 'echo "Hi from Android!"' >> test.sh

# b Step 2: Push the Script to the Emulator
Open PowerShell: If you haven't already, open PowerShell and navigate to the Android SDK platform-tools directory:

cd C:\Users\sunny\AppData\Local\Android\Sdk\platform-tools
# c start emulator 
Start the Emulator: Make sure your emulator is running. You can start it with the following command (replace  DemoAndroid14 with your emulator's name):

 .\emulator -avd DemoAndroid14
# d. Now push or copy the test.sh script in emulator from you machine
 Push the New Script to the Emulator: Once the emulator is running, push the hello_android.sh script to the /sdcard directory:

.\adb push C:\Users\sunny\Desktop\hello_android.sh /sdcard/


# e. Now open the shell in Android Emulator
.\adb shell

# f. Change the permission of the file to 755
chmod 755 /data/local/tmp/hello_android.sh

# g. Now run the test.sh script and share the Picture.
  output is 
emu64xa:/ $ chmod 755 /sdcard/test.sh                                                                                                          
emu64xa:/ $ sh /sdcard/test.sh                                                                                                                  
Hi from Android!
![Screenshot 2024-10-11 111404](https://github.com/user-attachments/assets/d4837efb-b6cb-46d6-88ac-3c607ce7d09c)
![Screenshot 2024-10-11 111505](https://github.com/user-attachments/assets/d047cae1-c0fe-43e9-938c-e3eb8c84dfbd)
