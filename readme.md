# Android SMS Extractor
With this Python script you can extract all SMS messages from the SQLite database of the `com.android.messaging` app. The extracted SMS messages will be displayed on `stdout` as readable plain text sorted by conversation.

## Usage instructions
1. Enable USB debugging in the developer options of your Android.
2. Enable "Root debugging" in the developer options of your Android.
3. Connect your Android to your PC and (re)start ADB in root mode:  
   `$ adb root`
4. Pull the corresponding database file to your PC:  
   `$ adb pull /data/data/com.android.messaging/databases/bugle_db .`
5. Pass the path to the extracted database file to this script:  
   `$ android-sms-extractor bugle_db`

**IMPORTANT:** This script has been written in 2019 when I needed a quick solution to export all SMS from my Android device (*OnePlus X*) running *LineageOS 14.1*. This script was later in 2022 also successfully tested with the SMS database of `com.android.messaging` in *LineageOS 17.1*. If it also works for you: Good! If not: I'm sorry!
