# Python-Reading-from-a-text-file
Examine the WordCount project.

In the Project pane, double-click wordsEn.txt.

Scroll down, and quickly scan the words in this file.


This file contains more than 100,000 English words, each of which is on a separate line. This is the word list. Only the words that are contained in this file will be counted within the manuscript.

From the Project pane, open and examine empty.txt and small.txt.

These manuscript files have been provided for testing during development.
The empty.txt file is useful to see what would happen if an empty manuscript file were analyzed.
The small.txt file is useful to verify that the program produces expected word counts. In this file, there is 1 instance of "one", 2 instances of "two", and so forth. Because it is small, it takes little time to load, which is convenient during development, when you may run a program many times to test code that you're adding.
Note: When developing and testing a program, it is helpful to have good testing data. Create various data sets that enable you to verify correct program logic and behavior, and that the program can deal acceptably with bad input.

From the Project pane, open and examine bartleby.txt and open-boat.txt.

These are normal manuscripts you can also use for testing.

From the Project pane, open large_file.txt.

You may see a warning in PyCharm because this is a large file. This file can be useful for testing how the script would respond to opening a very large manuscript. In some situations, very large input files may consume a lot of memory and may cause your program to become unstable. You may want to limit the size of files the program allows.

Right-click one of the editor tabs, and select Close All.

Write code to read the manuscript file.

Open wordprocess.py for editing.

Delete lines 53 through 55, and position the insertion point at the end of line 52 as shown.

lhrsdc6r.jpg You will add code here to read the input file.

Press Enter and enter the code as shown.


Lines 53 and 54 get the input file's size and display it in the output.
Line 55 opens the input file for reading.
Line 56 displays a message to keep the user informed, since reading a large file may take several seconds.
Line 57 reads the entire text file, then splits its words into a Python list to make it easy to analyze each word. The list is stored in the WordCount object's words_in_manuscript property.
Line 58 closes the file.
Line 59 displays a progress message to the user.
For the moment, you are not concerned with handling error situations. The read_input_file method will always return True. Later, you will add code to return False if an error occurs reading the file.
Write code to read the word list.

Delete lines 41 and 42, and enter the code to read the word list as shown.


Line 41 opens the wordsEn.txt file for reading.
Line 42 reads the entire text file, then splits its words into a Python list, which is stored in the WordCount object's wordlist property.
Line 43 closes the file.
Test the program.

In the Project pane, right-click wordcount.py and select Run 'wordcount'.

Note: Though wordprocess.py contains the class you are editing, remember that the wordcount.py script contains the program that actually uses this class. So you need to run wordcount.py to test the program.

When prompted for the file to analyze, enter open-boat.txt


When you provide only the file name (not including a directory path), the file is read from the current directory. By default, the current directory is the directory the script is running from, so in this case, the file is read in from the project directory.
The file size is shown, and the manuscript is read in from the file.
At each of the remaining two prompts, enter y to respond.

Verify that the read operations worked and the results were printed to the console.


You can scroll up to see lines that have scrolled out of view. The most frequently appearing words are summarized at the top of the report.
