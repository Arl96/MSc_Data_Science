# 20MAP501_CW Assignment


You will submit your coursework in the form of a single R notebook (i.e..Rmd file) which can be rendered (“knitted”) to an .pdf document, as well as the knitted version. Specifically, submit to the relevant submission section on learn:
• your R notebook (i.e. the .Rmd file),
• the rendered .pdf version of your notebook (in case there are any problems knitting your .Rmd during marking).
The coursework will be marked on the basis of correctness of code, interpretation of outputs and commentary
as indicated.
1. Preamble
In this section, you will prepare your workspace for undertaking the analyses in this coursework.
a. Load in any packages you will use to undertake this coursework, including AmesHousing. Use
make_ames() command to create a clean version of the Ames Housing dataset called Ames. (5 points)
b. Import the england-premier-league-players-2018-to-2019-stats.csv dataset as “playerstats”, ensuring
that all variables are treated correctly. Where variable names have a space, rename the variables
without these. Remove the cases with age<10 Create a new variable, “played”, in playerstats that
indicates if a player played greater than 0 minutes or not. Create a new dataset called “football”
consisting of only those players that played greater than 0 minutes. Create a new dataset called
“footballngk” consisting of those players in “football” who are not goalkeepers. Drop the unused level
of “position”. (5 points)
2. Linear Regression
In this problem, you are going to investigate the response variable Lot_Area from the dataset Ames through
linear regression.
a. By adjusting x axis range and number of bars, create a useful histogram of Lot_Area on the full
dataset. Ensure that plot titles and axis labels are clear. Comment on why deleting properties with
Lot_Area> 30000 makes sense. Create a new dataset Ames2 consisting only of those properties with
lot area <30000. (5 points)
b. Now remove all cases corresponding to MS_Zoning categories of A_agr (agricultural), C_all (commercial) and I_all (industrial) from the Ames2 dataset. Drop the unused levels from the MS_Zoning
variable. (2 points)
c. Choose an appropriate plot to investigate the relationship between MS_Zoning and Lot_Area in
Ames2. (2 points)
1
d. Choose an appropriate plot to investigate the relationship between Gr_Liv_Area and Lot_Area in
Ames2. Color points according to the factor MS_Zoning. Ensure your plot has a clear title, axis labels
and legend. (4 points)
e. Choose an appropriate plot to investigate the relationship between Garage_Cars and Lot_Area in
Ames2. Use the “jitter” command to make your plot more clear. (3 points)
f. Why do we make these plots? Comment on your findings from these plots (1 sentence is fine). (2
points)
g. Use the lm command to build a linear model, linmod1, of Lot_Area as a function of the predictors
MS_Zoning and Gr_Liv_Area for the Ames2 dataset. Evaluate the assumptions of the model. (5
points)
h. Use the lm command to build a second linear model, linmod2, for Lot_Area as a function of
MS_Zoning, Gr_Liv_Area and Garage_Cars. (2 points)
i. Use Anova and Adjusted R-squared to compare these two models, and decide which is a better model.
(3 points)
j. Construct a confidence interval and a prediction interval for the lot area of a residential property in
the High Density zone, with a 2 car garage and a living area of 1000 sq ft. Explain what these two
intervals mean. (4 points)
k. Now use the lmer function to build a third model, mmod1, for Lot_Area as a function of zoning, living
area, garage size and neighborhood. What is the critical number to pull out from this, and what does
it tell us? (3 points)
l. Construct 95% confidence intervals around each parameter estimate for mmod1. What does this tell
us about the importance of the random effect? (2 points)
m. Write out the full mathematical expression for the model in linmod2 and for the model in mmod1.
You may round to the nearest integer in all coefficients. (4 points)
3. Logistic Regression
a. Construct a logistic regression model glmod1 for “played” as a function of player age and position. (2
points)
b. Construct confidence bands for the variable played as a function of age for each position (hint: create
a new data frame for each position). Colour these with different tranparent colours for each position
and plot them together on the same axes. Put the actual data on the plot, coloured to match the
bands, and jittered in position to make it possible to see all points. Ensure you have an informative
main plot title, axes labels and a legend. (6 points)
c. Split the data using set.seed(123) and rebuild the model on 70% of the data. Cross validate on the
remaining 30%. Plot the ROCs for both data and comment on your findings. (6 points)
4. Multinomial Regression
a. For the dataset footballngk, create a model multregmod to predict position from goals_per_90_overall,
assists_per_90_overall, conceded_per_90_overall and cards_per_90_overall. (2 points)
b. Write out the formulas for this model in terms of P(Forward) and P(Midfielder). You may round
coefficients to 2 digits. All other factors equal, what position is a player with more assists more likely
to play? (5 points)
2
c. Evaluate the performance of this model using a confusion matrix and by calculating the sum of sensitivities for the model. Comment on your findings. (3 points)
5. Poisson/quasipoisson Regression
a. For the football dataset, first create a variable indicating the total number of all cards a player received
overall. Then create a model countmod to predict the total number of cards a player received based
on position and appearances. (3 points)
b. Check the assumption of the model using a diagnostic plot and comment on your findings. (2 points)
c. What do the coefficients of the model tell us about which position gets the most cards? For the same
minutes of play, how many times more cards do they get than the position that gets the least cards?
(3 points)
