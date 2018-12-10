# BeFit | fitNessMod | Beat Saber v0.12.x+ supported
An IPA Plugin for BeatSaber to add a calorie counter/ tracker

## v0.2.0 coming soon! 
v0.1.x will continue to be updated until completed
### Inaccuracies in current algorithm v0.1.0
*Calorie Counts are nearly double what they should be. Next update will be using researched calorie counting methods called **METS**.*
### New Algorithm Psuedo (Will change based on most efficient process):
```float[] metsVals = new float[6];
 bool[] enabledMetVals = {true};
metsVals[0] = 3f; //Minimal Effort
metsVals[1] = 4f; //Minimal to some effort
metsVals[2] = 5f; //Trying Hard Difficulty up
metsVals[3] = 6f; //Hard putting towards effort | Expert moderate effort
metsVals[4] = 7f; //Expert putting towards effort | Expert+ moderate effort
metsVals[5] = 8f; //Expert+ putting towards effort
metsVals[6] = 9f; //Top of the leaderboard effort

  

if(Women){BMR = 655 + (9.6 x weight in kg) + (1.8 x height in cm) - (4.7 x age in years);}
if(Men){BMR = 66 + (13.7 x weight in kg) + (5 x height in cm) - (6.8 x age in years);}
difficulty = based on changes on movement considering both hands and headset relative to BMR

caloriesBurnedLast90FixedUpdates = ((metVals[difficulty] * 3.5f * weightInKiloGrams)/200)/60);
  
```

### What to expect with the new update?
**The plugin will ask for you to enter your:**
- [ ] weight *choose between metric or lbs*
- [ ] height *Height can be toggled off to use in-game height measurement. As of right now, not sure which will perform better*
- [ ] Age
- [ ] Gender

Expect new calorie counts to be around half of what they are now. 
The legacy counting algorithm will still be included and be able to be switch on in the new menu.



**Calorie counts may be *higher* or *lower* than what the users actually doing.**

*All calorie counting software/ devices are estimates and do not accurately represents calories burned!*

## Current Features
1.  [x] Count Song Calories    - Displays calories adding up as you play beat saber songs
2.  [x] Count Session Calories - Everytime you open beat saber, a new session starts from 0
3.  [x] Count Daily Calories   - Based on the current date. *Known Bug with playing during date changes*
4.  [x] Count All Calories     - Counts calories since mod has been installed. *Will most likely be removed, or by default hidden from main scren at later date.*
5.  [x] Last Song Played       - Shows calories from last song played.

## Future Improvments
Things to add:
* [ ] Calories based on vertical movment of headset
* [ ] ~~Larger distance between blocks has higher coefficient.~~
* [ ] A seperate menu composed of:
  * [ ] Toggle individual labels visible on menu screen
  * [ ] Setting daily Calorie goals
  * [ ] Setting Weekly Calorie Goals
  * [ ] Implement weightloss playlists
  * [ ] View Calorie Statistics
  * [ ] Include a pounds to calories value, 3500 calories ~= 1 lbs
* [ ] Somehow list calorie estimates for songs when selected. *Will be an option to toggle off in the menu*

## Important!
There is no way that this mod is accurate! However, I have been trying to set the amount of calories calculated to be lower than what I **imagine** they really are.

Please let me know if you find the calorie counting process to not be fair or too forgiving.

## Install
Make sure your game is patched with IPA, [Beat Saber Mod Installer](https://github.com/Umbranoxio/BeatSaberModInstaller/releases) will do this for you. Then,
1.  Download the [BeFit Mod latest release here](https://github.com/viscoci/BeFit/releases)
2.  Copy the fitNessMod.dll file to the Beat Saber Plugins folder
3.  That's it! Start the game and beat some calories to death! (I am aware that's not how that works)

![Menu Layout](https://visco.city/external/images/bfit.PNG)

## How it works
Currently it is really simple. Take a look at the source code and it won't take long to understand.

### How do the calories get calculated?
I played a less fun game that had a calorie calculator and I did an extreme session where I found the calories for a 12 minute period. I then used an element from the score controller and gave my best estimates to a multiplier that was accurate. *Completely Scientific Method Approved!*

### Feedback
Yes. There is much to be done, and to do it well I will need help. I'm a full time college student and currently work the rest my time. Please send me suggestions, concerns, etc. This has already been a fun way to keep track of my exercise and I would love to make it function well for everyone!
  

