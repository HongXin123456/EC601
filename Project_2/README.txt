MVP (Minimum Valuable Product)
1. Allow users access to selected a Twitter account
   1. Use Twitter API to retrieve a Twitter user’s posts up to 20 posts
2. Analyzing the sentiment of posts by using Google API

User Stories
1. Reporters, social media researchers, or students
   1. A group of people who want to analyze the sentiment of the tweets of a politician, a celebrity, or anyone

Modular design
1. User input 
   1. Twitter username
2. Twitter API
   1. Retrieve one's posts base on user’s input
3. Google API
   1. Retrieve a sentiment analysis result from Google
4. Results
   1. Show the score and magnitude at sentences level and document level


Twitter API:
Explain 4 tests and the results of each test. 
1. Get the timeline of a user: this section of codes is used to get the 20 most recent statues posted from a user, JessicaXinH who only has 18 statue posts. The output is stored in a text file. By running the first section, for example, you will see the first information is this user comment under HTSPedicini’s post on Monday, May 05, 2014. By looking at the text file, we can observe that the last time that this user post something was a few years ago. I also print out the top 20 most recent statuses for reference.
2. Get the trending tweets of all countries: this section of codes will fetch the locations that Twitter has trending topic information for. In my codes, I did not specify the names of countries, so the codes will return all countries’ trending topics. The output is stored in a JSON file. I print out the top 10 trending locations. It seems like Canada is very popular.
3. Get the trending tweets of a city: Similar to section (2), this section of codes will look for the latitude and longitude of a city, such as Boston, that is entered by users. Then, the codes will use the latitude and longitude to find the trending tweet in that location. The result is output into a JSON file.
4. Count number of hashtags: The user randomly selects and enters a keyword, such as Apple. The codes will download tweets that contain this keyword. I printed out a tweet that was created on Monday, September 27. This user mentioned “Apple Music” in his/her tweet.

Google API:
Explain a test and result.
This code analyzes the sentiment of a given text file and analyzes the sentiment of each sentences.
The program will return a score and a magnitude for each analysis.

