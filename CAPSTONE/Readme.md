# Analyzing the Careers of Top California Distance Runners: Exploratory Data Analysis for High School Running Continued Success Factors
## Does the Athlete Make the Coach or the Coach Make the Athlete?

## Does Success in High School Running Predict Success in College?
California high schools have produced hundreds of amazing runners that have gone on to continue to run and compete in college. Are there any lessons learned or obvious trends in the data that can help predict success factors for star high school runners as they attempt to choose the "right" university and competitive level (D1,D2,D3, club) for them.

Deciding to compete in college at the NCAA Division 1 level takes a high level of success in high school and focus and determination in college. Not all high schoolers will go on to continued success. Is this a matter of their collegiate academic pressures? their changing interests and expanded horizons that college environment affords? Does the level of training or over-training in high school determine if they still have room for development in college?

**DATA SOURCES:** 
What take-aways will the data reveal? Some data sources to investigate: 
* https://www.xcstats.com/search-xc-california.php - various XC and track stats are kept here
* https://www.rtspt.com/events/cif/xc2022/mp/#event1 - CIF XC State Results from past 10 years
* https://www.strava.com/activities/8387865995/overview - Strava contains a wealth of runner information and does have a public API - I also am trying to meet with Strava's head AI Data Scientist
* https://athletic.net  - contains athlete profiles for both High School and Collegiate Records/times 
* https://www.milesplit.com/signings - several places provide data on who signed to go run at which college
* https://ca.milesplit.com/signings?year=2016&state=ca&sortBy=athlete&collegeSearch=&page=1 - 2016 signings summary

**Data Collection:** will have to be manual and pieced together from various sources - very time-consuming process
* **STEP ONE:** Collate a list of past top California XC runners (on the Woodward State Park 5K Course used every year) - obtained from: https://www.cifstate.org/sports/cross_country/past_results_records/index - gather the top 30 male runners by divisional race and their times for 2016 in preliminary analysis phase and then add 2014, 2015 years time-permitting
* **STEP TWO:** Runner by runner, determine if that runner ran in college using the following two main search sites as well as a generic google search per athlete: https://www.tfrrs.org/, https://ca.milesplit.com/signings?year=2016&state=ca&sortBy=athlete&collegeSearch=&page=1
* **STEP THREE:** Using profile summary sites fill out athlete's profile data if possible: HS Mile PR/1600m PR and College 5K, 3K, Mile PRS,  College In/Out of State? Location/State of College
* **FUTURE:** Obtain additional High School data - School Name, Coach, Division/Size, Graduation Year, Location, Private/Public
* **FUTURE** Obtain Athlete data - Name, DOB, Multi-Sport?, Years competing in HS?, Years Competing in MS?, Years Conmpeting in College?, Event Specialty, HS Events, College Events, GoPro? (Y/N), 
* **FUTURE** Obtain additional College data - School Name, Coach, Division/Size, Graduation Year, Gap Year?, Location

**Questions:**¶
* Which top California runners continue into collegiate running? Is this predictable based on their high school XC results at state?
* Which top California runners continue into Collegiate running and what factors influence this? Is it the high school program? the geographical location? the individual athlete's drive?
* What are the strongest factors of success for high school running?
* Where do California High School Runners go to run in college?
** Can we predict whether a high school athlete will continue be successful at their chosen college level program?
** Is there a correlation or trend between where the athlete went to HS and College and whether that athlete will continue to develop/improve in their main (2) events?
* Do some high schools create superstar runners?
* Do some collegiate programs develop the runners better than others?
* Is there a difference in how athletes develop depending on whether they go to D1 versus D2, D3 collegiate programs?
* Are there any factors that make it more likely to have a full HS/Collegiate running career? Prediction for who might go pro?

**FINAL PROJECT QUESTION:** 
**Which runners continue into collegiate running?** The first preliminary question looked at for this exploratory project is to simply classify the available data to understand the factors predicting if an athlete will run in college or not.  Future analysis will include understanding which runners improved in college and what factors might have contributed to that. 

**DATA ANALYSIS:** 
* The Data Analysis for this project was focused just on 2016 data given how time-consuming and manual the compilation of the data file is.  This preliminary data analysis resulted in the following findings: 

NOTE: need to get all 170 rows of data loaded first so this is incorrect summary: 

* Breakdown by which runners continued in college:
14 (9.3%) of top California high school XC runners went on to run in college varsity

<img width="459" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/78992740-35ff-4796-815f-cc02538a945a">


* Breakdown by college division that the runners chose:

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/69c4fee8-0b47-4a0f-a33c-9cf59cd4ce48">
                           
                           Number of runners Percentage of runners

* Breakdown by Out of State vs In State college choice: 

<img width="307" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/a0f9a2d4-7286-4a17-8807-d448e7b82f58">


**DATA MODELING:**
*Preliminary EDA Modeling done:* 

**DEPENDENT VARIABLES TO PREDICT:**
* The main target variable explored was the 'RUN_IN_COLLEGE_VARSITY?' variable: indicates whether the top California runner continued to run in college  

The Models explored included: 
* LOGISTIC REGRESSION MODEL gave 58% accuracy 
* DECISTION TREE MODEL gaver 75% accuracy - it seems like a very good dataset for using Decision Tree Analysis (based on where the athlete goes to school, which geographic location, and the size of the school) 
 <img width="566" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/cb7d8b31-5829-4520-b9ec-dfa7833a41ac">

* RANDOM FOREST MODEL - a Random Forest Model was added for the final project analysis and gave the best results so far of 82% accuracy


* A possible future dependent variable to explore is the 'FASTER_MILE' feature: likelihood the top California runner's mile time will improve in college - i.e. what percentage got faster in the mile in college - i.e. 9% got faster from the 20 runners analyzed so far: 

<img width="515" alt="image" src="https://github.com/tinalount/BerkeleyAIML/assets/5034662/3b814c5c-cb42-4f35-8816-b7580d064536">


**CONCLUSIONS:DETERMINING WHICH TOP RUNNERS WILL COMPETE COLLEGIATELY** 

This project analyzed data from all the top cross country high school boy runners in the state of California for 2016 (top 30 across all 5 divisions) in order to understand the likelihood that these top runners would continue to run in college in the United States. Part of the motivation for this project was to understand what the main predictors for success in developing high school runners through to college and on to potentially professional levels.  Is it the coaches at particular high schools making the difference for the kids continuing in the sport or is it other factors such as socio-economic location factors or the size of the high school (division by divsion)? 

For the final Capstone Project, the data collected was increased to cover all 2016 top runners from California (this is a first step and continuing this project will involved collecting additional years of high school data). 

Of the three Machine Learning algorithms deployed the Random Forest performed the best so those results are used for this conclusion. 

<CONCLUSION HERE> 


  
  
  
**EARLIER FINDINGS: PHASE 1 for EARLY DATA EXPLORATION (EDA)**
With very little data (20 rows) two classification models were applied with different hyperparameter settings against the top California running data from 2016 to predict if the athlete will run in college with 50% accuracy using Logistic Regression and 75% accuracy using Decision Tree classification to determine if the athlete would run in college or not. It is too early to rely on these results because the data is not complete - however, early analysis does give the indication that Decision Tree modeling would be a good approach for this analysis project. It also indicates that perhaps there are not that many factors beyond a few that influence if the runner continues running into college.  Note that the data being used is already selecting the top runners in California by nature of them being in the top 30 at State so it's agreed they are all good runners - so what other factors contribute to continuing into college? 

**NEXT STEPS:** 
* -- expand data beyond 2016 runners only - this is incredibly manual and time consuming to collate the data together 
* -- do further data analysis to compare time improvements from high school to college and to understand any data trends based on which high school, which division (school size) and which section (school location) to see if this affected the results in any significant way? 
*  -- do further data analysis to compare collegiate choices and to see if doing well in hs means getting recruited to "better" programs and thus basically sets your trajectory as a runner for college - ie. if you don't get recruited to a "top program" can you still be successful in  college? How much do people improve by by college?
*  -- do further analysis to understand if the section (geographic location) the runner comes from influences likelihood to run in college (i.e. socio-economic factors in play due to geographic region?) 
*  -- do further data analysis to understand if the high school XC 5k time or track mile time is a better predictor for success in collegiate running 
*  -- do further modeling using different techniques for final capstone project results
