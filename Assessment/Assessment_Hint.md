# Assessment Hints

# Section 1 - Beginner
1. **Flexible Solution**

    The expected solution doesn’t have to follow the exact working of the question if you have a better or more efficient approach that works well. The focus is really on applying the topics we’ve covered in class—using variables, lists, functions, and loops, however it still needs to follow the necessary **requirements**:
    - A budget variable
    - Two lists to store item names and prices
    - Two specific functions:
    i. `add_item_to_cart(item_name, item_price)` – This should add the item’s name and price to their respective lists.
    ii. `calculate_total(item_prices)` – This should calculate and return the total of the prices in the list. 
    - You follow the loop conditions, and the output format

2. **Separating Logic**

    You don’t need to handle all conditions in `calculate_total`. For instance, you can check if the budget is exceeded or if a discount should apply outside the functions, in the main program that manages the shopping cart. This keeps `calculate_total` focused on just calculating the total.

3. **Simplified Goal**

    In case the wording of the question is confusing, here's a simplified goal to help you understand the question better:
    - Take input for items and their prices, and store them in their respective lists.
    - Keep a running total of prices (updating the total each time an item is added)
    - If the total exceeds $200 (budget), or when the user enters 'done,' stop adding items.
    - Apply a 10% discount *only if the final total (after all items are added)* is over $100.

# Section 3 - Advanced

### Section 3 Part B: Group the dataset by `Industry` and calculate the average `Hours_Worked_Per_Week` for each combination. (5 marks)

**Explanation:**

`Job_Role` and `Industry` have a many-to-many relationship, meaning there are numerous job types that span across multiple industries.
For instance: A Data Scientist job type might exist in industries like healthcare, education, technology, etc. Here, the task is to group the data by Industry and compute the average `Hours_Worked_Per_Week` for all job roles in each industry.
This will help identify which industries, on average, have the highest or lowest work hours across all associated job roles.

### Section 3 Part C: Use a bar chart to display the average Stress_Level for each job_role, with separate bars for high and low stress levels. (5 marks)

To better understand the question, let’s break it into actionable steps:
  1. Use a bar chart
  2. Display the average `Stress_Level`
  3. For each `job_role`
  4. With separate bars for high and low stress levels.

**Explanation**

  Step 1: Since `Stress_Level` contains non-numeric values, first convert them into numeric values using a scale, i.e., low = 1, medium = 2, and high = 3.
  
  Step 2: To calculate the average, group the data by `job_role` and compute the average `Stress_Level` for each role.
  
  Step 3: Use this data to create a bar chart
  
**Clarifying the Confusion**

The phrase *“separate bars for high and low stress levels”* is to be  interpreted as follows:
- We know that the numeric value for high stress level is always 3, and for low stress level, it’s always 1. These are fixed values across all job_roles.
- Therefore, calculating the average of these fixed values (3 and 1) for high and low stress levels will always result in 3 and 1, respectively, which isn't very meaningful.
- Instead, the expectation is to show the count of high and low stress levels for each `job_role` using separate bars. This interpretation makes the data more insightful and aligns with the question’s intent.

There are two possible approaches to visualize this:

1. Single Graph with 3 Bars Per Job Role
    - One bar for the average `Stress_Level`.
    - Two additional bars for the count of high stress levels and low stress levels for each `job_role`.

2. Subplots (1x2 or 2x1 Layout)
    - One plot dedicated to the average `Stress_Level` for each `job_role`.
    - Another plot showing the counts of high and low stress levels for each `job_role`.

Both approaches will help you make the same analysis. Choose the one that makes the analysis easier to interpret for the reader.

### **Section 3 Part D - Analyze the results: Which job roles and workload levels appear to have the greatest impact on mental health? (5 marks)**

**What is asked:**

The relationship between job roles and workload levels and their impact on mental health.

**What we have:**

1. Workload levels (based on hours worked per week)
2. Relation between job type and stress level

**Possible approach:**
1. Identify Workload Levels for Each Job Type:
   - To determine the workload, calculate the average hours worked per week for each job type.
   - Compare the average hours for each job type with the overall average work hours per week (performed in part A). If a job type’s average work hours exceed the overall average, it is considered to have a high workload.

2. Calculate Overall Average Stress Level:
   - Find the average stress level for each job type (performed in part C).
   - Compute the overall average stress level by averaging the stress levels across all job types.
   - Compare the stress level of each job type with the overall average. Job types with a higher-than-average stress level will indicate higher impact.

4. Conclusion:
   - Job roles with both higher average work hours (above the overall average) and higher average stress levels (above the overall average) are likely to have the greatest impact on mental health.

*(Note: While stress level is not directly part of the question, it is a key indicator of mental health, and its inclusion is necessary to fully address the impact of workload on mental well-being.)*

Example - 
If the overall average of `working hours = 39.61` and overall average of `stress level = 2.008`
Then from the [image], we can conclude that only Marketing, Project Manager and Sales jobs have the greatest impact on mental health.
![image](https://github.com/user-attachments/assets/ba23027c-37d7-4298-8c98-ca484a38ec66)


I hope this gives some more clarity and makes the questions easier to understand. Focus on getting these parts working with the required elements, and don’t worry about making it overly complex.
