# Study Tracker App

A console-based Java application designed to help students systematically log, track, summarize, and export their study activities.

## Platform Requirements

* **Platform:** Windows NT or Linux
* **User Interface:** Command Line Interface (CLI)
* **Technology:** Java Programming

## Project Overview

The **Study Tracker App** is a console-based Java application designed to help students systematically log, track, summarize, and export their study activities.

It allows users to maintain daily study records, view summaries grouped by date or subject, and export all logs into a CSV file for offline reference.

This project demonstrates the practical use of **Java Collections, File I/O, Date and Time API, and Object-Oriented Design** in a real-world utility application.

## Key Features

### 1. Insert Study Log

* Record study sessions with:

  * Date
  * Subject
  * Duration
  * Description
* The date is automatically generated using `LocalDate`.

### 2. Display All Logs

* View all study logs currently stored in memory.

### 3. Summary by Date

* Calculate and display total study hours grouped by date.

### 4. Summary by Subject

* Calculate and display total study hours grouped by subject.

### 5. Export to CSV

* Export all study logs into a CSV file named `MarvellousStudy.csv`.
* The exported file can be used for offline tracking and reference.

### 6. User-Friendly Console Menu

* Menu-driven interface.
* Uses `switch-case` for menu navigation.

## Technologies Used

### Language

* Java

### Packages and APIs

* `java.util.*`

  * `ArrayList` for storing study logs.
  * `TreeMap` for generating summaries.
  * `Scanner` for user input.

* `java.time.LocalDate`

  * Automatically captures the current date for study logs.

* `java.io.*`

  * Used for file handling and CSV export.

## Project Flow

```text
Launch Application
       |
       v
Main Menu
       |
       +---- 1. Insert Study Log
       |          |
       |          +-- Enter Subject
       |          +-- Enter Duration
       |          +-- Enter Description
       |          +-- Date automatically generated
       |
       +---- 2. Display All Study Logs
       |
       +---- 3. Summary By Date
       |
       +---- 4. Summary By Subject
       |
       +---- 5. Export to CSV
       |          |
       |          +-- MarvellousStudy.csv
       |
       +---- 6. Exit
```

## Classes and Responsibilities

### StudyLog

Represents a single study session.

**Attributes:**

* `LocalDate date`
* `String subject`
* `double duration`
* `String description`

**Methods:**

* Constructor
* Getters
* `toString()`

### StudyTracker

Manages all study logs stored in memory.

**Attribute:**

```java
ArrayList<StudyLog> database
```

**Methods:**

* `InsertLog()`
* `DisplayLog()`
* `SummaryByDate()`
* `SummaryBySubject()`
* `ExportCSV()`

### StudyTrackerApp

Main class of the application.

**Responsibilities:**

* Contains the `main()` method.
* Displays the menu-driven interface.
* Accepts user input.
* Calls the appropriate methods from `StudyTracker`.

## Example Usage

### Console Flow

```text
====== Marvellous Study Tracker ======

1. Insert Study Log
2. Display All Logs
3. Summary By Date
4. Summary By Subject
5. Export to CSV
6. Exit

Enter choice: 1

Enter Subject: Java Programming
Enter Duration (hours): 2.5
Enter Description: Practiced ArrayList and TreeMap

Study log added successfully for date: 2025-09-13
```

## Sample CSV Output

**MarvellousStudy.csv**

```csv
Date,Subject,Duration,Description
2025-09-13,Java Programming,2.5,Practiced ArrayList and TreeMap
2025-09-13,Database,1.5,Revised SQL Joins
```

## Concepts Demonstrated

* Java Classes and Objects
* Encapsulation
* Constructors
* ArrayList
* TreeMap
* Scanner
* LocalDate
* File I/O
* CSV File Handling
* `switch-case`
* Menu-driven Programming
* Object-Oriented Programming
