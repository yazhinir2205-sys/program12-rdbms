# Lab Program 12 – ER Diagram for College Management System

## Aim

To create an Entity-Relationship (ER) diagram for a College Management System using MySQL Workbench.

## Problem Statement

Draw an ER diagram for a College Management System including the following entities:

* Student
* Course
* Faculty
* Department

Use the following relationships:

1. One Department has many Students.
2. One Faculty handles many Courses.
3. Many Students can enroll in many Courses.

Clearly represent the relationship cardinalities:

* One-to-One (1:1)
* One-to-Many (1:M)
* Many-to-Many (M:N)

## Software Required

* MySQL Workbench
* GitHub account
* Git

## Required Entities

The EER model must contain the following four entities:

### Student

Suggested attributes:

* StudentID – Primary Key
* StudentName
* Email
* Phone

### Course

Suggested attributes:

* CourseID – Primary Key
* CourseName
* Credits

### Faculty

Suggested attributes:

* FacultyID – Primary Key
* FacultyName
* Email

### Department

Suggested attributes:

* DepartmentID – Primary Key
* DepartmentName

Students may add additional meaningful attributes.

## Required Relationships

### 1. Department – Student

```text
Department 1 ───────── N Student
```

Relationship type:

**One-to-Many (1:M)**

Meaning:

> One Department has many Students.

---

### 2. Faculty – Course

```text
Faculty 1 ───────── N Course
```

Relationship type:

**One-to-Many (1:M)**

Meaning:

> One Faculty handles many Courses.

---

### 3. Student – Course

```text
Student M ───────── N Course
```

Relationship type:

**Many-to-Many (M:N)**

Meaning:

> Many Students can enroll in many Courses.

In a relational implementation, this M:N relationship can be represented using an associative entity such as:

```text
Enrollment
----------------
EnrollmentID
StudentID
CourseID
```

Students should represent the M:N relationship appropriately in their Workbench model.

## One-to-One Relationship

The given College Management System requirements do **not require a 1:1 relationship**.

Students must clearly understand the difference between:

```text
1 : 1  → One-to-One
1 : N  → One-to-Many
M : N  → Many-to-Many
```

The required relationships for this practical are:

```text
Department 1 : N Student
Faculty    1 : N Course
Student    M : N Course
```

## MySQL Workbench Instructions

1. Open MySQL Workbench.
2. Select **File → New Model**.
3. Create the required tables/entities.
4. Add the required attributes.
5. Mark the appropriate primary keys.
6. Create the required relationships.
7. Ensure the cardinalities are correctly represented.
8. Resolve the M:N Student–Course relationship using an appropriate associative entity if required.
9. Arrange the model clearly.
10. Save the model.

## Required Submission Files

Students must submit:

```text
ER_Diagram.mwb
ER_Diagram.png
model_check.txt
```

### ER_Diagram.mwb

The original MySQL Workbench model file.

### ER_Diagram.png

Export the EER diagram from MySQL Workbench as a PNG image.

The image must clearly show:

* Entity names
* Attributes
* Primary keys
* Relationships
* Cardinalities

### model_check.txt

Complete the checklist provided in the starter repository.

## GitHub Submission

After completing the practical:

```bash
git add .
git commit -m "Completed Lab Program 12"
git push
```

Open the **Actions** tab in GitHub to view the automated checking result.

## Important

Do not modify:

```text
test.sh
.github/workflows/autograding.yml
```

## Learning Outcome

After completing this practical, students will be able to:

* Identify entities and attributes.
* Identify primary keys.
* Create an EER model using MySQL Workbench.
* Represent one-to-many relationships.
* Represent many-to-many relationships.
* Understand one-to-one, one-to-many and many-to-many cardinalities.
* Export an EER model as a visual diagram.
