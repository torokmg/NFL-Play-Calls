# NFL Play Call Prediction Modeling

## Business Case
When a defensive coordinator is deciding on what play to call, he'll typically use probability distribution charts of what the other team likes to run on certain downs, distances, formations, etc. These charts are good guidelines but do not encompass all of the features together. In today's NFL, the play clock is only 40 seconds and an NFL offense typically only uses about 25 seconds of that time to decide on a play and hike the ball.  This time is only getting shorter as more teams adopt a hurry-up offense.  Therefore being able to quickly make a prediction on a play call is extremely important.  There just is simply not enough time between plays for the coach look at each invidual chart. I beleive that using machine learning to model the play data in aggregate would solve both of these problems, leading to coaches being able to more adequately predict what kind of play was coming.  

## Business Value
There are two applications of the machine learning model to NFL teams:

* **Game Prep** - Each week before a game, every single coach is creating a game plan for their team to use against their upcoming opponent.  Most of this is currently accomplished through watching and breaking down film of the opponent.  Using the model would uncover team-specific tendencies of the upcoming oponent, which a human watching film could not pick up on their own.  This would allow a defensive coach to create a game plan that better incorporates the behavior of that specific opponent.

* **In-Game** - As stated in the buisness case, the main issue with current play prediction is lack of time.  There is simply not enough time to factor in every single aspect of an upcoming play.  A model could easily be trained on the opponent's data before a game, and then a prediction could be made in a matter of seconds between plays. 

Both of these applications should put the team into a much better chance to win the game and eventually a Super Bowl.  A Super Bowl can provide teams with the ability to command higher ticket prices, consistently fill more stadium seats and suites, sell more concessions, and charge more for sponsorships.  It can also provide an increase in name recognition and more international fans, which will lead to more revenue from merchandise sales.

## Obtaining Data
My first step was to obtain the data I would use to create my model.  I used two sources for my data:

- https://github.com/guga31bb/nflfastR-data
- https://www.pro-football-reference.com/

The data used from GitHub was an adaptation of the popular nflscrapR to enable it to be used with Python coding language.  
The data used from Pro-Foootball-Refrence was scraped using a WebScraper that I had built.

## Exploring Data

I wanted to explore the data to try and understand which features influence the probability of a play the most.  I also wanted to take a look at the distribution of play calls amongst the various teams in the league.

### NFL Offense Plays Attempted 
<img src="https://github.com/torokmg/NFL-Play-Calls/blob/master/Images/team_att_off.png" height="500" width="500"> 

### NFL Defense Plays Faced
<img src="https://github.com/torokmg/NFL-Play-Calls/blob/master/Images/team_att.png" height="500" width="500">

## Model

The final model, which was modeled on the Philadelphia Eagles, wound up having a 71.35% accuracy score.  When using this model on every NFL team, I was able to obtain an accuracy score of 78.2% for the NY Giants.

<img src="https://github.com/torokmg/NFL-Play-Calls/blob/master/Images/all_teams.png" height="500" width="500">

## Conclusion

In summary, this project focuses on the development of a machine learning model for predicting NFL plays.  By running various models and adjusting the hyperparameters, I was able to obtain an accuracy of 71.35% for the Eagles, and a score as high as 78.2% for the Giants.  Whether or not a team was in a shotgun formation proved to be the most important feature.  Because of this, I feel there is definately a potential to increase the accuracy by obtaining and modeling in other formation data. Unfortunately this infromation is not publically available, but it is something that an NFL team would have access to. I believe this model can be useful as a decision-aid in NFL games due to how quickly it make predictions on play types once it is trained on an opponents data.  It is also a great tool for creating a game plan each week for a specific opponent.
