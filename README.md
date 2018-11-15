# codelouisville2018python
Final project for the September 2018 

2018PythonProject README , MTG GRN FLAVOR TEXT ANALYZER

Description:

I have developed a  Python script which analyzes the length of the flavor text included on Magic cards in a given set and compares them for each particular color on the color pie. What does this accomplish as a Magic player? Nothing! Unless, of course, you're interested in creating a deck with cards that have more or less useless verbiage. This tool could be easily modified to compare more pertinent statistics on cards, but in its infant stage I couldn't think of anything better to compare.

Project Contents:

QuickstartGuide.txt: A quick, step-by-step guide on how to run the script properly. Tired of this snarky README file? Go look at that for directions instead, you robot!

README.md: This file. Enough said.

2018PythonProject.ipynb: Python script consisting of the bulk of the project. Run this in Jupyter Notebook after placing it and the database into Jupyter Notebook's current working directory to execute the script.

workingdirectory.ipynb: Not sure where your current working directory is? Don't want to copy/paste 2 lines of Python into Notebook? Run this script to find out! In my testing it's always been the home directory but I'm not familiar enough with Notebook to say that's always the case.

cardtable.db: The database provided with the GRN cards preloaded into it. Unfortunately the web scraper I used to gather the data would not create a CSV file in a format readable by pandas, so I was forced to create my own database. It begins with a single table named "Ncards". To show my Python database manipulation prowess, my script creates a new table in cardtable.db named "pulledcards" and extracts the required information into there. The database should only contain table "Ncards" when downloaded from GitHub, but should show another table "pulledcards" after execution. (NOTE: I used SQLiteStudio (3.2.1) to test this. In order to show any change by my script to the database, I was forced to remove the database from SQLiteStudio and add it again. I could not figure out how to refresh the database within the program itself).

How it works:

To use the tool, simply drop it into the working directory for Jupyter Notebook along with the provided database.  If you are unsure what your working directory is, you can find it by running workingdirectory.ipynb in Notebook, or by copy/pasting the following Python code into Notebook:

import os
print(os.getcwd())

The current database consists of Magic Cards from the latest set, Guilds of Ravnica, but could be substituted with past/future Magic sets. The script takes the data and pulls the necessary information into a new database table. The script uses the new table to group cards by their individual colors and plot them on a boxplot in order to compare their distributions by color.
That's it! It's an extremely simple program but I believe it checks off all the requirements for our class.

Special Thanks to: 

The guy who wrote the Gatherer Extractor. It was by far the data source I found for all current Magic: The Gathering cards. Also, your janky .csv files forced me to apply a couple extra steps, which reinforced some of the learning done in this class.
