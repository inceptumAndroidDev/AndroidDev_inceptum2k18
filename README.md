**Note:**
```
Following text is just the guidelines for building the app.
You are expected to show your creativity to achieve the features and functionality of the app.
```
## Guidelines for making the app:

The app would contain 5 Activity and one fragment:

The 1st Activity will be the **MainActivity containing 3 Button** namely _Play, Score and Tv shows._

On click of these corresponding bottom a new activity will up.

**On click of Play** button a Dialog Box should ask for Player Name and after submitting the name QuestionsActivity should start.
* QuestionsActivity will contain:
    - Stop Button at top-right corner of Activity
        - onClick will show player name with score and store it in Db before exiting the Questionsactivity
    - Score (textView)  at the top left corner of Activity
        - Display the score of the player(+1 score for every correct answer)
    - Timer (text) placed in top middle of the activity
        - Initialize it with 2 minutes and keep  decreasing it by one second
        - When the timer reaches zero show the player name with score in a dialog Box, add the score to Db and exit the activity.
    - A seek-bar below these three views
        - Initialize it with 100% progress
        - Progress will keep decreasing every second as the timer decreases
    - A fragment below the seek-bar (All the content inside the fragment should be in cardView)
    - The fragment will contain the following:
        - A question with question number and 4 options (Radio Buttons) associated with it.
            - Question Example
                >
                    Q1: What's 7+4?
                        - 7
                        - 6
                        - 9
                        - 11
                    Q2: What's 2*3?
                        - 4
                        - 6
                        - 8
                        - 10
        - Submit Button: clicking on it should do the 3 things:
            - 1. shows a toast telling if the answer is correct or incorrect
            - 2. update the score at the top left corner
            - 3. Show the next questions with

**Score Activity**  Contains the list of player name with their respective score.
* This data should be persistent and should be stored in the database.
* You can make use of RoomDb or SqlLite or any other Db of your choice.

**TvShow Activity** will show a list of TvShows using the tvmaze api. [Api docs](api.tvmaze.com)

* You will get the list of shows in JSON format [here]( http://api.tvmaze.com/shows)
* Display all the TvShow image and name in a recycler view
* onClick of the item of the list should open up the activity which shows the details of the selected TvShow.
* **TvShowDetailActivity** The activity should contain the following
    - 1. Image of the show
    - 2. TvShow Name
    - 3. Genres of the show
    - 4. TvShow Summery
    - 5. Average Rating of the show
    - 6. List of all the cast with (character name in Bold and actor/actress name along with Date of Birth)
## How will the points be rewarded?

**Total Points 150**

* **10 Points** Main Activity

* **50 points** Question Activity
    - 5 seek-bar and timer
    - 5 Score of the Player
    - 5 stop button and its functionality
    - 10 fragment
    - 5 random question and its random options
    - 5 submit button and it's functionality
    - 5 material design and creativity
    - 10 clear code
* **30 points** Score activity
    - 15 implementing SQLite or RoomDb or any other Db for data persistence
    - 5 List with each item having player name and score
    - 5 Using recycler view to show data
    - 5 Material design
* **60 Points** API fetching
   - 20 Fetching data from API
   - 10 Displaying data in prorper manner
   - 15 Tv show detail Activity containing(image, show name , summery , genre, avg. rating)
   - 5 Cast list in TvShow details.
   - 5 caching of TvShow Detail Activity data.
   - 5 Architecture followed for this part( eg: MVP, MVM)
   - 5 material design
**Screenshot for QuestionsActivity***

![small screen](https://user-images.githubusercontent.com/20511163/46569546-5852a280-c974-11e8-9558-073800ffd928.png)
