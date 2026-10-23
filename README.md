# Python Salary Tracker

A Object-Oriented Programming (OOP) project built as part of the **freeCodeCamp** Python certification curriculum. This application models an employee management system that dynamically tracks salary ranges, enforces promotion rules, and validates data integrity using Python properties and custom setters.

---

## Key Features

- **Class-Based Architecture:** Models employees using standard Python OOP concepts (`__init__`, `__str__`, `__repr__`).
- **Encapsulation & Validation:** Uses `@property` decorators and custom setters to control access and validate input types (`name`, `level`, `salary`).
- **Dynamic Salary Management:**
  - Base salary automatically updates upon employee level changes (`trainee`, `junior`, `mid-level`, `senior`).
  - Strict business logic checks prevent downgrading levels or setting salaries below the baseline for a specific level.
- **Robust Error Handling:** Explicitly raises `TypeError` and `ValueError` with descriptive messages for invalid assignments.

---

## Concepts & Technologies Applied

- **Python 3**
- **Object-Oriented Programming (OOP)**
- **Decorators:** `@property`, `@<attribute>.setter`
- **Error & Exception Handling** (`TypeError`, `ValueError`)
- **Data Structures:** Dictionaries and Class Attributes

---

## Usage Example

```python
# Create a new employee
charlie_brown = Employee('Charlie Brown', 'trainee')
# Output: 'name' updated to 'Charlie Brown'.
# Output: Salary updated to $1000.

print(charlie_brown)
# Output: Charlie Brown: trainee

print(f'Base salary: ${charlie_brown.salary}')
# Output: Base salary: $1000

# Promote the employee
charlie_brown.level = 'junior'
# Output: 'name' promoted to 'junior'.
# Output: Salary updated to $2000.
