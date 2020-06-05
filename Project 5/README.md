##  WeRateDog Tweet Analysis

### Visualization report 
**Graph 1 : Confidence rate**
In this bar chart show the rate of each picture p1,p2,p3.P1 has the highest possibility of confidence rate which is about 60 percent. But P2 and P3 show markedly lower rate of confidence.I used barplot to compare the rate of confidence rate. In the beginning I built list,which includes the mean of confidence rate p1,p2,p3 and then that list was applied the variable of height factor. Height factor decide the height of column. Next part for loop was implemented. This function plays a important role to annotate each value of mean direct on the column.

**Graph 2 : Timeline of Hour and Number of tweet**
This graph shows the user trends of twitter especially the timeline of tweet result.The most important process that you have to know is using datetime library. Datetime library supplies classes for manipulating dates and times.I extracted Hour,Minute,Second, from timestamp. This column has not only time but also date data.And then I plotted time series along hour column.I added also Countcolumn in order to count the number of tweet in each timezone.We can get easily which time people post dog picture mostly.

**Graph 3 : Number of rating numerator**
Last visualization is about depiction of counting rating_numerator.I made a new dataframe,which contains rating_numerator samller than 10.because more than rating 10 is minor of whole column.So the bar chart shows from rating 1 to 10.As you can see over 50% of pictures got perfect score.


### Wrangle report
This report help readerto understand easiy what I was trying show in this project.The dataset that I wrangled(and analyzed and visualized)is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs.We are handling 3 different type of files with different python libraries.

The first step that I did for wrangling was gathering.Gathering is collecting the data so that we can assess and clean the data. So gather is very important step.If we make a mistake we can't go one step further.

#### 1.Gathering
We have 3 differnt type of files, namely csv,tsvand JSON.We can load csv with pd.read_csv(""). For tsv we do same as csv but we have to add seperator sep otherwise all data are save in one column.For JSON we need first special library(called tweepy) in order to query twitter_api.Beside import json is required because through tweepy queried table is written by json. So as you can see in the jupyter file we got json file called tweet(you can define whatever you want,I just took eaier name).

We need ID,retweet_count,favorite_count from tweet file. So I used for-loop and dictionary to get relevant informations.In the end we saved as twitter_api.csv.

#### 2.Assessing
Aseessing a data is a process of measuring the table in many differnt ways.There are the programmatic assessment methods in pandas that I used in this project.

- head(DataFrames and Series)
- tail(DataFrames and Series)
- sample(DataFrames and Series)
- info(DataFrames only)
- describe(DataFrames and Series)
- value_counts(Series only)

And then  figured out the quality issues and tidiness issuse of each files.

#### 3.Cleaning
As you can see the title this part is cleaning session.Above we defined quality and tidness issuse.Now it's time to solve issues.To lose the problem we have to take 3 steps to built a better structure.

- Define : Validity / Consistency / Accuracy / Completness
- Code
- Test
