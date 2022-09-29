# Pewlett-Hackard-Analysis
## Overview of the analysis
### The analysis is to help Pewlett Hackard prepare for the upcoming “silver tsunami”.  
## Results
### We created a Retirement Titles table to hold all the titles of employees who were born between January 1, 1952 and December 31, 1955. This was done by joining the existing Employees and Titles tables. See table head below:
<img width="498" alt="image" src="https://user-images.githubusercontent.com/110864175/192914204-7c0cc90f-be01-44f3-8c2f-cca8d4474b5a.png">

### We created a Unique Titles table from the Retirement Titles table. This table was created because there are duplicate entries for some employees in the Retirement Titles table because they switched titles over the years, we used the DISTINCT ON clause to remove the duplicates and keep only the most recent title of each employee. We also excluded employees who have already left the company by filtering on to_date. See table head below:
<img width="369" alt="image" src="https://user-images.githubusercontent.com/110864175/192914321-37f86f83-c463-45bc-b3ef-1e5303e26e96.png">

### We created Retiring Titles table from the Unique Titles table. This table was created to hold the number of employees by their most recent job title who are about to retire. See table head below:
<img width="192" alt="image" src="https://user-images.githubusercontent.com/110864175/192914396-8a8788c9-ffd3-45a4-bbca-eaabc08839a4.png">

### We created a Mentorship Eligibility table by joining the Employees table, Department Employee table, and Titles table. This table was created to hold the employees who are eligible to participate in a mentorship program. See table head below:
<img width="551" alt="image" src="https://user-images.githubusercontent.com/110864175/192914467-e3e96bdf-2ccf-49d0-b491-18312769dcda.png">

## Summary
### Pewlett Hackard will need to fill roles to fight the impact of the “silver tsunami.” Since there are 72458 employees who are ready to retire, Pewlett Hackard will need to bring 72458 employees on to fill the empty positions to make an impact. To figure out exactly how many roles need to be filled, we made a new table using the following code:
 ![image](https://user-images.githubusercontent.com/110864175/192913845-9594071d-2f04-4850-a070-d92f8ff96cc2.png)

### Although Pewlett-Hackard can bring these new employees on, they will need to be trained and mentored by seasoned employees. There are only 1549 number of qualified, retirement ready employees compared to 72458 employees who need to be trained. This means one trainer to roughly 47 trainees. There are not enough retirement-ready employees in the departments to mentor new Pewlett Hackard employees. I would recommend broadening age range to increase the number of qualified, retirement ready employees. To figure out how many qualifies, retirement ready employees there are that could be mentors, we made a new table using the following code:
![image](https://user-images.githubusercontent.com/110864175/192913864-1fc12280-6880-40e8-8985-32321e909978.png)
