# How it works
Run the task and type a passphrase into the dialog that pops up. The passgen task takes your input string,
appends a unique salt string to it, and then generates a hash. The resulting hash is then
base91 encoded so that it uses all uppercase and lowercase letters, numbers, and standard
symbols.  A subset of 15-100 (default is 40 and can be changed in preferences) characters
is picked from the base91 encoded hash and then placed in your clipboard to be pasted into
a password field.

Every time you use the same input string, you will get the same result from the passgen
task. This allows you to use an easy to remember passphrases to generate lengthy,
complicated passwords that no one can reproduce unless they know your passphrase, salt,
and method of generating passwords.

# Installation
1. Install Tasker if you haven't already https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm
2. Copy or download PassGen.tsk.xml to your Android device
3. Import the task into Tasker by long pressing the Tasks tab
4. Set your salt to a random string
5. Run the task to generate passwords
6. (Optional) Using an app like [QuickTask](https://play.google.com/store/apps/details?id=com.balda.quicktask) you can put a shortcut to PassGen in your Quick Settings tiles

# PassGen for Windows
You can also use the same method of password generation on your Windows computer by installing my [Hain plugin](https://github.com/jhotmann/hain-plugin-passgen). Make sure to use the same salt for both (this plugin will generate a random salt that you can use for both). 

## Links to Libraries I Used
Skein hash https://github.com/drostie/sha3-js
Base91 https://github.com/mscdex/base91.js
