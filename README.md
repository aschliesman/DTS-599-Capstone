# Introduction

This project seeks to determine which regular-season factors can predict team success for 
Division I Men’s basketball teams—specifically related to NCAA March Madness tournament outcomes.

# Data and Variables 

The original dataset can be found on Kaggle.com, and it contains 23 statistics on over 300 Division I Men’s basketball teams. It 
contains data for the years 2013-2023, and it is updated each year after the tournament. The following variables are included in the dataset:

G: Number of games played\
W: Number of games won\
ADJOE: Adjusted Offensive Efficiency\
ADJDE: Adjusted Defensive Efficiency\
BARTHAG: Power Rating\
EFG_O: Effective Field Goal Percentage Shot\
EFG_D: Effective Field Goal Percentage Allowed\
TOR: Turnover Percentage Allowed\
TORD: Turnover Percentage Committed\
ORB: Offensive Rebound Rate\
DRB: Offensive Rebound Rate Allowed\
FTR : Free Throw Rate\
FTRD: Free Throw Rate Allowed\
2P_O: Two-Point Shooting Percentage\
2P_D: Two-Point Shooting Percentage Allowed\
3P_O: Three-Point Shooting Percentage\
3P_D: Three-Point Shooting Percentage Allowed\
ADJ_T: Adjusted Tempo (An estimate of the tempo (possessions per 40 minutes) a team would have against the team that wants to play at an average Division I tempo)\
WAB: Wins Above Bubble\
POSTSEASON: Round where the given team was eliminated or where their season ended\
SEED: Seed in the NCAA March Madness Tournament\
YEAR: Season

# Objectives 

The goals and objectives for the project include:
- Determine the effect of regular season statistics on postseason outcomes
- Determine patterns of upsets in March Madness. Is it truly random, or is there a pattern to underdogs winning?
- Compare regular season outcomes with postseason outcomes. Do they have the same trends?
- Develop a model to predict team outcomes for new seasons, regular and postseason
- Compare tournament outcomes across different seasons

# Description 
This code looks to test data over the course of previous years of march madness to determine how well each team will do in the post season. There are 5 different equations that were tested, with the basic variables and the important variables performing the best. All of these equations will be posted to see what coparison is needed to be made.

# Formulas 
Predicted Seed=2.45530+0.67538xADJDE-0.67537*ADJOE+12.36019xBARTHAG+0.19725xEFG_O+FTRDx0.05740-ADJ_Tx0.08455\

Predicted March Madness Success1=76.3730+1.4671xADJDE-1.5632xADJOE\
(Related to only ADJOE and ADJDE)\

Predicted March Madness Success2=-10.4514+1.1880xSEED-1.8632xW+3.7798xADJDE-2.3714xADJOE+68.8196xBARTHAG+1.2750xTORD-1.3082xDRB+0.3124xFTR-1.4533xTWOP_D+2.248xWAB(Related to Important Variables)\

Predicted March Madness Success3=55.3479+0.3623xSEED-1.5262xW+WABx0.3918(Related to Basic Variables)\

Predicted March Madness Success4=205.0355-2.495xADJOE+1.8113xEFG_O-1.3013xTOR+ORBx0.1067+FTRx0.3631+0.5797xTHREEP_O-0.8719xTWOP_O+0.7859xADJ_T(Related to Offense)\

Predicted March Madness Success5=-138.3163+3.0282xADJDE+5.0483xEFG_D+1.54xTORD-DRBx1.4060+FTRDx0.3314-3.7031xTHREEP_D-4.884xTWOP_D(Related to Defense)\

Predicted Wins1=5.21235-0.38954xADJDE+0.49404xADJOE(Related to only ADJOE and ADJDE)\

Predicted Wins2=15.73771+0.59479xTHREEP_O-0.67821xTHREEP_D+0.71905xTWOP_O-0.69906xTWOP_D+0.13843xFTR-0.06921xFTRD(Related to Basic Variables)\

Predicted Wins3=-40.12261+0.199xADJOE+0.50192xEFG_O-0.74015xTOR+ORBx0.48263+0.12185xFTR+0.04667xTHREEP_O+0.33595xTWOP_O-ADJ_Tx0.17809(Related to Offense)\

Predicted Wins4=88.63371-ADJDEx0.24796-EFG_Dx1.17020+TORDx0.51659-DRBx0.37067-FTRDx0.0211+0.22497xTHREEP_D+TWOP_Dx0.26545 (Related to Defense)\

Predicted Wins5=1.373930+ADJDEx0.09432+BARTHAGx4.012412+EFG_Ox0.811507-EFG_Dx0.847656-TORx0.779007+TORDx0.786747+ORBx0.335041-DRBx0.292518+FTRx0.124129-FTRDx0.126843+ADJ_Tx0.055060(Related to Important Variables)\

# Results

ADJDE and ADJOE only:about 69% accurate

Significant Variables:about 72% accurate

Basic Variables:about 72% accurate

Offense Only:about 65% accurate

Defense Only:about 59% accurate

Predicting wins varied heavily, though the most consistent and accurate was equatioin 2 regarding basic variables being 68-70% accurate over 10 years.

Brackets(both predicted and actual results) will be provided.



