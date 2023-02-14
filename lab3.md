# -cse-15l-lab-report-week5
## Lab Report 3
### Researching Commands For Find
### Command 1: 
**grep -n** this command searches a file and essentially returns the lines where the specificed string is located in the text file.

**Example 1:**

**Command Line Argument:**
This command searches for the word travel in the file WhereToItaly.txt.
```
#code block
$ grep -n "travel" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:**
The lines are returned where the specified string "travel" is located on each line of the text file.
```
#code block
66:        Even the most free-spirited traveler can use a little help
78:        national travel agency for transportation, excursions, and hotel
81:        217) gives detailed practical guidance on the technicalities of travel
86:        buffs and travelers with plenty of time, patience, and curiosity. The
722:        especially the Greece he loved above all else — a travel notebook for
2081:        important for weary or hungry travelers, elegant 18th-century cafés.
3448:        Neapolitans are justifiably proud. For adventurous travelers looking
3846:        tempt travelers and aspiring photographers onto jutting crags high
3868:        roads to speak of, most travel is by foot up and down its endless
3955:        Mont-Saint-Michel after Bishop Aubert traveled to Gargano to collect a
```
**Example 2:**
**Command Line Argument:**
This command searches for the word "history" in the file HistoryDublin.txt.
```
#code block
$ grep -n "History" written_2/travel_guides/berlitz1/HistoryDublin.txt
```
**Output:**
The lines are returned where the specified string "travel" is located on each line of the text file. It seems to only appear once in line 6.
```
#code block
6:        A Brief History
```
***Source***: **[geekforgeeks grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)**

### Command 2:
**grep -i** this command searches for a string within a file, but it ignores case sensitivity. For instance, if the string used was "Hello" it would search the file for "HELLO", "HelLo", etc. As long as the letters are the same, the command will output it even if there is difference in capitalization with the string.
**Example 1:**
**Command Line Argument:**
This command searches for the word travel in WhereToItaly.txt.
```
#code block
$ grep -i "travel" written_2/travel_guides/berlitz1/WhereToItaly.txt
```
**Output:**
The output includes lines for the words travel that includes different capitlizations. Some new lines appear with the word travel since case sensitivity does not matter. Comparing it to the grep -n command, it seems that there are lines such as that did not show up earlier, showing up now.
```
#code block
Even the most free-spirited traveler can use a little help
        national travel agency for transportation, excursions, and hotel
        The Travel Tips section at the back of the book (see page
        217) gives detailed practical guidance on the technicalities of travel
        buffs and travelers with plenty of time, patience, and curiosity. The
        especially the Greece he loved above all else — a travel notebook for
        important for weary or hungry travelers, elegant 18th-century cafés.
        Fruit, is here. Travelers on their way to or from Rome will be
        Neapolitans are justifiably proud. For adventurous travelers looking
        tempt travelers and aspiring photographers onto jutting crags high
        roads to speak of, most travel is by foot up and down its endless
        Mont-Saint-Michel after Bishop Aubert traveled to Gargano to collect a
```
**Example 2:**
**Command Line Argument:** This command line argument searches for the word history in HistoryDublin.txt.
```
#code block
$ grep -i "History" written_2/travel_guides/berlitz1/HistoryDublin.txt
```
**Output:** The power of -i becomes more clear when searching for the word history in this file, as earlier it was clear that grep -n only returns one line, but running -i returns 4 lines. The variations of history is returned here with History or history. Since -i ignores case sensitivity any instance of history that shows up in the file is returned.
```
#code block
 A Brief History
        Irish history really begins with the arrival of the Celts around the
        history, for both the Irish themselves and civilization in general,
        struggle between England and Ireland that was to dominate Irish history
```
***Source***: **[geekforgeeks grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)**


### Command 3:
**Example 1:**
**Command Line Argument:**
```
#code block

```
**Output:**
```
#code block

```
**Example 2:**
**Command Line Argument:**
```
#code block

```
**Output:**
```
#code block

```
***Source***:

### Command 4:
**Example 1:**
**Command Line Argument:**
```
#code block

```
**Output:**
```
#code block

```
**Example 2:**
**Command Line Argument:**
```
#code block

```
**Output:**
```
#code block

```
***Source***:
