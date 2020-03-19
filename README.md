# Udacity data science nanodegree blogpost project #

This is an introductory data science project which tries to use the [Stack 
Overflow annual developer survey][1] to learn a bit about the field of software
development and the people in it.

## Requirements ##

This should be able to run on any system that has python installed through
Anaconda. It uses raw data from the developer surveys for 2017-19. The files 
are renamed with the convention `survey_results_YYYY.csv` and located in the
subfolder `data/` in this repository. Due to space constraints, I'm not 
including th data in the repo.

## Objectives ##

I was interested in digging more into job satisfaction among respondents, 
following some interesting observations from the course. In particular, I wanted
to know: 
 
1. Can respnses to the job satisfaction question be credibly compared across
multiple survey years? If so, this would allow us to look at multiple years to
see whether relationships are consistent.
2. Are there consistent differences in job satisfaction among respondents when
grouped by their educational level? 
3. How well can job satisfaction be predicted using only factors that can are 
common across the surveys for 2017-19?
4. Are the major predictors of job satisfaction consistent across years? Are the
effects of major predictors (sign and magnitude) consistent?

## File Descriptions ##

Data were downloaded from the [Stack Overflow annual developer survey][1]. 
Once the data are in place, it should be possible to run the analysis start to
finish with the file `dev_happiness.ipynb`.

## Results ##

Results are given more fully in an upcoming Medium post.

The job satisfaction question is asked in a different way each year. However, 
converting responses to a Likert scale (0-10 to match 2017) gives a reasonably
similar distribution. The average scores are also quite close, suggesting this
approach has some merit.

People with a doctoral degree are consistently more satisfied than other groups.
Beyond that, other groups do not seem to be consistently remarkable, although 
the professional degree holders go from being one of the most satisfied groups
in 2017 to one of the least in 2019.

The models I generated only explained a small portion of variation 
(R<sup>2</sup> values between 0.147 and 0.173), but given that these values hold
for the testing data as well, I'm confident that there are non-spurious 
relationships. It seems that the factors I looked at include "nudges" but not
outright drivers.

There were a few consistent predictors. Notably, not looking for a new job, 
having a doctoral degree, and being an independent contractor were all 
positives. Not listing a salary was impactful, but changed signs from 2017 to
other years. Seeing onesself as below-averge in skill was linked to lower 
satisfaction, as was feeling underpaid.    

## Licensing & Acknowledgements ## 

Data were downloaded from the [Stack Overflow annual developer survey][1] under
the the [Open Database License (ODbL)][2]. 

[1]: https://insights.stackoverflow.com/survey
[2]: http://opendatacommons.org/licenses/odbl/1.0/