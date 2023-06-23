# Analyzing the Careers of Top California Distance Runners: Exploratory Data Analysis for High School Running Continued Success Factors
## Does the Athlete Make the Coach or the Coach Make the Athlete?

## Capstone Project Final Code - Determining the Likelihood Top California High School Runners will run in College
-- Link to Final Capstone Project Jupyter Notebook:  https://github.com/tinalount/BerkeleyAIML/blob/main/CAPSTONE/TL%20Capstone%20Final.ipynb

## Which Top California Runners will Continue to Run in College?
California high schools have produced hundreds of amazing runners that have gone on to continue to run and compete in college. Are there any lessons learned or obvious trends in the data that can help predict success factors for star high school runners as they attempt to choose the "right" university and competitive level (D1,D2,D3, club) for them.

Deciding to compete in college at the NCAA Division 1 level takes a high level of success in high school and focus and determination in college. Not all high schoolers will go on to continued success. Is this a matter of their collegiate academic pressures? their changing interests and expanded horizons that college environment affords? Does the level of training or over-training in high school determine if they still have room for development in college?

**This project focused on exploring which top California high school runners would continue to run in college and whether there were certain predictive factors that could be determined from the data.**

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
* FUTURE: What are the strongest factors of success for high school running?
* FUTURE: Where do California High School Runners go to run in college?
** FUTURE: Can we predict whether a high school athlete will continue be successful at their chosen college level program?
** FUTURE: Is there a correlation or trend between where the athlete went to HS and College and whether that athlete will continue to develop/improve in their main (2) events?
* FUTURE: Do some high schools create superstar runners?
* FUTURE: Do some collegiate programs develop the runners better than others?
* FUTURE: Is there a difference in how athletes develop depending on whether they go to D1 versus D2, D3 collegiate programs?
* FUTURE: Are there any factors that make it more likely to have a full HS/Collegiate running career? Prediction for who might go pro?

**FINAL PROJECT QUESTION:** 
**Which runners continue into collegiate running?** 
The first preliminary question looked at for this exploratory project is to simply classify the available data to understand the factors predicting if an athlete will run in college or not.  Future analysis will include understanding which runners improved in college and what factors might have contributed to that. 

**DATA ANALYSIS:** 
* The Data Analysis for this project was focused just on 2016 data given how time-consuming and manual the compilation of the data file is.  This preliminary data analysis resulted in the following findings: 

* Breakdown by which runners continued in college:
124 (82.67%) of the top 150 California high school XC boy runners in 2016 went on to run in college varsity. 


<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/raw/main/CAPSTONE/Graphs/y_variable_plot.png">


* Breakdown by college division that the runners chose:  Of those that ran in college, 72.5% ran at D1 schools, 10.8% ran at D2 schools, 8.3% ran at D3 schools, 4.2% ran at Community Colleges, and 3.3% ran at NAIA division schools. 

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/blob/main/CAPSTONE/Graphs/percentage_of_runners_by_college_division.png">


* In-State versus Out-Of-State: of those that ran in college, 43 ventured out-of-state (35.8%) to run wile 77 (64.2%) stayed in-state.

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/blob/main/CAPSTONE/Graphs/collegiate_runners_by_state_percentage.png">  




**DATA MODELING:**
*Preliminary EDA Modeling done:* 

**DEPENDENT VARIABLES TO PREDICT:**
* The main target variable explored was the 'RUN_IN_COLLEGE_VARSITY?' variable: indicates whether the top California runner continued to run in college  and whether we could determine any key indicators for this outcome 
* A possible future dependent variable to explore is the 'FASTER_MILE' feature: likelihood the top California runner's mile time will improve in college 


**RESULTS:**
The Models explored included:

* **LOGISTIC REGRESSION MODEL**
Logistic Regression Results: The best Logistic Regression model results gave an accuracy of 58.8% accuracy

