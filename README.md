🦠 Flu Tweet Analyzer

CIT 5940 – Data Structures & Software Design
Author: Neysa Porter

What This Project Does

This program reads tweet data (either from a .json or .txt file), determines if a tweet is flu-related, matches it to a U.S. state based on its location, and counts how many flu-related tweets came from each state. It also logs all flu tweets with their corresponding state to a log file.

How It Works

The app is modular and organized into clearly defined classes:

Tweet Parsers – Load tweets from JSON or TXT formats into objects.

State Reader – Parses a CSV of state center coordinates.

Location Mapper – Matches tweets to their nearest state based on latitude and longitude.

Flu Detector – Detects flu-related tweets using regular expressions.

Analyzer – Tallies up flu tweet counts per state.

Logger – Writes matched flu tweets to a log file.

ConsolePrinter – Outputs sorted flu counts to the terminal.

All functionality is controlled via the Main class using command-line arguments.

Sample Output
California: 1  
Florida: 1  
Louisiana: 2  
New Jersey: 3  
Pennsylvania: 2  


And the generated log file might look like this:

New Jersey	This flu season is the worst yet.  
Louisiana	Feeling awful... might be the #flu.  

How to Run It

From the command line:

# Run with JSON file:
java -cp "out;json-simple-1.1.1.jar" edu.upenn.cit594.Main flu_tweets.json states.csv log.txt

# Run with TXT file:
java -cp "out;json-simple-1.1.1.jar" edu.upenn.cit594.Main flu_tweets.txt states.csv log.txt


Or if you’re using Codio, click:

✅ Run BasicTests to test functionality

✅ Run Your Program: JSON

✅ Run Your Program: TEXT

Testing

The BasicTests.java file contains automated tests to verify:

Output formatting

Flu keyword detection

Proper state mapping

Log file structure and accuracy

You’ll see console output for each test run and can manually inspect generated logs.

Folder Structure

Your project should be organized like this:

submit/
└── src/
    └── edu/
        └── upenn/
            └── cit594/
                ├── datamanagement/
                ├── processor/
                ├── ui/
                └── util/

Final Thoughts

This project gave me hands-on experience designing a clean, testable Java application from scratch using real-world data. I worked with file parsing, regex filtering, geographic calculations, and logging — all within a modular design that made the code easier to test and extend. It’s one of my favorite early projects for demonstrating core Java skills and software design principles.
