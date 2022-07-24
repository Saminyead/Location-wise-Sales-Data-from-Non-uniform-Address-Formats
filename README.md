Imagine you had a delivery business which delivered across mutliple cities in the United States. Now, you want to conduct an analysis of the performance of your 
business in different cities. Let's say for that, you choose Python. But, the delivery datas are in multiple CSV files, none of which have a separate 'City'
column. What you have to work with are just delivery addresses. How do you extract the city information from there? If all the addresses were written in a
uniform format - let's say "street-name, city-name, state-name zip-code" like in this dataset, then all you had to do was parse the string between the first and
the second comma. But what if they were not written in a uniform format? What if some addresses were written in the "street-name, city-name, state-name zip
code" format, while others were written in "house-number, street-name, city-name, state-name", and others in yet other formats?

With this in mind, this fork was created. The original files are from Keith Galli's exercise on Data Analysis using the Pandas library in Python available on <ahref="https://youtu.be/eMOA1pPVUc4">YouTube</a>.(Please read Keith_Galli_README.md for more information) In the exercise was a question -  which city had the
highest amount of sale in USD. His solution to it was to parse the string between the first two commas. This worked well for the purpose of the exercise, but I
figured, in real life, people use different number of commas in their addresses. So, what could be a solution to deal with non-uniform addresses?

In this fork, I try to explore 2 solutions to this problem:
1. Comparing our delivery dataset with a publicly available dataset containing the names of all US Cities. The US cities dataset used in this case, was taken
   from <a href="https://simplemaps.com/data/us-cities">simplemaps.com</a>. Free use of this dataset requires linking back to the page. This codes exploring 
   solution is in the notebook "Comparing_to_public_dataset.ipynb".
2. Using the Geopy library to query the addresses on popular geocoding services like Google Maps and OpenStreetMaps. To do this, you would need to make API 
   which may cost money. This is definitely more expensive than the above option, but if you have, adresses with missing city names - then this solution would
   be more suitable. The file for this will be added in a later commit.

Besides exploring these 2 solutions, I have one more objective in this project - to visualize some key figures using a web dashboard. 

If you wish to fork this repo, please feel free. 
