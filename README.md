BIDA25-166 ASSIGNMENT README
ASSIGNMENT SUBMISSION COVER SHEET
Student Information
Student ID: BIDA25-166

Student Name: Ruth Ketshabile

Student Email: Bida25-166@thuto.bac.ac.bw

Cohort: July 2025

Assignment Title: Introduction to Python Programming

Date of Submission: 22 October 2026

Programme of Study: Business Intelligence & Data Analytics

Year of Study: 2026

Declaration
By checking the box below, I certify that this assignment is my own work and is free from plagiarism. I understand that the assignment may be checked for plagiarism by electronic or other means and may be transferred and stored in a database for the purposes of data matching to help detect plagiarism. The assignment has not previously been submitted for assessment in any other unit or to any other institution.

I have read and understood the Botswana School of Business Sciences plagiarism guidelines policy.

☒ Agree

Signature: R. Ketshabile

Date: 22 October 2026

PROJECT OVERVIEW
Student Grade Management System
This is a Python-based grading system developed progressively throughout Sections A to F of the assignment. The system allows users to store and manage student records through operations such as adding, updating, removing and searching for students. The purpose of the system is to demonstrate the use of lists, tuples, dictionaries, functions, classes, searching, sorting and exception handling.

SETUP INSTRUCTIONS
Install the latest version of PyCharm.
Install Anaconda Navigator.
Launch PyCharm and select Create New Project.
Rename the project.
Configure the project interpreter and virtual environment.
Select the Anaconda Base Interpreter.
FEATURES LIST
SECTION A
Input student name
Grade input and validation
Total average grade calculation
Average class grade calculation
Print student grades
SECTION B
Input multiple subject grades per student
Store grades using lists and tuples
Calculate average grades for each student
Display highest and lowest grades
Display summary table of student grades and averages
SECTION C
Nested dictionary to store student records
Add new student
Update student grades
Remove student record
Search student by name
Display grades of a particular subject
SECTION D
Modularized program using functions
Search student records and update grades
Grade validation
Try/Except error handling
SECTION E & F
Student class with methods
GradeBook class
Object-oriented record management
Exception handling
Searching and sorting functionality
CLASS ARCHITECTURE
A nested dictionary named student_grades stores student records. Student names act as keys while subjects and grades are stored in nested dictionaries.

Example Structure
student_grades = {
    "ruth": {
        "Math": [90],
        "English": [78],
        "Science": [65]
    },
    "anaya": {
        "Math": [98],
        "English": [76],
        "Science": [60]
    }
}
EXAMPLES OF INPUTS AND OUTPUTS
Student Record Input
Input
Input number of students: 2

Input student name: ruth
Input Math grade: 90
Input English grade: 60
Input Science grade: 77

Input student name: anaya
Input Math grade: 88
Input English grade: 70
Input Science grade: 56
Output
{
    "ruth": {
        "Math": [90],
        "English": [60],
        "Science": [77]
    },
    "anaya": {
        "Math": [88],
        "English": [70],
        "Science": [56]
    }
}
Add Student
Input
Input new name: omatla
Input Math grade: 67
Input English grade: 72
Input Science grade: 45
Output
Student successfully added
Update Student Grade
Input
Input student name: ruth
Input subject: Math
Input new grade: 94
Output
Grade successfully updated
Remove Student
Output
Student not found
View Subject Marks
Output
[77]
[56]
[45]
Grade Statistics
Total Student Grades: 184
Average Mark: 20.44

ruth   77.00
anaya  71.33
omatla 61.33
Search Student
Output
{'Math': [67], 'English': [72], 'Science': [45]}
Average = 61.33
Highest and Lowest Grades
Highest Math Grade: 90
Lowest Math Grade: 88

Highest English Grade: 70
Lowest English Grade: 60

Highest Science Grade: 77
Lowest Science Grade: 56
Student Summary Table
Name	Math	English	Science	Average
Ruth	94	60	77	77.00
Anaya	88	70	56	71.33
Omatla	67	72	45	61.33
SECTION D STRUCTURE
subject_input() → Captures student name and grades
student_add() → Captures a new student record
update() → Updates student grades
remove_student() → Removes a student record
subject_view() → Displays grades for a specific subject
mark_add() → Adds all subject marks
average_subject_mark() → Calculates class average
grade_average() → Calculates student average
display_grade_average() → Displays student averages
student_statistics() → Displays highest and lowest grades
student_display() → Displays student summary table
ERROR HANDLING
Try/Except blocks were used to handle:

Non-numeric grade input
Invalid grade ranges
Searching for non-existent student records
SECTION E & F COMPREHENSIVE TESTING
Functional Testing
Test Case	Input	Expected Result	Actual Result	Status
Add Student	Ruth, 90, 85, 70	Student added successfully	Student added successfully	PASS
Search Student	Ruth	Display student details	Student details displayed	PASS
Remove Student	Ruth	Student removed successfully	Student removed successfully	PASS
Sort Students	Multiple student records	Students sorted by average	Students sorted by average	PASS
Validation Testing
Test Case	Input	Expected Result	Actual Result	Status
Invalid Grade	150	Grade must be between 0 and 100	Grade must be between 0 and 100	PASS
Negative Grade	-5	Grade must be between 0 and 100	Grade must be between 0 and 100	PASS
Non-numeric Grade	abc	ERROR: non-numeric grade entered	ERROR: non-numeric grade entered	PASS
Duplicate Student Name	Ruth (already exists)	Duplicate student name not allowed	Duplicate student name not allowed	PASS
Exception Handling Testing
Test Case	Input	Expected Result	Actual Result	Status
Search Non-existent Student	Joshua	StudentNotFoundError: Student not found	Student not found	PASS
Remove Non-existent Student	Joshua	StudentNotFoundError: Student not found	Student not found	PASS
Edge Case Testing
Test Case	Expected Result	Actual Result	Status
Student With No Grades	Average = 0	Average = 0	PASS
Large Number of Students	Program remains responsive	Program remains responsive	PASS
Special Characters in Name	Accepted as valid names	Successfully accepted	PASS
The system was tested using functional, validation, exception-handling and edge-case scenarios. The program recovered successfully from invalid inputs without crashing.

ASSUMPTIONS & LIMITATIONS
Assumptions
Names are unique
Grades entered are integers
Grades range from 0–100
Subject names must match stored subject names
Limitations
The program supports only three subjects:
Math
English
Science
Names and subject names are case-sensitive
Data is only stored while the program is running
TESTING SUMMARY
Test Case	Expected Result	Actual Result	Status
Add Student	Student successfully added	Student successfully added	PASS
Update Grade	Grade successfully updated	Grade successfully updated	PASS
Remove Student	Student successfully removed	Student successfully removed	PASS
Search Student	Student grades displayed	Student grades displayed	PASS
Invalid Grade (-1/150)	Invalid Math grade, Invalid English grade, Invalid Science grade	Invalid Math grade, Invalid English grade, Invalid Science grade	PASS
KNOWN ISSUES
Floating-point averages may produce long decimal values.
Structural changes from integers to lists and dictionaries required updates to calculation functions.
Structural changes from functions to classes required modifications to prevent errors and crashes.
REFERENCES
W3Schools Python Tutorial
https://www.w3schools.com/python/
Python Documentation
https://docs.python.org/3/

Python Lecture Slides

PyCharm Documentation
https://www.jetbrains.com/pycharm/
