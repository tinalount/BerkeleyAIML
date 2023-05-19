# Does the Athlete Make the Coach or the Coach Make the Athlete?
OR
# Does Success in High School Running Predict Success in College?

California high schools have produced hundreds of amazing runners that have gone on to continue to run and compete in college.  Are there any lessons learned or obvious trends in the data that can help predict success factors for star high school runners as they attempt to choose the "right" university for them
* What are the strongest factors of succes
s for high school running?
* Where do California High School Runners go to run in college?
* Can we predict whether a high school athlete will continue be successful at their chosen college level program?

Deciding to compete in college at the NCAA Division 1 level takes a high level of success in high school and focus and determination in college.  Not all high schoolers will go on to continued success.  Is this a matter of their collegiate academic pressures? their changing interests and expanded horizons that college environment affords? Does the level of training or over-training in high school determine if they still have room for development in college?  

**DATA SOURCES:** 
What take-aways will the data reveal? Some data sources to investigate: 
** https://www.xcstats.com/search-xc-california.php - various XC and track stats are kept here
** https://www.rtspt.com/events/cif/xc2022/mp/#event1 - CIF XC State Results from past 10 years
** https://www.strava.com/activities/8387865995/overview - Strava contains a wealth of runner information and does have a public API - I also am trying to meet with Strava's head AI Data Scientist
** https://athletic.net  - contains athlete profiles for both High School and Collegiate Records/times 
** https://www.milesplit.com/signings - several places provide data on who signed to go run at which college
** https://ca.milesplit.com/signings?year=2016&state=ca&sortBy=athlete&collegeSearch=&page=1 - 2016 signings summary

**Data Collection:** will have to be manual and pieced together from various sources - very time-consuming process
** **STEP ONE:** Collate a list of past top California XC runners (on the Woodward State Park 5K Course used every year) - obtained from: https://www.cifstate.org/sports/cross_country/past_results_records/index - gather the top 30 male runners by divisional race and their times for 2016 in preliminary analysis phase and then add 2014, 2015 years time-permitting
** **STEP TWO:** Runner by runner, determine if that runner ran in college using the following two main search sites as well as a generic google search per athlete: https://www.tfrrs.org/, https://ca.milesplit.com/signings?year=2016&state=ca&sortBy=athlete&collegeSearch=&page=1
** **STEP THREE:** Using profile summary sites fill out athlete's profile data if possible: HS Mile PR/1600m PR and College 5K, 3K, Mile PRS,  College In/Out of State? Location/State of College
** **FUTURE:** Obtain additional High School data - School Name, Coach, Division/Size, Graduation Year, Location, Private/Public
** **FUTURE** Obtain Athlete data - Name, DOB, Multi-Sport?, Years competing in HS?, Years Competing in MS?, Years Conmpeting in College?, Event Specialty, HS Events, College Events, GoPro? (Y/N), 
** **FUTURE** Obtain additional College data - School Name, Coach, Division/Size, Graduation Year, Gap Year?, Location

**Questions:**¶
** Which top California runners continue into collegiate running? Is this predictable based on their high school XC results at state?
** Which top California runners continue into Collegiate running and what factors influence this? Is it the high school program? the geographical location? the individual athlete's drive?
** What are the strongest factors of success for high school running?
** Where do California High School Runners go to run in college?
** Can we predict whether a high school athlete will continue be successful at their chosen college level program?
** Is there a correlation or trend between where the athlete went to HS and College and whether that athlete will continue to develop/improve in their main (2) events?
** Do some high schools create superstar runners?
** Do some collegiate programs develop the runners better than others?
** Is there a difference in how athletes develop depending on whether they go to D1 versus D2, D3 collegiate programs?
** Are there any factors that make it more likely to have a full HS/Collegiate running career? Prediction for who might go pro?

**EDA QUESTION:** 
**Which runners continue into collegiate running?** The first preliminary question looked at for the EDA(exploratory data analysis) phase is to simply classify the available data to understand the factors predicting if an athlete will run in college or not

**DATA ANALYSIS:** 
*Round1:* Preliminary EDA Data Analysis was focused just on 2016 data given how time-consuming and manual the compilation of the data file is.  This preliminary data analysis resulted in the following findings: 
NOTE: need to get all 170 rows of data loaded first so this is incorrect summary: 

* Breakdown by which runners continued in college:
14 (9.3%) of top California high school XC runners went on to run in college varsity

<img width="459" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/78992740-35ff-4796-815f-cc02538a945a">


* Breakdown by college division that the runners chose:

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/69c4fee8-0b47-4a0f-a33c-9cf59cd4ce48">
                           
                           Number of runners Percentage of runners

* Breakdown by Out of State vs In State college choice: 
* 
<img width="307" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/a0f9a2d4-7286-4a17-8807-d448e7b82f58">


**DATA MODELING:**
*Preliminary EDA Modeling done:* 
DEPENDENT VARIABLES TO PREDICT:
* 'RUN_IN_COLLEGE_VARSITY?': likelihood the top California runner will continue to run in college - so far the LOGISTIC REGRESSION MODEL gave 58% accuracy while the DECISTION TREE MODEL gaver 75% accuracy - it seems like a very good dataset for using Decision Tree Analysis (based on where the athlete goes to school, which geographic location, and the size of the school) 
<img width="285" alt="image" src="https://github.com/tinalount/BerkeleyAIM
L/assets/5034662/a807254a-73b6-461e-8292-68cdf0e77e62">

* 'FASTER_MILE': likelihood the top California runner's mile time will improve in college - i.e. what percentage got faster in the mile in college - TO DO
* 'FASTER_5K': likelihood the top California runner's 5K will improve in college  - TO DO


**CONCLUSIONS:**
*Preliminary EDA Data Analysis and Modeling of 2016 data only to start with resulted in the following conclusions:* 
MODEL CONCLUSIONS/LEARNINGS
PHASE 1 for EARLY DATA EXPLORATION (EDA)
With very little data (20 rows) a Linear Regression model can be applied against the top California running data from 2016 to predict if the athlete will run in college with only 25% accuracy - but this will increase with more data I'm pretty sure..... just phase 1 of understanding and sourcing the data


**NEXT STEPS:** 
* -- expand data beyond 2016 runners only - this is incredibly manual and time consuming to collate the data together 
* -- do further data analysis to compare time improvements from high school to college and to understand any data trends based on which high school, which division (school size) and which section (school location) to see if this affected the results in any significant way? 
*  -- do further data analysis to compare collegiate choices and to see if doing well in hs means getting recruited to "better" programs and thus basically sets your trajectory as a runner for college - ie. if you don't get recruited to a "top program" can you still be successful in  college? How much do people improve by by college?
*  -- do further analysis to understand if the section (geographic location) the runner comes from influences likelihood to run in college (i.e. socio-economic factors in play due to geographic region?) 
*  -- do further data analysis to understand if the high school XC 5k time or track mile time is a better predictor for success in collegiate running 
*  -- do further modeling using different techniques for final capstone project results
