# Pewlett-Hackard-Analysis
## Purpose: The purpose of this analysis is to use the tables we have already created, and obtaining the number of retiring employees by title, and to identify emopoyees who are eligible to particulate in a mentorship program. 
### Deliverable 1 - Number of retiring employees by title: 
#### This step obtains retirement titles for employees born between Jan 1, 1952 and December 31, 1955. The table brought back all of the titles, so we also had to determine unique employees by their latest position. Finally, we establish a count by title of those individuals retiring. Select the folder below and select retirement_titles_distinct to get the final outcome of employees whom will be retiring soon. 


### Deliverable 2 - Employees eligible for the Mentorship Program: This step involved creating a mentorship-eligibility table. This involved obtaining employees from the employee table who were born during 1965. Select the link below and select the file called mentorship_eligibility to get the final list of employees eligible for mentorship. 


### Results
 a. The majority of retirees are Sr. Engineers and Senior Staff accounting for ~64% of all retiring. 
 b. There were 43,378 duplicate employees that were eliminated from the original file (employees who had multiple titles during their carreer at the company) once the distinct on command was used.  
 c. The mentorship eligibility file is far smaller than the sunami of employees schedule to retire within the next few years. 
 d. The majority of mentorship eligible employees come from the Sr. Staff as well as Engineers that are not Sr. Engineers, reflecting ~55% of eligible employees. 
 
 i. Retirement count from unique titles table
 Count    	title
29414	Senior Engineer
28254	Senior Staff
14222	Engineer
12243	Staff
4502	Technique Leader
1761	Assistant Engineer
2	Manager
90398	




ii. Count of mentorship eligible positions.   
count	title
436	Senior Staff
411	Engineer
288	Staff
276	Senior Engineer
77	Technique Leader
61	Assistant Engineer
1549 
 
 
 
 ### Summary
    1. How many roles will need to be filled as the "silver tsunami" begins to make an impact? There are 90,398 employees who have been identify to retire. 
    2. Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees? There are 1549 employees eligible        for mentorship. It would appear there are plenty of retirement ready employees available for mentorship to the next generation.  
       
Count    	title
29414	Senior Engineer
28254	Senior Staff
14222	Engineer
12243	Staff
4502	Technique Leader
1761	Assistant Engineer
2	Manager
90398	
   
-- Count number of mentorship eligible employees by position
SELECT COUNT(me.title), me.title
INTO me_count
FROM mentorship_eligibility as me
GROUP BY me.title
ORDER BY COUNT(me.title) DESC
ii. Count of mentorship eligible positions.   
count	title
436	Senior Staff
411	Engineer
288	Staff
276	Senior Engineer
77	Technique Leader
61	Assistant Engineer
1549 
