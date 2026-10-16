🔍 Inverted Search
A menu-driven Inverted Search Engine developed in C using Hash Tables, Linked Lists, and File Handling. The project indexes words from multiple text files and enables fast keyword-based searching by maintaining an inverted index.

📖 Overview
Searching through multiple text files sequentially is inefficient as the number of files grows. This project implements an Inverted Search mechanism that preprocesses the files and builds an index for quick retrieval.

Each unique word is mapped to:

The files in which it appears.
The number of occurrences in each file.
The project demonstrates the practical application of Data Structures and File Handling concepts in C.

✨ Features
✅ Create database from multiple text files
✅ Display the complete inverted database
✅ Search for a word efficiently
✅ Update the database by adding new files
✅ Save the database to a file
✅ Validate input files before processing
✅ Detect duplicate files
✅ Handle empty files
✅ Validate file extensions
✅ Collision handling using linked lists
✅ Modular implementation with separate source files
🛠 Technologies Used
Language: C
Data Structures:
Hash Table
Singly Linked List
Concepts:
Dynamic Memory Allocation
File Handling
String Manipulation
Modular Programming
Build Tool:
Makefile
📂 Project Structure
.
├── main.c
├── validation.c
├── create_database.c
├── create_file_list.c
├── search_database.c
├── display_database.c
├── save_database.c
├── update_database.c
├── inverted.h
├── Makefile
├── sample text files
└── README.md
⚙️ Working Principle
The project creates an inverted index using 27 hash buckets.

Buckets 0–25 represent the letters a–z
Bucket 26 stores words beginning with digits or special characters
Each bucket points to a linked list of Main Nodes.

Each Main Node stores:

File Count
Word
Pointer to Sub Node List
Pointer to next Main Node
Each Sub Node stores:

Word Count
File Name
Pointer to Next File
Hash Table
    |
    +---- Bucket[0]
    |         |
    |         +---- Word: apple
    |                    |
    |                    +---- file1.txt (5)
    |                    |
    |                    +---- file3.txt (2)
    |
    +---- Bucket[1]
    |
    +---- ...
🚀 How to Build
Run

./inverted_search file1.txt file2.txt file3.txt
📋 Menu
1. Create Database
2. Display Database
3. Search Database
4. Save Database
5. Update Database
6. Exit
✅ File Validation
Before creating the database, the project validates every input file by checking:

Valid .txt extension
File existence
Empty files
Duplicate files
Only valid files are inserted into the file list and indexed.

🔎 Search Operation
When the user searches for a word:

The hash index is calculated.
The corresponding bucket is accessed.
The linked list is traversed.
Matching word details are displayed, including:
File names
Number of occurrences
This provides efficient lookup compared to searching every file individually.

💾 Save Database
The complete inverted database can be saved into a text file, allowing the indexed data to be reused without rebuilding the database.

🔄 Update Database
New text files can be added after the database has already been created.

The project validates the new file, checks for duplicates, updates the file list, and indexes only the newly added file without rebuilding the existing database.

📷 Output Screenshots
Validation & Database Creation
Validation

Display Database
Display Database

Search Word
Search

Update Database
Update

Save Database
Save

📚 Concepts Demonstrated
Hash Tables
Linked Lists
File Handling
Dynamic Memory Allocation
String Handling
Data Indexing
Searching Algorithms
Collision Handling
Modular Programming
🎯 Learning Outcomes
This project strengthened my understanding of:

Designing real-world applications using Data Structures
Implementing hash-based indexing
Efficient searching techniques
File processing in C
Dynamic memory management
Writing modular and maintainable C programs
