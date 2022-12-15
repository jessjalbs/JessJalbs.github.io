## A Hospital Holiday Investigation: How Can Hospitals Save Money and Keep Beds Open! 

### Okay, okay, maybe not an _actual_ holiday investigation, but it is the holiday season, no? Merry Everything, Y'all!

**Project description:** I have _hypothetically_ been hired by a hospital's data analytics team to evaluate how the hospital can save money by keeping their beds open.
I have been given a dataset that includes 2 tables, one with patients' demographics, and one with their health information. This dataset comes from [Kaggle](https://www.kaggle.com/code/iabhishekofficial/prediction-on-hospital-readmission/data?select=diabetic_data.csv).
I have uploaded my data into my MySQL Workbench and I am ready to get started! 

### To begin, I want to see what the time being spent in the hospital looks like. 

I figured that it would be easiest to get a gauge on the distribution of time spent in the hospital by creating a histogram. While I am aware that MySQL is not a data viz
tool, I think it would help my "boss" see how long the majority of our patients are staying. You can see the query that I used here:

<img src="images/Histogram.png?raw=true"/>

Based on our histogram, we can see that the majority of our patients are staying less than 7 days. That is interesting information! But let's dive deeper. 

### Procedures are the biggest cost to our hospital. What specialty is doing the most procedures on average?

We have a number of different secialists at our hospitals performing procedures. I wrote a query to see the average amount of procedures per specialty and put them in 
descending order based on the average. 

<img src="images/HAVING.png?raw=true"/>

I chose to focus on specialties that have at least 50 patients, (specialties with low procedures are not costing us much money), as well as limiting our concerns to 
specialties that have more than 2.5 procedures on average. i can give these results to my "boss" so she can share this information with our stake holders. 

### Are nurses treating patients of different races differently? 

Our hospital has a zero-tolerance policy for racism, and while it may not affect our bottom line, I want to make sure that everyone is being treated fairly by our staff. 
I wrote a query cross-referencing our patients race with the number of lab procedures to make sure that **every** patient is being treated with the utmost care. 

<img src="images/JOIN.png?raw=true"/>

Thankfully, it lookes like our results are pretty consistent across all of our patients. As it should be! 

### Next, Let's see if there is a correlation between the number of procedures a patient has and the amount of time that is spent in the hospital. 

This seems like a pretty obvious assumption, but I want to be sure about these stats. In order to write the full query for this correlation, I wanted to get a little
more familiar with the num_procedures column. 

<img src="images/CASE WHEN 1.png?raw=true"/>

Our average procedure per patient is 1.3, with patients maxing out at 6 procedures. Not surprisingly, the minimum amoutn of procedures is 0. Using this information I am
going to group our patients based on the amount of procedures that they have had. 

<img src="images/CASE WHEN 2.png?raw=true"/>

Now that all of our patients have been assigned to a group, I can use this information to write a query that will give us the average amount of time spent at the hospital
for each procedure group. 

<img src="images/CASE WHEN FINAL.png?raw=true"/>

And here are our results! My "boss" will be very interested to know this information. I wonder why patients with no procedures are staying for over 3 days on average?

### I got an email from a coworker in research and they need my help for some information!

My coworker says that the research team wants to run some tests with any patient that is African American or who has an "Up" for metformin, (whatever that means 🤷🏼‍♀️),
so they have asked me for anyone who falls under this criteria's patient_nbr.
I have the time and am a great team player so I quickly write a query so I can send her this information, STAT!

<img src="images/UNION.png?raw=true"/>

### Let's highlight some success stories for the hospital! 

The hospital administrator wants to put some emphasis on cases where patients came in with an emergency, (admission_type_id of 1), but stayed less than the average
amount of time at the hospital. 

<img src="images/SUBQUERY CTE.png?raw=true"/>

This is a great opportunity to study any patterns in the consistency in these cases as well as celebrating the staff that helped ensure these success stories. 

### The big "boss" wants a summary of the top 50 patients who take the most medication.

THe summary of the information is pretty extensive and both tables will be used. In order to complete to ful summary I need some more information. My first query was to find out what the different text strings were under the readmitted column. 

<img src="images/CONCAT 1.png?raw=true"/>

Now that I know the different text strings, I can write out my full query for my summaries. I will need to use the CONCAT funtion in order to include all of the 
requested information. This one was a good time 😉

<img src="images/CONCAT 2.png?raw=true"/>

Hopefully the hospital will be able to utilize this information to better understand how they can keep beds open and save some money.

### Thank you for joining me for my hospital project using MySql! As I am writing this it is December 15th, 2022, and I can only hope that anyone who is sick in the hospital can get home and spend time with their families this holiday season. Sending positive, healing thoughts to anyone out there who is going through a hard time ❤ 

## All in a days work! I wonder what I will be able to assist with tomorrow 👩🏼‍💻 




