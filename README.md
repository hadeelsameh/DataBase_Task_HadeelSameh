# DataBase Task
### Author: Hadeel Sameh Hassan

## Discribtion:

1. **Import the provided excel sheet into any relational database**
    Xampp server was used to create database and the csv file was uploaded.
2. **Answers these questions:**
    1. **Which drink has the highest calories from the dataset ?**
        `SELECT Beverage 
            FROM `drinkmenu` 
            WHERE Calories = (SELECT MAX(Calories) FROM `drinkmenu`);` query was used to get the solution.
        the silution is " White Chocolate Mocha (Without Whipped Cream)".
`
    2. **What is the average calorie amount for each drink category ?**
        `SELECT Beverage_category , AVG(Calories) 
        FROM `drinkmenu` 
        GROUP BY Beverage_category;
        ` query was used and results are attached in `Question2_Answer.PNG`

    3. **Which drinks have below average calorie amount ?**

        `SELECT Beverage FROM `drinkmenu` 
        JOIN (SELECT Beverage_category as bc , AVG(Calories) as avgc FROM `drinkmenu` GROUP BY Beverage_category) r 
        ON Beverage_category = r.bc 
        WHERE Calories < r.avgc;` query was used and results are attached in `Question3_Answer.pdf`






## User Instructions :
* User only needs to have any relational Database ingine to create database , import csv file and run the queries provided in `queries.txt` . 

* Results are attached in screenshots.


