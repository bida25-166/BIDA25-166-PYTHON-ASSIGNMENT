PROJECT OVERVIEW
Student Grade Management System
This is a python-based grading system that is gradually developed. The grading system allows users to store and manage student records through operations such as adding, updating, removing and searching for students. The purpose of the system is to showcase the use and understanding of lists, tuples and dictionaries to manage and process data.
SETUP INSTRUCTIONS
1.	Install the latest PyCharm application
2.	Install Anaconda Navigator as an IDE
3.	Launch PyCharm and click create new project
4.	Rename your project and activate the project interpreter and virtual environment as well as the base interpreter (Anaconda).

FEATURES LIST
SECTION A
•	input student name
•	grade input and validation
•	total average grade calculation
•	average class grade calculation
•	print out student grade

SECTION B
•	Input multiple subject grades per student
•	Store grades in lists and tuples
•	Calculation of average grades for each student
•	Display highest and lowest grade 
•	Display summary table of student name, individual marks and their average


SECTION C
•	Nested dictionary to store student records
•	Add new student 
•	Update student grades
•	Remove student record
•	Search student by name
•	Display grades of a particular subject
SECTION D
•	Modularized program with functions
•	Search student name & update grades
•	Grade validation
•	Try/except error handling

SECTION E & F
•	Creating class & methods to add grades, calculate average and print student details
•	 Create gradebook class
•	 objects with methods to manage student records
•	Exception handling
•	Searching & sorting 


CLASS ARCHITECTURE
A nested dictionary named “student_grades{}” that stores another dictionary within itself listed with student grades as the values and the subjects as keys. An example of a structure is shown below;
{
'ruth’: 'math': [90], 
             'English': [78],
             'science': [65]}, 
'anaya’: 'math': [98],
                 'English': [76], 
                'science': [60]}
}



EXAMPLES OF INPUTS/OUTPUTS
INPUT- student number, names and grades
Input number of students
2
Student Number: 2

input student name
ruth

input math grade:90
input english grade:60
input science grade:77

input student name
anaya

input math grade:88
input english grade:70
input science grade:56

OUTPUT
Student Number: 2
{
'ruth’: 'math': [90], 
             'English': [60],
             'science': [77]}, 
'anaya’: 'math': [88],
                 'English': [70], 
                'science': [56]}
}

INPUT
input new name: omatla
input math grade:67
input english grade:72
input science grade:45

OUTPUT
student successfully added

INPUT- update student grade
input new name to update: ruth
input subject name: math
input new grade:94

OUTPUT
grade successfully updated

INPUT- remove students
input student name to remove:

OUTPUT
student not found

INPUT- view subject mark
input subject to view: science

OUTPUT
[77]
[56]
[45]

OUTPUT- total grades, class average & student grade average
Total Student Grades: 184
Average Mark: 20.444444444444443
ruth 77.0
anaya 71.33
omatla 61.33

INPUT-check specific student grades
input student name to check: omatla

OUTPUT
{'math': [67], 'English': [72], 'science': [45]} 61.333333333333336

OUTPUT- highest/lowest grade

Highest math grade: 90
Lowest math grade: 88
Highest english grade: 70
Lowest english grade: 60
Highest science grade: 77
Lowest science grade: 56

OUTPUT – student summary table
name	math	english	science	average
ruth [94] [60] [77] 77.0
anaya [88] [70] [56] 71.33
omatla [67] [72] [45] 61.33





SECTION D STRUCTURE
•	Subject_input () -> captures student name and grades
•	Student_add () -> capture new student record
•	Update () -> check student name & update subject grade
•	Remove_student () -> remove student record
•	Subject_view () -> view specific subject grades
•	Mark_add () -> add all student subject marks
•	Average_subject_mark () -> calculate class average
•	Grade_average () -> calculate individual student average
•	Display_grade_average () ->display student grades alongside the grade average
•	Student_statistics () -> display highest/lowest grade for each subject
•	Student_display () -> display student summary table
ERROR HANDLING
Try/except blocks were used to handle errors caused by;
•	Non-numeric grade input
•	Input of invalid grade ranges
•	Search for non-existent student records






SECTION E & F COMPREHENSIVE TESTING
1. Functional Testing
Test Case	Input	Expected Result	Actual Result	Status
Add Student	Ruth, 90, 85, 70	Student added successfully	Student added successfully	PASS
Search Student	Ruth	Display student details	Student details displayed	PASS
Remove Student	Ruth	Student removed successfully	Student removed successfully	PASS
Sort Students	Multiple student records	Students sorted by average	Students sorted by average	PASS
2. Validation Testing
Test Case	Input	Expected Result	Actual Result	Status
Invalid Grade	150	Grade must be between 0 and 100	Grade must be between 0 and 100	PASS
Negative Grade	-5	Grade must be between 0 and 100	Grade must be between 0 and 100	PASS
Non-numeric Grade	abc	ERROR: non-numeric grade entered	ERROR: non-numeric grade entered	PASS
Duplicate Student Name	Ruth (already exists)	Duplicate student name not allowed	Duplicate student name not allowed	PASS
3. Exception Handling Testing
Test Case	Input	Expected Result	Actual Result	Status
Search for Non-existent Student	Joshua (does not exist in records)	StudentNotFoundError: Student not found	Student not found	PASS
Remove Non-existent Student	Joshua (does not exist in records)	StudentNotFoundError: Student not found	Student not found	PASS
4. Edge Case Testing
Test Case	Expected Result	Actual Result	Status
Student with No Grades	Average = 0	Average = 0	PASS
Large Number of Students	Program remains responsive	Program remains responsive	PASS
Special Characters in Name	Accepted as valid names	Successfully accepted	PASS
The system was tested using functional, validation, exception-handling, and edge-case test scenarios. The program recovered from invalid inputs without crashing and behaved as expected.

TESTING SUMMARY
Test Case	Expected Result	Actual Result	Status
Add Student	Student successfully added	Student successfully added	PASS
Update Grade	Grade successfully updated	Grade successfully updated	PASS
Remove Student	Student successfully removed	Student successfully removed	PASS
Search Student	Student grades displayed	Student grades displayed	PASS
Invalid Grade (-1/150)	Invalid subject grade	Invalid subject grade	PASS
The system was thoroughly tested, including unit tests for individual methods and integration tests for the overall system functionality. The program recovered successfully from invalid inputs without crashing and behaved as expected.


ASSUMPTIONS & LIMITATIONS
ASSUMPTIONS
•	Names are unique
•	Grades entered are integers
•	Grades range from 0 -100
•	Names of subject should match the stored subject names
LIMITATIONS
•	The program supports only 3 subjects. Math, English and science.
•	Names and subject names are case sensitive
•	Data is only stored when the program is running

TESTING SUMMARY
Test Case	Expected Result	Actual Result	Status
Add Student	Student successfully added	Student successfully added	PASS
Update Grade	Grade successfully updated	Grade successfully updated	PASS
Remove Student	Student successfully removed	Student successfully removed	PASS
Search Student	Student grades displayed	Student grades displayed	PASS
Invalid Grade (-1/150)	Invalid Math grade, Invalid English grade, Invalid Science grade	Invalid Math grade, Invalid English grade, Invalid Science grade	PASS

KNOWN ISSUES
•	Floating point averages may produce long decimals
•	Structural change from integers to lists and dictionaries prompted modifications in existing calculation functions to avoid errors.
•	Structural change from functions to classes with methods required modification to existing code to avoid errors or the program crashing.

REFERENCES
W3SCHOOLS. Python tutorial available at Python Tutorial
Python lecture slides


