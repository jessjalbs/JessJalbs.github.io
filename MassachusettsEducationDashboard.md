# Massachusetts Wants College Enrollment En Masse

<img src="images/MASSeduPic1.jpg?raw=true"/>
_photo belongs to [livingconcord.com]<https://www.livingconcord.com/listing/middlesex-school/> _

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
for our chart. I also changed the field that the bar chart was ordered to ascending order of graduating % since we wanted to see the schools based on the lowest 
graduating %, not alphabetically. 

<img src="images/Screenshot (59).png?raw=true"/>

As shown, I wanted to emphasize that data points for each school so I added labels. At the top I noticed that there was a school that had a 0% graduating, which I find 
to be improbable. I will look into why that may be later but for now I am going to exclude this school from our data because I believe it is an outlier or a mistake.

<img src="images/Screenshot (60).png?raw=true"/>

**and voila!** a bar chart that can help the board of education look into the graduating percentage of their high schools with emphasis on the worst performing schools in
the state. 

### Next we are going to take a look at college enrollment in relation to high school class size. 
I am going to use a scatterplot to look at the patterns for this particular question. I added average class size to columns and % attending college in rows. I changed the marks to circle to make it easier to see each individual point on our plot. 

<img src="images/Screenshot (61).png?raw=true"/>

Based on this plot, we can see that there is a pretty solid % attending college when class sizes are between 12 and 20 students. I don't think the state needs to build more schools in order to lower class size, since the smallest class sizes actually have low college attendance. 

I decided to add another attribute to our plot by adding some color. As a former teacher myself, I understand that students who are economically disadvantaged have a lower probability of attending college. Maybe the school board would have some interest in this information if they choose to build more schools. I added AVG % econimically disadvantaged to our plot as a color as a measure of our graph. 

<img src="images/Screenshot (62).png?raw=true"/>

It seems that econimically disadvantaged students are still most successful within the range we noticed earlier. While the percentage of economically disavantaged students attending college needs some improvement, I believe that there are other factors that can be changed to increase that percentage other than class size. 

### The superintendent believes that 4th grade mathematics is a key indicator of a student's future success and wants to improve the state's 4th grade math passing rate. 

He wants to know which districts have more than an average of more than 50% passing 4th grade math so that he can have teachers from those districts lead professional development workshops for the districts that are struggling. 

I started by adding district name to rows and %MCAS 4th Grade Math P (meaning passing) into columns. I want the average passing rate so I made that the measure. There are districts in Massachusetts that don't have elementary schools which has resulted in some nulls in our visualization so I filtered those out. I decided to add a reference line since we know our target is districts with a passing average higher than 50%. I thought that this data viz may be more insipiring as an area chart, here are the results thus far. 

<img src="images/Screenshot (64).png?raw=true"/>

I wanted it sorted in descending order by passing average so that we can see the highest performing schools at the top. I labaled the data points as well so it was easier to see the exact passing average percentage for each district. 

<img src="images/Screenshot (66).png?raw=true"/>

I grouped the districts that met the standards set by the superintendent and set the two seperate groups to "passing" and "needs work". I think it looks pretty good! It should be easy for state to find their professional development leaders. 

<img src="images/Screenshot (67).png?raw=true"/>

#### Dashboard Time!

I created 2 new sheets, one to count the number of schools, and one to count total student enrollemnt. That should cover our BANs. 

(<div class='tableauPlaceholder' id='viz1670870948110' style='position: relative'><noscript><a href='#'><img alt='Massachusetts Education Overview ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;DA&#47;DAA1-MASSSchools&#47;MassachusettsEducationOverview&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='DAA1-MASSSchools&#47;MassachusettsEducationOverview' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;DA&#47;DAA1-MASSSchools&#47;MassachusettsEducationOverview&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1670870948110');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1366px';vizElement.style.height='795px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='1366px';vizElement.style.height='795px';} else { vizElement.style.width='100%';vizElement.style.height='1377px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>)
