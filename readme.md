# EAS503 Spring 2021

## Topics (Tentative)
- Week 1  - 8/30/2021 -- Python Programming: Introduction, Python Basics (data types, mathematical operations, variables), Functions, NBGrader 
- Week 2  - 9/6/2021 -- Python Programming: Function Examples, Strings, Strings Examples, String Methods
- Week 3  - 9/13/2021 -- Python Programming: Making Choices/Flow Control/Conidtionals Examples, 
- Week 4  - 9/20/2021 -- Python Programming: Lists, Tuples, Loops, File Handling, Modify loop execution, while loops, List Comprehension, Sets, Dictionaries, Lambda, Filter, Map, Sorting, 
- Week 5  - 9/27/2021 -- Python Programming: Modify loop execution, while loops, List Comprehension, Sets, Dictionaries, Lambda, Filter, Map, Sorting, Matplotlib Part 1
- Week 6  - 10/4/2021 -- Python Programming: Lambda, Filter, Map, Sorting,
- Week 7  - 10/11/2021 -- Python Programming: Python Errors, Exception Handling, Matplotlib Part 2
- Week 8  - 10/18/2021 -- Python Programming: Function Input, Scope, Object-Oriented Programming, Generators, and Iterators
- Week 9  - 10/25/2021 -- Object-Oriented Programming, Generators, and Iterators; Database Concepts: SQLite3
- Week 10  - 11/1/2021 -- Database Concepts: SQLite3 continued, Python and Database
- Week 11 - 11/8/2021  -- Working with Data: Numpys, Pandas, and database
- Week 12 - 11/15/2021 -- Visualization: Linking Database to Pandas and Visualization (matplotlib, seaborn, plotly)
- Week 13 - 11/22/2021 -- Machine Learning with Python 1 (only one class due to fall recess)
- Week 14 - 11/29/2021 -- Machine Learning with Python 1 (continue)
- Week 15 - 12/6/2021 --  Machine Learning with Python 2

## Grading
- Homework (8) -- 50%
- Labs (2) -- 30%
- Project (1) -- 20%
- No final!

### Midterm Grade

```python
#%%
# midterm grade
def average_normalized_score(hw1, hw2, hw3):
    """ Return average normalized score in range 0 to 100. Every homework is normalized to 100.
    hw1 - max score 116, hw2 - max score 100, hw3 - max score 98,
    """
    hw1_norm = 100 * hw1 / 116
    hw2_norm = hw2
    hw3_norm = 100 * hw3 / 98
    avg_score = (hw1_norm + hw2_norm + hw3_norm) / 3
    return avg_score

def get_letter_grade(score):
    """Return letter grade based on 100-normalized score"""
    score=int(round(score))
    if score >= 95:
        return "A"
    elif score >= 90:
        return "A-"
    elif score >= 87:
        return "B+"
    elif score >= 83:
        return "B"
    elif score >= 80:
        return "B-"
    elif score >= 77:
        return "C+"
    elif score >= 73:
        return "C"
    elif score >= 70:
        return "C-"
    elif score >= 67:
        return "D+"
    elif score >= 63:
        return "D"
    elif score >= 60:
        return "D-"
    else:
        return "F"
```

## Homework Dates (Tentative)
- Homework will be posted by Sundays @ 11:59 PM EST 
- Homework will be due on the date listed @ 11:59 PM EST
- No late homework will be accepted, not even for partial credit
- Homework 0  -- release date: ???; due 9/12/2021 -- Does not count toward grade
- Homework 1  -- release date: 9/12/2021; due 9/19/2021
- Homework 2  -- release date: 9/19/2021; due 9/26/2021
- Homework 3  -- release date: 9/26/2021; due 10/10/2021
- Homework 4  -- release date: 10/10/2021; due 10/17/2021
- Homework 5  -- release date: 10/24/2021; due 10/31/2021 
- Homework 6  -- release date: 10/31/2021; due 11/7/2021
- Homework 7 -- release date: 12/2/2021; due 12/12/2021
- Homework 8 -- release date: 12/9/2021; due 12/19/2021


## Lab Dates (Tentative)
- Labs will be due on the date listed @ 11:59 PM EST
- No late labs will be accepted, not even for partial credit
- Lab 1 -- release date: 10/17/2021; due 10/31/2021
- Lab 2 -- release date: 11/7/2021; due 12/02/2021

## Project Dates (Tentative)
- 10/18/2021 -- Form groups on UB Learns
- 11/7/2021 -- Submit project description on UB Learns
- 12/04/2021 -- Submit preliminary report on UB Learns
- 12/17/2021 -- Submit video presentation
- 12/20/2021 -- Watch 5 other presentation and provide feedback, final report and code
