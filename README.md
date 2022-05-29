I created this fork Keith Galli's exercise on Data Analysis using the Pandas library in Python available on <a href="https://youtu.be/eMOA1pPVUc4">YouTube</a>.
(Please read Keith_Galli_README.md for more information) The inspiration behind this was a particular exercise task which asked which city had the highest amount of sale 
in USD. The way it was done in the video was to parse the string contained in the Purchase Address column between the first and the second comma. This worked because all
the addresses were in the format - 'street, city, state and zip code'. But sometimes we may find a dataset, where the address is not formatted in this convenient manner.
For example, some address may be 'house no., street, city, state', while others may be 'street, city, state, zip code.' This may happen when addresses are entered into 
the front end of a data entry application, as different people have different ways of writing addresses. This is where the Geopy library comes in handy, as it is used as a
client to check the address against popular geocoding services like OpenStreetMap, Google Maps, and others. The result is that, no matter what the format of the address is,
it can be used to gain exact address - coordinates, name of city, county, state etc, provided the address is a real one. 

I have run into two difficulty using geopy. 

The first is the Nominatim API used for OpenStreetMap only allows 1 request per second. At that rate, it will take about 2 days to go through the entire dataframe.

The second difficulty is that the Nominatim API will return a dictionary named 'address' containing the relevant information with indexes like house_no, road_no, county, city
and so on. If I wish to get the names of cities from each of the address, for some of them, the 'address' dictionary would not contain a city index, and in stead contain town.
Please check Geopy_In_Pandas_Dataframe.ipynb for further explanation. 

If you wish to work on this problem, feel free to fork and leave a pull request.