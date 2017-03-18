# LeapSign
Leap Sign is working towards providing individuals who cannot speak with the means to communicate in an efficient, cost-effective manner.

### Basics
"LetterChooser.java" runs through these steps:

1. Uses the Leap Motion Sensor to identify the five fingers on a hand.
2. Creates vectors for each finger and returns the extention of each finger as a value.
3. Takes the vector values and compares it to our inputed requirements for various letters.
4. Determines which letter has been signed and sends the word to "LeapSign.java"

"LeapSign.java" runs through these steps:

1. Imports various requirements (Color, File, JPanel, etc.)
2. Recieves the letter from "LetterChooser.java" and appends it to a word.
3. Performs predictive analysis using the the current word based on a dictionary.
4. When a space has been signed, the word is analyzed and the program determines if a weather module is needed.
5. While recieving each letter, it is sending each letter and three possible predictions to the "Leap Sign Interface" using Firebase

"Leap Sign Interface" runs through these steps:

1. Recieves each letter and three predictions from "LeapSign.java" through FireBase and displays each letter with each predicted word.
2. Allows for the word to be autocompleted when a predicted word is chosen and relays back the information to "LeapSign.java".
3. Displays the weather module if the word "weather" has been signed.
