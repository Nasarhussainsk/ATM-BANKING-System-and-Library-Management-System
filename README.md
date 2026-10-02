# ATM-BANKING-System-and-Library-Management-System
Python OOP concepts with real-world examples.

# Python OOP Concepts

This project demonstrates the core concepts of **Object-Oriented Programming (OOP) in Python** through practical examples of a **Banking System** and a **Library Management System**.

## 📌 Project Overview

The notebook demonstrates how Python classes, objects, inheritance, abstraction, encapsulation, and method overriding can be used to build simple real-world applications.

The project contains two main examples:

1. **Banking System**
2. **Library Management System**

---

## 🛠️ Concepts Covered

### 1. Classes and Objects

Classes are used as blueprints for creating objects.

Examples:

* `Secureuser`
* `SavingsAccount`
* `CurrentAccount`
* `LibraryUser`
* `StudentUser`
* `TeacherUser`

Objects are created from these classes to perform different operations.

---

### 2. Abstraction

The `ABC` and `abstractmethod` features from Python's `abc` module are used to create abstract classes.

For example:

```python
class Secureuser(ABC):
```

The methods `deposit_cash()` and `withdraw_cash()` are defined as abstract methods.

Similarly, `LibraryUser` defines abstract methods for:

* `borrow_book()`
* `return_book()`

Child classes provide their own implementations of these methods.

---

### 3. Encapsulation

Encapsulation is demonstrated by restricting direct access to sensitive attributes.

For example:

```python
self.__atm_pin = atm_pin
```

and:

```python
self.__user_id = user_id
```

The double underscore (`__`) makes these attributes private.

Protected attributes are also used:

```python
self._balance = 0
self._borrowed_books = []
```

---

### 4. Inheritance

Child classes inherit properties and methods from parent classes.

#### Banking System

```text
Secureuser
├── SavingsAccount
└── CurrentAccount
```

#### Library System

```text
LibraryUser
├── StudentUser
└── TeacherUser
```

---

### 5. Polymorphism / Method Overriding

Different child classes implement the same method in their own way.

For example, both `StudentUser` and `TeacherUser` have:

```python
borrow_book()
return_book()
```

However, the borrowing limits are different:

* Students can borrow up to **3 books**
* Teachers can borrow up to **5 books**

This demonstrates polymorphic behavior through method overriding.

---

## 🏦 Banking System

The banking example contains:

### `Secureuser`

The base class manages:

* User name
* ATM PIN
* Account balance
* PIN verification
* Account balance display

The user gets **3 attempts** to enter the correct PIN. After unsuccessful attempts, access is denied.

### `SavingsAccount`

Provides:

* Cash deposit
* Cash withdrawal
* Balance checking

### `CurrentAccount`

Provides:

* Cash deposit
* Cash withdrawal
* Balance checking

The notebook also demonstrates creating objects and performing transactions.

Example:

```python
savings = SavingsAccount("john", 1234)
current = CurrentAccount("rio", 5678)
```

---

## 📚 Library Management System

The library example contains:

### `LibraryUser`

The base class manages:

* User name
* User ID
* Borrowed books
* User ID verification
* Viewing borrowed books

### `StudentUser`

Students can borrow a maximum of **3 books**.

### `TeacherUser`

Teachers can borrow a maximum of **5 books**.

Both classes can:

* Borrow books
* Return books
* View borrowed books

The notebook also demonstrates what happens when a user reaches their borrowing limit.

---

## 💻 Technologies Used

* **Python 3**
* Python `abc` module
* Object-Oriented Programming concepts
* Jupyter Notebook

---
## 🔗 GitHub Repository

[View the project on GitHub]
(https://github.com/Nasarhussainsk/ATM-BANKING-System-and-Library-Management-System)

---

## ▶️ How to Run

1. Install Python.
2. Install Jupyter Notebook or use JupyterLab.
3. Open `OOPS_CONCEPT.ipynb`.
4. Run the cells sequentially.
5. When prompted, enter the required ATM PIN or User ID.

---

## 🎯 Learning Objectives

After completing this notebook, you should understand:

* How to create classes and objects
* How constructors work
* How inheritance works
* How abstraction is implemented
* How encapsulation protects data
* How method overriding demonstrates polymorphism
* How OOP concepts can be applied to real-world problems

---

## 📁 Project Structure

```text
OOPS_CONCEPT.ipynb
README.md
```

---

## 👨‍💻 Project Summary

This project provides a practical introduction to **Object-Oriented Programming in Python** by implementing banking and library management scenarios. It demonstrates how OOP principles can be combined to create structured and reusable Python programs.
