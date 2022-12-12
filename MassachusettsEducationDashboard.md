# Massachusetts Wants College Enrollment En Masse

<img src="images/MASSeduPic1.jpg?raw=true"/>
_photo belongs to [livingconcord.com]<https://www.livingconcord.com/listing/middlesex-school/>_

## "We don't need no education," said no one on the the state of Massachusetts school board.

**Project description:** I have been tasked with looking into some aspects of the school system in Massachusetts to help the education department better understand
their strengths and weaknesses. I have been given a spreadsheet with data from every school in the state and I am using Tableau to create a dashboard for the department.

### Let's get our data uploaded into Tableau
<img src="images/Screenshot (58).png?raw=true"/>

I uploaded out spreadsheet into Tableau public and got familiar with the rows and columns. There are A LOT of columns in this dataset. Thankfully we are not going to 
utilize many of them. I will be focusing my attention on some specific information such as KPIs, or my prefered term, BANs (big a** numbers) based on the parameters set
by the school board. 

### Our first order of business is to determine the 10 schools that are performing the worst based on graduating percentage.
I created a horizontal bar chart with the school names for rows and the graduating % of each school for columns. Since there are schools within our data that are not 
high schools, we had some null values within our bar chart. I removed them by adding a filter for the graduating % by attirbute and keeping only non-null values
for our chart. I also changed the field that the bar chart was ordered to descending order of graduating % since we wanted to see the schools based on the lowest 
graduating %, not alphabetically. 

<img src="images/Screenshot (59).png?raw=true"/>

As shown, I wanted to emphasize that data points for each school so I added labels. At the top I noticed that there was a school that had a 0% graduating, which I find 
to be improbable. I will look into why that may be later but for now I am going to exclude this school from our data because I believe it is an outlier or a mistake.

<img src="images/Screenshot (60).png?raw=true"/>

**and voila!** a bar chart that can help the board of education look into the graduating percentage of their high schools with emphasis on the worst performing schools in
the state. 

### Next we are going to take a look at college enrollment in relation to high school class size. 



