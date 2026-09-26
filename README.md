Student Record Application

A simple Student Record Application built using HTML, CSS, and JavaScript.

This project allows users to search, filter, and view student records based on their name, section, and performance status. It also calculates student averages and provides a class performance summary.

Features
Display student records in a table
Search students by name
Filter students by section
Filter students by status
Find a student using their ID
Calculate individual student averages
Determine whether a student passed or needs improvement
Calculate the overall class average
Display the number of passing students
Responsive design for smaller screens
Technologies Used
HTML5 – Structure of the application
CSS3 – Styling, layout, and responsive design
JavaScript (ES6+) – Application logic and data processing
JavaScript Modules – Separating student data from application logic
Project Structure
student-record-application/
│
├── index.html
│
├── css/
│   └── style.css
│
├── js/
│   ├── app.js
│   └── students.js
│
└── README.md
How to Run
Download or clone this repository.
Open the project folder in VS Code.
Make sure the file structure matches the structure above.
Open the project using Live Server.

Because the application uses JavaScript modules (type="module"), it is recommended to run it through a local development server instead of opening index.html directly.

Student Data

The student records are stored in students.js.

Example:

{
  id: 101,
  name: "Ana Santos",
  section: "A",
  scores: [90, 85, 88]
}

Each student contains:

id – Unique student ID
name – Student's name
section – Student's section
scores – Array containing the student's scores
Grade Calculation

The application calculates the average of the student's scores.

For example:

Scores: 90, 85, 88

Average = (90 + 85 + 88) / 3
Average = 87.67

A student is considered Passed when the average is 75 or higher.

isPassed: average >= 75

Students below 75 are displayed as Needs Improvement.

Search and Filters
Search by Name

Users can enter a name in the search field.

Example:

Ana

The application will display students whose names contain the search keyword.

Filter by Section

Users can filter students by:

All Sections
Section A
Section B
Section C
Filter by Status

Users can filter students by:

All Students
Passed
Needs Improvement

Multiple filters can be used at the same time.

Find Student by ID

Users can enter a student ID and click Find Student.

Example:

Student ID: 101

The application displays:

Ana Santos | Section A | Average: 87.67 | Passed
Class Summary

The application displays:

Number of students shown
Overall class average
Number of passing students

Example:

6 student(s) shown
Class Average: 81.92
Passing Students: 5 of 6
JavaScript Concepts Used

This project demonstrates several JavaScript concepts:

Variables
Arrays
Objects
Functions
Arrow functions
Destructuring
Spread syntax
ES6 Modules
map()
filter()
find()
reduce()
includes()
Template literals
DOM manipulation
Event listeners
Form/input handling
Conditional logic
Main JavaScript Functions
calculateAverage()

Calculates the average of a student's scores.

const calculateAverage = (scores) => {
  const total = scores.reduce((sum, score) => sum + score, 0);
  return total / scores.length;
};
renderStudents()

Displays the student records in the HTML table.

renderSummary()

Calculates and displays the class average and number of passing students.

applyFilters()

Filters the student records based on:

Name
Section
Status
findStudentById()

Searches for a student using their unique ID.

Responsive Design

The application includes a media query for smaller screens.

On screens smaller than 720px:

Filters are displayed in one column.
The student lookup controls are displayed vertically.
The table can scroll horizontally when needed.
Future Improvements

Possible improvements for this project:

Add new students
Edit student records
Delete student records
Add more subjects
Add individual subject names
Add sorting by average
Add pagination
Store data using localStorage
Connect to a backend API
Add a database
Add student authentication
Author

Created as a Full Stack Development learning project.