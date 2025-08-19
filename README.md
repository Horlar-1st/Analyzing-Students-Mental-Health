## Analyzing-Students-Mental-Health
---
<img width="20%" align="right" alt="Github" src="https://github.com/Horlar-1st/Analyzing-Students-Mental-Health/blob/main/mentalhealth.jpg"/> 

Does going to university in a different country affect your mental health? A Japanese international university surveyed its students in 2018 and published a study the following year that was approved by several ethical and regulatory boards.

The study found that international students have a higher risk of mental health difficulties than the general population, and that social connectedness (belonging to a social group) and acculturative stress (stress associated with joining a new culture) are predictive of depression.

Explore the students data using PostgreSQL to find out if you would come to a similar conclusion for international students and see if the length of stay is a contributing factor.

Here is a data description of the columns you may find helpful.

| Field Name    | Description                                      |
| ------------- | ------------------------------------------------ |
| `inter_dom`     | Types of students (international or domestic)   |
| `japanese_cate` | Japanese language proficiency                    |
| `english_cate`  | English language proficiency                     |
| `academic`      | Current academic level (undergraduate or graduate) |
| `age`           | Current age of student                           |
| `stay`          | Current length of stay in years                  |
| `todep`         | Total score of depression (PHQ-9 test)           |
| `tosc`          | Total score of social connectedness (SCS test)   |
| `toas`          | Total score of acculturative stress (ASISS test) |


## 📝 The Question this Query Answers

- Among international students, how many are there in each stay category, and what are their average PHQ, SCS, and AS scores for each group?

- For international students, how does their stay status relate to both their group size and their average well-being scores (PHQ, SCS, and AS)? Specifically, how many international students fall into each stay category, and what are their average PHQ, SCS, and AS scores?


## 🔎 What the SQL Query Does

1. Filters data: Only includes students whose `inter_dom` = `'Inter'` (meaning international students).

2. Groups data: Groups the remaining students by the column `stay` (which represent length of stay in years).

3. Counts students: For each `stay` group, it counts how many international students (`'Inter'`) there are.

4. Computes averages: It calculates the average values of:
 - `todep` → stored as `average_phq` (maybe related to a PHQ depression score).
 - `tosc` → stored as `average_scs` (possibly a social connectedness score).
 - `toas` → stored as `average_as` (maybe an anxiety score or adjustment score).

5. Orders results: Displays results in descending order of stay.




## How to Use
---
- Download the repository as a zip file
- Extract the files
- Run the `notebook.ipynb`. It is an SQL code on Jupyter notebook
