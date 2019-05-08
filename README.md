### Data Question 1
#### A guided exploration of UN data

##### In-class practice 1:
1. create a folder called `data` in your local `Data Question 1` repository.
88.	Download two CSV files and place them in this folder:

    a.	Gross Domestic Product (GDP) per capita http://data.un.org/Data.aspx?d=WDI&f=Indicator_Code%3aNY.GDP.PCAP.PP.KD **DO NOT APPLY ANY FILTERS**
     - rename the file to gdp_percapita.csv
     - open it with a text editor (not excel) and take a look

    b.	Percentage of Individuals using the Internet http://data.un.org/Data.aspx?d=ITU&f=ind1Code%3aI99H  **DO NOT APPLY ANY FILTERS**
     - rename the file to internet_use.csv
     - open it with a text editor (not excel) and take a look

2.	Launch a Jupyter Notebook. 
 - _*You are likely to get errors along the way. When you do, read the errors to try to understand what is happening and how to correct it.*_
  - Use markdown cells to record your answers to any questions asked in this exercise. On the menu bar, you can toggle the cell type from 'Code' to 'Markdown'.

3.	Import the required packages with their customary aliases as follows:

    `import pandas as pd`   
    `import numpy as np`  
    `import matplotlib.pyplot as plt`  
    `import seaborn as sns`

4.	Use the `%matplotlib inline` command so that your plots show in the notebook _without_ having to call `plt.show()` every time.
5.	Using the pandas `read_csv()` function, read the GDP dataset into your notebook as a DataFrame called `gdp_df`. Take a look at the first 6 rows.
6. Repeat for the internet use dataset. Call this DataFrame `internet_df`. Take a look at the first six rows.
7. Look at the shape of each dataframe - how many rows, how many columns.
8.	Take a look at the data types for the columns in each table.
9. Take a look at the last 10 rows of each dataset in turn.
10.	Drop the 'value footnotes' data (column) from both datasets. Check that this worked as expected.
11.	Change the columns for the GDP Per Capita data frame to ‘Country’, ‘Year’, and ‘GDP_Per_Capita’.
12.	Change the columns for the Internet Users data frame to ‘Country’, ‘Year’, and ‘Internet_Users_Pct’.
13.	Merge the two DataFrames to one. Merge all rows from each of the two DataFrames. Call the new DataFrame `gdp_and_internet_use`.
14.	Look at the first five rows of your new data frame to confirm it merged correctly.
15.	Look at the last five rows to make sure the data is clean and as expected.
16.	Subset the combined data frame to keep only the data for 2004, 2009, and 2014. Check that this happened correctly.
17.	Create three new data frames, one for 2004, one for 2009, and one for 2014. Give them meaningful names that aren't too long.
18.	Which country had the highest percent of internet users in 2014? What was the percentage? (Try typing the first 3 letters of your DataFrame name and hitting the tab for auto-complete options).
19.	Which country had the lowest percent of internet users in 2014? What was the percentage?
20.	Repeat for 2004 and 2009.
21.	Which country had the highest gdp per capita in 2014? What was the gdp per capita?
22.	Which country had the lowest gdp per capita in 2014? What was the gdp per capita?
23.	Create some scatterplots:  
    a.  2004 Percent Using the Internet vs gdp per capita  
    b.	 2009 Percent Using the Internet vs gdp per capita  
    c.	 2014 Percent Using the Internet vs gdp per capita  
24.	Are there differences across years? What do the plots tell you about any relationship between these two variables? Enter your observations as a markdown cell.
25.	Look at the distribution of gdp per capita values for 2014. Is it unimodal?
26.	Look at the distribution of Internet Use for 2014. Is it unimodal?
27.	What are the top 5 countries in terms of internet use in 2014?
28.	Create a data frame called top_5_internet from the combined data frame that has all three years for these 5 countries. You should have 15 rows. Check that this is true.
29.	Create a seaborn FacetGrid to show the internet usage trend over time for these 5 countries. Which country had the greatest growth between 2004 andd 2014? If you have time, try to figure out how to fix the plotting issue with Bermuda.
30.	Repeat the steps above to look at the trend for 5 countries with the lowest 2014 internet usage. WHich country has consistently had the least internet use?
31.	Get the top 5 countries for 2014 in terms of GDP per capita; create a dataframe to look at 10-year trends in gdp per capita. Use a seaborn facet grid for this.
32. Repeat this one more time to look at 10-year trend for the bottom 5 countries for 2014 in terms of GDP per capita.
33.	Is there anything surprising or unusual in any of these plots? Searching on the internet, can you find any possible explanations for unusual findings?


### In class practice 2:
1.	Import stats from scipy:

     `from scipy import stats`

2.	Print the docstring for stats:

     `print(stats.__doc__)`

    Try shift + tab + tab to see the documentation too!

3.	Create a set of 500 randomly generated numbers called iq_scores with a mean = 100 and standard deviation = 15.
4.	Using the example at the bottom of this webpage as a guide (https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.random.normal.html), plot the distribution of your iq_scores.  Does it look normally distributed?
5. Create a boxplot of these iq_scores

### Bonus exercises:
1.    Download another data set from the UN data (http://data.un.org/Explorer.aspx) to merge with your data and explore.
2.    Look through the bokeh gallery (https://bokeh.pydata.org/en/latest/docs/gallery.html#gallery) and if time allows create a bokeh visualization using the UN data.
