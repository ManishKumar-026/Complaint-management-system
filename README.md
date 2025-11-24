# Complaint Management System (Python Desktop Application)

This repository contains the source code for a simple *Complaint Management System* desktop application developed in Python. This system allows users to submit complaints through a graphical user interface (GUI) and stores the data persistently in a local SQLite database.

The functionality and design of this project are fully documented in the accompanying project report.

## 📄 Associated Document

The file manish report card python.pdf is the comprehensive *Project Report Card* for this Complaint Management System. It contains:

  * *Detailed Introduction and Purpose*
  * *Problem Statement and Solution*
  * *Functional and Non-functional Requirements*
  * *System Architecture (3-Tier)*
  * *Design Diagrams (Use Case, Workflow, Sequence, Class, ER)*
  * *Implementation Details (Code snippets and rationale)*
  * *Testing Approach and Future Enhancements*

-----

## 💻 Project Overview

The application is built using the following technologies:

  * *Frontend GUI:* tkinter (Standard Python GUI library)
  * *Backend Database:* SQLite3 (Lightweight, serverless, file-based database)
  * *Language:* Python 3

### Core Features

1.  *Complaint Submission:* A user-friendly form to input name, gender, and the detailed complaint comment.
2.  *Data Persistence:* Stores all submitted complaints in an information.db file using SQLite.
3.  *View Records:* A separate window using a Treeview widget to display all stored complaints in a structured, tabular format.

## 🚀 Setup and Run

To run this application, you only need a standard Python 3 installation.

### 1\. Prerequisites

Ensure you have *Python 3* installed on your system. No external Python packages are strictly required as tkinter and sqlite3 are part of the standard library.

### 2\. Project Files

The project consists of the following key files:

| File Name | Description |
| :--- | :--- |
| main.py | The main application file. Initializes the Tkinter GUI, sets up the input form, and handles button commands (Submit Now, List Comp.). |
| db.py | The Data Access Layer. Contains the DBConnect class for managing the SQLite connection, creating the Comp table, and handling data Add and ListRequest operations. |
| listComp.py | The Display Layer. Contains the ListComp class, which creates a new window and populates a Treeview widget with all complaints retrieved from the database. |
| information.db | The SQLite database file where all complaint data is stored. (Automatically created if it doesn't exist). |

### 3\. Execution

1.  Make sure the three Python files (main.py, db.py, listComp.py) are in the same directory.

2.  Run the main application file from your terminal:

    bash
    python3 main.py
    

3.  The main application window will open, allowing you to submit a complaint or view the existing list.

## 🛑 How to Use

1.  *Submit a Complaint:*

      * Enter your *Full Name*.
      * Select your *Gender* (Male or Female).
      * Enter your detailed *Comment* in the text box.
      * Click the *Submit Now* button. A confirmation message box will appear, and the fields will clear.

2.  *View All Complaints:*

      * Click the *List Comp.* button on the main window.
      * A new window will open displaying the database records in a table (Treeview).

-----

## 🛠 Future Enhancements

As detailed in the project report, potential future enhancements include:

  * *CRUD Operations:* Implementing *Edit* and *Delete* functionality for existing complaints.
  * *Advanced Features:* Adding search, filtering, and sorting capabilities to the list view.
  * *Reporting:* Generating statistical reports or exporting data to formats like PDF/Excel.
  * *Scalability:* Migrating the database to a multi-user server (like PostgreSQL or MySQL) for enhanced scalability.
