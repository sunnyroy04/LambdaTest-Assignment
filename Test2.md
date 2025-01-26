echo "# LambdaTest-Assignment`n`n## Task 2: Prefer using Command Line Terminal/PowerShell`n`n### 1. On Your Machine, Create a File Named test.sh`n- Created the file **test.sh** in my device at `C:\Users\sunny\Desktop`." > task2.md
echo "`n#### Create the New Script:`" >> task2.md
echo "`n- Use the following commands to create the **test.sh** file:`" >> task2.md
echo "`n  \`\`\`bash`n  echo '#!/bin/bash' > test.sh`n  echo 'echo \"Hi from Android!\"' >> test.sh`n  \`\`\`" >> task2.md
echo "`n### 2. Push the Script to the Emulator`" >> task2.md
echo "`n#### Step 1: Open PowerShell`" >> task2.md
echo "`n- Open PowerShell and navigate to the Android SDK platform-tools directory:`" >> task2.md
echo "`n  \`\`\`powershell`n  cd C:\Users\sunny\AppData\Local\Android\Sdk\platform-tools`n  \`\`\`" >> task2.md
echo "`n#### Step 2: Start Emulator`" >> task2.md
echo "`n- Make sure your emulator is running. You can start it with the following command (replace **DemoAndroid14** with your emulator's name):" >> task2.md
echo "`n  \`\`\`powershell`n  emulator -avd DemoAndroid14`n  \`\`\`" >> task2.md
echo "`n#### Step 3: Push the **test.sh** Script to the Emulator`" >> task2.md
echo "`n- You can use the **adb push** command to copy the **test.sh** file to the emulator's file system:`" >> task2.md
echo "`n  \`\`\`powershell`n  adb push C:\Users\sunny\Desktop\test.sh /data/local/tmp/`n  \`\`\`" >> task2.md
echo "`n### 3. Execute the Script on the Emulator`" >> task2.md
echo "`n- Once the script is pushed to the emulator, run the following command to execute it:" >> task2.md
echo "`n  \`\`\`powershell`n  adb shell sh /data/local/tmp/test.sh`n  \`\`\`" >> task2.md
echo "`n- You should see the output:`" >> task2.md
echo "`n  \`Hi from Android!\`" >> task2.md


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
