# SBM23
All new code for a classic pinball machine. With an Arduino connected to the MPU, this code will run on a Silverball Mania pinball machine (1980).  
  
## How to build this for your machine  
1) build or buy a board to interface an Arduino MEGA 2560 PRO with the MPU processor socket or J5 connector  
2) get this code, put it in a SBM23 folder  
3) update configuration in RPU_config.h to match your board type  
4) compile/install code on the Arduino MEGA 2560 PRO
  
## More Information  
http://pinballrefresh.com  
  
## Test / Audit / Settings from coin-door switch  
Tests (test number shown in Credits, Ball in Play is blank)  
1 - Lamps  
2 - Displays  
3 - Solenoids  
4 - Switches  
5 - Sounds (not applicable)  
  
Settings & Audits (page number shown in Ball in Play, Credits is blank)  
1 - Award Score 1  
2 - Award Score 2  
3 - Award Score 3  
4 - High Score  
5 - Credits  
6 - Total Plays  
7 - Total Replays  
8 - High Score Beat  
9 - Chute 2 Coins  
10 - Chute 1 Coins  
11 - Chute 3 Coins  
12 - Reboot (All displays show 8007 (as in "BOOT"), and Credit/Reset button restarts)  
13 - Coins per Credit for Chute 1  
14 - Coins per Credit for Chute 2  
15 - Coins per Credit for Chute 3  
16 - Free Play  
17 - Ball Save  
18 - Sound Selector  
    0 = no sounds  
    1 = sound effects through -51  
    2 = sound effects & background drone through -51  
    3 = sound effects through WAV Trigger  
    4 = sound effects & background song through WAV Trigger  
19 - Music Volume  
20 - Tournament Scoring  
21 - Tilt Warnings  
22 - Award Scores (0 = all extra balls, 7 = all specals)  
23 - Number of Balls Per Game  
24 - Scrolling Scores  
25 - Extra Ball Award (for tournament scoring)  
26 - Special Award (for tournament scoring)  
27 - Dim level  
  
## Example Sound Files  
https://drive.google.com/file/d/1xsmqtWZP9hqvHiajO6iWM1bCcZa6pH1e/view?usp=sharing  


## Game Play
### Skill Shot
At the start of each ball, there are four skill shots available:  
1) Left & Right Top Lanes - hitting either the left or right top lane when the lamp is lit will spot the player one “Silverball Mania“ letter. The 50 pt switches change which lane is lit.  
2) Middle Top Lane - hitting the middle top lane when the lamp is lit will spot the player one “Silverball Mania” letter, award the player 5,000 points, and activate the ball kicker for 15 seconds.  
3) Horseshoe Rollover - hitting the center horseshoe rollover will award the player 20,000 points, turn on the ball kicker for 2 seconds, and qualify the super skill shot.
Super skill shot - if the Horseshoe Rollover skill shot is hit, the player can then hit the Center Target (“N” target) for an additional 15,000 points as a super skill shot.  
Any switch hit aside from those listed above (and the right spinner) will exit the Skill Shot mode and drop the player into normal play.
  
### Normal Play  
During the course of normal play there are three main objectives to Silverball Mania.  
1) Collecting the “Silverball Mania” lamps.  
2) Advancing the Bonus Multiplier  
3) Collecting the Combo Awards for 15,000, 30,000, and 60,000 points

#### Collecting “Silverball Mania” Lamps  
At the start of the first ball, after the Skill Shot mode is exited, all the Silverball Mania targets on the playfield will be lit. Hitting a target will turn off the lamp at the target and light the corresponding lamp in the middle of the playfield. Those letters collected will be rewarded 1,000 bonus points at the end of the ball (multiplied by the bonus multiplier).  
To collect the lamps a second time, the player has to collect them in groups. At first, “Silver” will be lit. Once those letters are collected, “Ball” will light. Finally, the player will need to collect the “Mania” lamps.  
The third and subsequent times the player collects the lamps, they will need to be collected in order. If a player hits a letter out of order (for example, the L before the S), the letters before that letter will have to be collected within 20 seconds or the out-of-order letter will be forfeited.  
For the first and second set of letters, collecting the M or the A on the out lanes will turn on the ball kicker for 5 seconds. For the first five sets of letters, the 50 point switches will rotate the MANIA letters so they can be collected without losing the ball.  
#### Advancing the Bonus Multiplier  
The bonus multiplier can be advanced by completing the top lanes, or completing a combo shot of the horseshoe and N center target.  
If the left or right top lanes are completed, the lamps associated with those lanes will indicate which lane is completed (they use the same lamp circuit, so they can’t be controlled individually). If the left lane is hit, the lane lamps will blink once slowly. If the right lane is hit, the lamps will blink twice and then pause. If the left and right lamps are steady, those lanes are complete. The center lane lamp will show solid when that lane has been completed. Completing all three lamps advances to 2x, 3x, 4x, and 5x bonus multiplier.  
Another method of increasing the bonus multiplier is to complete a combo of the horseshoe and then the center N target. As the bonus multiplier gets higher, the combo will have to be done in a shorter time period.  
#### Collecting Combo Awards  
When the ball travels through either in lane, the opposite spinner will flash to start a combo. After that spinner is hit, the other spinner will light for 10 seconds to advance the combo. When the alternating spinners have been satisfied, the lights will sweep in a circle to guide the player to hit the horseshoe to continue the combo. After the horseshoe is completed, the player has 20 seconds to finish the combo by allowing the ball to drop into the ball kicker.  
The first combo award is worth 15,000, then 30,000 and 60,000. The award is given at the time the ball kicker is hit, as well as a bonus at the end of the ball.  
#### Random Letter Combo  
During play, the SILVERBALL lamps on the head of the machine will cycle rapidly. When the horseshoe is hit, the cycle will stop, lighting a combo on one of the SILVERBALL stand up targets. The target will be lit (flashing) for 15 seconds. If this target is the first SILVERBALL MANIA target/rollover hit during the 15 seconds, the player will be awarded 15,000 points and advance the Bonus Multiplier.  

  
