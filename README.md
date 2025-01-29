# Library Management System

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
   - [Data Initialization](#1-data-initialization)
   - [Book Management](#2-book-management)
   - [Borrowing and Returning Books](#3-borrowing-and-returning-books)
   - [Search and Filter Features](#4-search-and-filter-features)
   - [Advanced Features](#5-advanced-features)
   - [Statistics Using NumPy](#6-statistics-using-numpy)
   - [Interactive Console Interface](#7-interactive-console-interface)
   - [File Handling](#8-file-handling)
3. [Technologies Used](#technologies-used)
4. [Examples](#examples)
5. [How to Run the System](#how-to-run-the-system)
6. [Future Enhancements](#future-enhancements)
7. [Conclusion](#conclusion)

## Overview

The Library Management System is a Python-based application designed to efficiently manage a library's book inventory and user interactions. It incorporates key programming concepts such as file handling, functions, loops, and data structures while leveraging libraries like Pandas, NumPy, and Matplotlib for data processing and visualization.

Link of the colaboratory notebook: [Library Management System](https://colab.research.google.com/drive/1ksD-zwPKYAaz0PZF-4EdjjWv7oS59xBT?usp=sharing)

## Features

### 1. Data Initialization

- Loads initial book inventory from a CSV file.
- Fields include: Book ID, Title, Author, Genre, Availability, and Borrower.
- Uses Pandas to manage and manipulate the dataset.

### 2. Book Management

- **Add a Book:** Allows librarians to add new books with details like ID, Title, Author, and Genre.
- **Remove a Book:** Deletes a book from the inventory based on its ID.
- **Update Book Details:** Modifies book information, including availability and borrower details.

### 3. Borrowing and Returning Books

- **Borrow a Book:**
  - Checks if the book is available.
  - Updates borrower details and marks the book as unavailable.
- **Return a Book:**
  - Marks the book as available.
  - Clears the borrower information.

### 4. Search and Filter Features

- **Search Books:**
  - Allows searching by Title, Author, or Genre using Boolean indexing.
- **Filter Books:**
  - Shows only available books.
  - Lists books borrowed by a specific user.

### 5. Advanced Features

- **Exception Handling:**
  - Ensures robustness by handling invalid inputs and missing book IDs gracefully.
- **Regular Expressions (RegEx):**
  - Validates book IDs (e.g., format: BK-001).
- **Data Visualization:**
  - Bar chart representing the number of books per genre.
  - Pie chart showing book availability status.

### 6. Statistics Using NumPy

- **Total Books Count:** Calculates the total number of books in the library.
- **Most Borrowed Genre:** Identifies the most borrowed book genre.
- **Borrowing Trends Analysis:** Determines average borrowing duration and other trends.

### 7. Interactive Console Interface

- Provides a menu-driven interface allowing users to:
  - View books
  - Add, remove, or update books
  - Borrow or return books
  - Search and filter books
  - View statistics and generate visualizations

### 8. File Handling

- Saves all modifications to the CSV file after each operation.
- Allows exporting filtered or searched data to a new CSV file.

## Technologies Used

- **Python** (Primary Language)
- **Pandas** (Data Handling & Manipulation)
- **NumPy** (Statistical Analysis)
- **Matplotlib** (Data Visualization)
- **Regular Expressions** (Input Validation)

## Examples

### Example: Borrowing a Book

```python
borrow_book("BK-002", "Alice")
```

- If the book is available, it will be marked as borrowed by Alice.
- If the book is unavailable, an appropriate message will be displayed.

### Example: Searching for a Book by Title

```python
search_books(title="Python Programming")
```

- Displays all books matching the title "Python Programming".

### Example: Viewing Books by Availability

```python
filter_books(available=True)
```

- Lists all books that are currently available in the library.

## How to Run the System

1. Install the required dependencies:
   ```bash
   pip install pandas numpy matplotlib
   ```
2. Upload the dataset (`11_Library_Management_System.csv`) to the working directory.
3. Run the Python script in Google Colab or a local Python environment:
   ```bash
   python library_management.py
   ```
4. Follow the menu prompts to interact with the system.
