# Password-Generator-app
Password-generating software
I built this because I got tired of using "Password123!" for everything. SecureGen is a small Python tool (command-line and GUI versions) that spits out strong, random passwords in a couple of seconds.

What it does

Instead of just grabbing random characters and hoping for the best, it makes sure every password actually includes a mix of letters, numbers, and symbols — not one of those "accidentally all lowercase" passwords that random generators sometimes produce. It also uses Python's secrets module under the hood, which is the module actually meant for security stuff, not the regular random module people often use by mistake.

Features

Real cryptographic randomness (via secrets, not random)
You choose the length
You choose which character types to include — uppercase, lowercase, numbers, symbols
Always includes at least one of each type you pick
Can spit out a batch of passwords at once
Works from the terminal, or there's a basic point-and-click GUI if you'd rather not use the command line

What you need

Just Python 3.6+. Nothing else to install — it only uses built-in stuff. If you want the GUI and you're on Linux, you might need to run sudo apt install python3-tk first since tkinter isn't always included by default.

How to use it

For the command-line version, just run the script and answer a few quick prompts about length and character types. It'll ask how many passwords you want and print them out.

For the GUI, run the other script, set your length with the spinner, check off the character types you want, and hit Generate. The password shows up in a text box you can copy.

How it actually works under the hood

It figures out which character pools you want (lowercase, uppercase, digits, symbols)
Grabs at least one character from each pool you picked, so nothing gets left out
Fills the rest of the password length with random picks from everything combined
Shuffles it all so the "guaranteed" characters aren't sitting predictably at the start

A note on security

Everything happens locally — nothing gets logged, saved, or sent anywhere. If you're generating something important, I'd stick to at least 12-16 characters with everything turned on (uppercase, lowercase, numbers, symbols).
