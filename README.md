# Overview of analysis

The purpose of this analysis is to prepare Pewlett-Hackard, a company with several thousand employees, for the upcoming retirement. A large number of employees will begin retiring at a rapid rate in the next few years and the company wants to be prepared with the retirement packages, open positions and employees’ training. In order to ensure a smooth transition this analysis focuses on the following:

1. Identify the retiring employees by their title.
2. Determine the sum of retiring employees grouped by title.
3. Identify the employees eligible for participation in the mentorship program.
4. Determine the number of roles-to-fill grouped by title and department.
5. Determine the number of qualified, retirement-ready employees to mentor the next generation grouped by title and department.

# Background
The data is gathered in six CSV files and the analysis is performed using relational databases. In this analysis I am using:

- QuickDBD to create quick database design for better visualization,
- PostreSQL a database system to load, build and host company’s data, and
- pgAdmin a GUI, using SQL Language to explore, manipulate and extract the data.


# Results
1. The list of retiring employees

- The table includes employee number, first name, last name, title, from-date and to-date.
- The query returns 133,776 rows.
- The table displays a list of employees who is going to retire in the next few years.
- The list is long and extensive, yet at-a-glance analysis gives us some insights about the query. Some employees appear more than once due to change of title during their career at Pewlett-Hackard.

2. The list of retiring employees without duplicates

- The table includes employee number, first name, last name, title, from-date and to-date.
- The query returns 90,398 rows.
- The table displays a list of employees who are going to retire in the next few years.
- In the table each employee is listed only once, by her or his most recent title.

3. The number of retiring employees grouped by title

- The table includes employees’ titles and their sum.
- The query returns a cohesive table with 7 rows.
- From this table we can quickly see how many employees with certain title will retire in the next few years.

4. The employees eligible for the mentorship program

- The table contains employee number, first name, last name, birth date, from date, to date and title.
- The query returns 1,549 rows.
- The table displays a list of employees who is eligible for the mentorship program.

# Summary

As the company is preparing for the upcoming retirement, a good planning is essential, especially when such a large number of the employees is involved. Reports above give a good insight about the number of the employees that are about to retire and hold specific title. However, I believe that additional break down per department will be beneficial for the company. In this case headquarters can see what to expect in each department separately. In order to retrieve department name information, I merged additional table departments into existing table retirement_titles with the inner join. After removing the duplicates, with DISTINCT ON command, the table was ready to be used for additional queries.
