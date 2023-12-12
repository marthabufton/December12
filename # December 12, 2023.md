# December 12, 2023
## Scoping review methodology (knowledge synthesis)

1. Develop search terms.
2. Search in relevant databases.
3. **Generate** an initial list of potential sources (e.g., CVS file from Omni).
4. **Screen** this initial list for duplications and remove duplicated sources.
5. Develop inclusion and exclusion criteria (e.g., publication date, keywords)
6. **Screen** titles and abstracts of articles from initial list of sources for eligibility.
7. **Exclude** those sources that do not meet the inclusion criteria.
8. Chart the data or details about the articles on the initial list of included sources.
9. Conduct a manual (hand) search of relevant journals and reference lists for additional sources.
10. **Screen** these sources for eligibility based on the inclusion criteria.

**Data problems**
*Clean daata*: text (import, open, split, tokenize)
*Analyze data*

1. Screen and exclude duplicates: is this a form of cleaning data? (need conditions and a loop to iterate a list to find the data that should be excluded.)
2. Screen and exclude ineligible sources.

**Questions**
1. Do you need to "cast" or change an integer (number) to a string (text) or vice versa?
2. How do I structure the sections of the code: do I start with Pandas (because starting with CSV) or do I start with Natural Language Toolkit (NLTK)?
3. Do you need to be familiar with the spreadsheet before starting to clean it? For example, do you need to know that there is data that is "not a number"?

**Map to Python**

| **Scoping method**                        | **Python code**              |
| -----------                               | -----------                  |
| Screen for duplicates                     | split, tokenize,loop, if/else,
  (working with CSV?)                         to compare strings,tokenize, stopwords                    |
| Screen abstracts                          | loop, if/else,               |
  Do we want to replace NaN with something?
  Do we want to put content in lowercase for text analysis?
| Exclude ineligible sources                | Date, no keywords            |






**Note** will have to import Pandas and Natural Language Toolkit (NLTK) to work with both numbers and text.

Condition (screening)
1. Create variable for publication date
   1. Integer for publication date (number)
   Pubdate == 2010

if pubdate >= 2010
    print(pubdate)
else 
    print("Excluded too old")


**Python resources**
1. *Python standard librarires:* https://docs.python.org/3/library/index.html
2. *Natural Language Toolkit:* https://www.nltk.org
3. *Best Python libraries 2023*: https://www.mygreatlearning.com/blog/open-source-python-libraries/
4. Pandas: enables the provision of easy data structure and quicker data analysis for Python. For operations like data analysis and modeling, Pandas makes it possible to carry these out without needing to switch to more domain-specific language like R. The best way to install Pandas is by Conda installation.

**Basic input and output structure** for solving a problem in Python

*Input*
1. Import functions.
2. Create variables for files to be analyzed. Remember: choose style and use consistently.
3. Include other elements according to type of analysis (textual or  numerical).
4. Open a file (e.g., a text or CSV file).


*Output*
1. Open file.
   1. full_text = open(filepath_of_text, encoding="utf-8").read().lower()
2. Create a list from strings (split).
3. Clean the data. For example, include only relevant columns in a CSV and rename the columns with clearer/more intuitive titles; and clean up data in these columns if needed (e.g., what if cells are blank or Not a Number [NaN]). 
4. Set conditions (if/else, which can involve comparison operators [T/F])
5. A loop to "iterate" or repeatedly look over the list for data to be excluded.
6. Final output.


Task from Coding for the humanities (already have NLTK and Pandas)

 *Key point*: Data cleaning is not a neutral activity.

1. Import CSV into a dataframe.
2. Create a variable to store all the text.
3. Extract text from a single column in the dataframe.
   1. Call the column by name (may already have changed the name of the column).
   2. Make sure the data is in strings and cast as a list.
4. Tokenize the content.
   1. 
5. Refine stopwords list.
6. Which words to include and exclude, and why?
7. Create a list of words and count the frequency of the words. 
