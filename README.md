🦠 Flu Tweet Analyzer

CIT 5940 – Data Structures & Software Design
Author: Neysa Porter

What This Project Does

This program reads tweet data (either from a .json or .txt file), figures out if each tweet is about the flu, matches it to a U.S. state based on its coordinates, and then counts how many flu-related tweets came from each state. It also creates a log file that lists each flu tweet along with the state it was matched to.

How It Works (Behind the Scenes)

The project is broken up into small, focused classes that each handle one job:

Tweet Parsers: Read tweet data from different formats (JSON or text) and convert them into a standard format.

State Reader: Reads the CSV file of U.S. state center coordinates.

Location Mapper: Figures out which state a tweet belongs to based on its latitude/longitude.

Flu Detector: Uses a regex to check if a tweet mentions the word “flu” or “#flu”.

Flu Analyzer: Counts how many flu tweets are mapped to each state.

Logger: Saves flu tweets to a .log file for future reference.

Console Output: Prints the final results to the terminal in alphabetical order by state.

Everything is tied together in the Main class, which takes 3 command-line arguments: the tweet file, the state file, and the log file.

Sample Output
Arkansas: 1  
California: 1  
Florida: 1  
Louisiana: 2  
New Jersey: 3  
Pennsylvania: 2  


It also generates a log file like this:

New Jersey	This flu season is the worst yet.  
Louisiana	Feeling awful... might be the #flu.  

How to Run It

From your terminal:

# For JSON input:
java -cp "out;json-simple-1.1.1.jar" edu.upenn.cit594.Main flu_tweets.json states.csv output.log

# For text input:
java -cp "out;json-simple-1.1.1.jar" edu.upenn.cit594.Main flu_tweets.txt states.csv output.log


Or if you’re using Codio, just click:

✅ Run BasicTests to check correctness

✅ Run Your Program: JSON

✅ Run Your Program: TEXT

Testing

This project comes with a built-in test suite in BasicTests.java that checks:

Output formatting

Flu detection logic

Whether log files are being written correctly

State mapping accuracy

You’ll see test results in the console and can manually inspect the generated log files.

Submission Structure

Your submission folder should look like this:

submit/
├── src/
│   └── edu/
│       └── upenn/
│           └── cit594/
│               ├── datamanagement/
│               ├── processor/
│               ├── ui/
│               └── util/
└── Neysa Porter.txt  ← academic integrity statement (outside src)

Final Thoughts

This project helped me reinforce key Java concepts like modular design, file parsing, regex matching, and working with coordinates. It also gave me practice designing programs that can be tested and extended easily, with clean separation of concerns.