* **DECISTION TREE MODEL**
Decision Tree Results: Decision Tree Model produced an accuracy of 59.3% (with 10 features selected giving best results)¶ The output of the Decision Tree model was very interesting because it consistently showed the DIVISION the athlete ran in to be the most important decision factor for whether the athlete would continue to run in college.
The Decision Tree Model first splits the decision based on the DIVISION the athlete ran in at the State Championships and then their OVERALL TIME, and then the next important features are the High School Year and the SCHOOL THEY WENT TO

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/blob/main/CAPSTONE/Graphs/decision_tree.png"> 

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/blob/main/CAPSTONE/Graphs/decision_tree_scores.png"> 


* **RANDOM FOREST MODEL with GridSearch algorithm**
Random Forest Results: Random Forest initially gives a 59.3% accuracy - about the same 3,4, or 10 features are selected.
However, when the gridsearch was applied to find the best hyperparameters for the model, the accuracy increased to 84.4% using 10 estimators and a maximum decision tree depth of 3.

<img width="486" alt="image" src="https://github.com/tinalount/BerkeleyAIML/blob/main/CAPSTONE/Graphs/random_forest_scores2.png"> 


**CONCLUSIONS:DETERMINING WHICH TOP RUNNERS WILL COMPETE COLLEGIATELY** 
This project analyzed data from all the top cross country high school boy runners in the state of California for 2016 (top 30 across all 5 divisions) in order to understand the likelihood that these top runners would continue to run in college in the United States. Part of the motivation for this project was to understand what the main predictors for success in developing high school runners through to college and on to potentially professional levels.  Is it the coaches at particular high schools making the difference for the kids continuing in the sport or is it other factors such as socio-economic location factors or the size of the high school (division by divsion)? 

For the final Capstone Project, the data collected was increased to cover all 2016 top runners from California (this is a first step and continuing this project will involved collecting additional years of high school data).  Of the three Machine Learning algorithms deployed the Random Forest performed the best so those results are used for this conclusion. 


**CONCLUSIONS:**
The following are the key take-aways from Phase 1 of this analysis project:

* It appears that the majority of top California distance boy runners continue on to compete in college each year or about 3/4ths of the runners.
* The athlete's school size (division) and cross country/track program plays a very large role in whether the athlete will continue on into college.
* Other factors include the particular school the athlete is from and actually the religion of the athlete as many Christian schools offer running scholarships or programs. How fast the athlete runs in high school only matters up to a point.
* Several who ran incredibly fast in high school go on to run well in college while others don't.
* And several that ran pretty well in high school go on to run extremely well in college, surpassing those that beat them in high school.
* <span style="color:blue"> **All of these initial modeling results and findings lead me to believe that it is actually the PROGRAM that makes the ATHLETE as opposed to the ATHLETE that makes the PROGRAM. PROGRAM includes not just the coach but also the SIZE of the team, the LOCATION of the school, the ECONOMIC wealth of the program, the SUPPORT given the athlete (in terms of adult support/nutrition/team culture/etc), and the COMMITMENT to the team by the ATHLETE.** </span>
* If you want to run fast, go to the high school or university with a program that has the resources and dedicated culture to support athlete progression and development.


**NEXT STEPS:** 
* -- expand data beyond 2016 runners only - this is incredibly manual and time consuming to collate the data together 
* -- do further data analysis to compare time improvements from high school to college and to understand any data trends based on which high school, which division (school size) and which section (school location) to see if this affected the results in any significant way? 
*  -- do further data analysis to compare collegiate choices and to see if doing well in hs means getting recruited to "better" programs and thus basically sets your trajectory as a runner for college - ie. if you don't get recruited to a "top program" can you still be successful in  college? How much do people improve by by college?
*  -- do further analysis to understand if the section (geographic location) the runner comes from influences likelihood to run in college (i.e. socio-economic factors in play due to geographic region?) 
*  -- do further data analysis to understand if the high school XC 5k time or track mile time is a better predictor for success in collegiate running 
*  -- do further modeling using different techniques for final capstone project results
