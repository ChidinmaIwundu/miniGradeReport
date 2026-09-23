#  Student Grade Calculator — Java

## Project Overview

This project is a simple **Java Student Grade Calculator** that demonstrates object-oriented programming concepts by creating student objects, storing their scores, calculating their average scores, and assigning letter grades based on their performance.

The project is designed as a beginner-friendly Java application for practicing **classes, objects, arrays, methods, constructors, loops, and conditional statements**.

---

##  Project Objectives

The program is designed to:

- Create student objects using a Java class.
- Store each student's name and scores.
- Calculate the average score for each student.
- Convert the average score into a letter grade.
- Display each student's name, average, and grade.

---

##  Technologies Used

- **Java**
- Object-Oriented Programming (OOP)
- Arrays
- Methods
- Constructors
- `for` loops
- Conditional statements (`if`, `else if`, `else`)

---

## Project Structure

```text
Student-Grade-Calculator/
│
├── Student.java
├── Main.java
└── README.md
```

---

## How It Works

### 1. Student Class

The `Student` class represents a student and contains two main attributes:

```java
String name;
int[] scores;
```

- `name` stores the student's name.
- `scores` stores the student's test scores.

---

### 2. Constructor

The constructor initializes each student's name and scores:

```java
public Student(String name, int[] scores) {
    this.name = name;
    this.scores = scores;
}
```

This allows a new student to be created with their information immediately.

---

### 3. Calculating the Average

The `getAverage()` method calculates the student's average score.

```java
public double getAverage() {
    int sum = 0;

    for (int i = 0; i < scores.length; i++) {
        sum += scores[i];
    }

    return (double) sum / scores.length;
}
```

The program:

1. Starts the total at `0`.
2. Loops through every score.
3. Adds each score to the total.
4. Divides the total by the number of scores.



---

### 4. Assigning a Letter Grade

The `getLetterGrade()` method uses the student's average to determine their grade:

| Average | Grade |
|---:|:---:|
| 90–100 | A |
| 80–89 | B |
| 70–79 | C |
| 60–69 | D |
| Below 60 | F |

For example:

```java
if (avg >= 90) {
    return "A";
} else if (avg >= 80) {
    return "B";
} else if (avg >= 70) {
    return "C";
} else if (avg >= 60) {
    return "D";
} else {
    return "F";
}
```

---

## Sample Students

The program creates three students:

```java
students[0] = new Student("Amara", new int[]{85, 92, 78, 90});
students[1] = new Student("Tunde", new int[]{60, 70, 65, 72});
students[2] = new Student("Chidi", new int[]{95, 89, 93, 97});
```

### Expected Output

```text
Amara - Average: 86.25, Grade: B
Tunde - Average: 66.75, Grade: D
Chidi - Average: 93.5, Grade: A
```

---

## Concepts Demonstrated

This project demonstrates several fundamental Java concepts:

### Object-Oriented Programming
The `Student` class is used as a blueprint for creating multiple student objects.

### Arrays
An integer array stores multiple scores for each student.

### Constructors
The constructor initializes each object with its required data.

### Methods
`getAverage()` and `getLetterGrade()` encapsulate specific operations.

### Loops
A `for` loop is used to iterate through the student's scores.

### Conditional Logic
`if`, `else if`, and `else` statements determine the student's letter grade.

### Type Casting
The average calculation uses:

```java
(double) sum / scores.length
```

This ensures that the division produces a decimal value rather than integer division.

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/student-grade-calculator.git
```

### 2. Navigate into the project

```bash
cd student-grade-calculator
```

### 3. Compile the Java files

```bash
javac Student.java Main.java
```

### 4. Run the program

```bash
java Main
```

---

## 🚀 Possible Improvements

The project can be expanded by adding:

- User input instead of hard-coded students.
- More students and subjects.
- GPA calculation.
- Highest and lowest score detection.
- Class-wide average.
- Pass/fail status.
- Input validation.
- A graphical user interface.
- File/database storage for student records.

---

## 📚 Learning Outcome

This project provides practical experience with the fundamentals of Java programming and object-oriented design for fun. It demonstrates how raw student scores can be transformed into useful academic information through **data structures, calculations, and conditional logic**.

---


This project can serve as a foundation for a more complete **Student Management System**, where student information, scores, grades, and academic performance can be managed through a structured application.
