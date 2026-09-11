# Python API & OOP Assignment
**MASAI X IIT Collaborative Training Program**

A comprehensive Python learning repository featuring Object-Oriented Programming (OOP) fundamentals and HTTP API interactions using the `requests` library.

## 📋 Project Overview

This repository contains a series of progressive exercises designed to build proficiency in:
- **Object-Oriented Programming (OOP)**: Classes, inheritance, polymorphism, encapsulation, composition
- **HTTP API Interactions**: GET, POST, PUT, DELETE operations with proper status code handling
- **Python Best Practices**: Error handling, validation, type hints, and clean code principles

## 🏗️ Project Structure

```
iitropar_masai_code/
├── README.md                           # This file
├── requirements.txt                    # Python dependencies
├── src/                                # Main exercise source code
│   ├── q01_oop_book_basics.py         # OOP: Basic class definition
│   ├── q02_oop_encapsulation.py       # OOP: Encapsulation with properties
│   ├── q03_oop_inheritance.py         # OOP: Inheritance and method overriding
│   ├── q04_oop_polymorphism.py        # OOP: Polymorphism with duck typing
│   ├── q05_oop_all_in_one.py          # OOP: Combined exercise with composition
│   ├── q06_requests_get.py            # API: Basic GET request
│   ├── q07_requests_get_params.py     # API: GET with query parameters
│   ├── q08_requests_post.py           # API: POST request with JSON body
│   ├── q09_requests_put_delete.py     # API: PUT and DELETE operations
│   ├── q10_http_status_classifier.py  # API: HTTP status code classification
│   ├── q11_fetch_with_status_handling.py # API: Fetch with error handling
│   └── q12_cli_http_client.py         # API: CLI HTTP client tool
├── tests/                              # Test suite
│   └── smoke_tests.py                 # Basic smoke tests for all exercises
└── notebooks/                          # Jupyter notebooks for reference
    ├── Masai_Master_IITRPR2409.ipynb
    ├── Masai_Python_Intro.ipynb
    ├── masai_iit_assignment.ipynb
    ├── masai_iit_example.ipynb
    ├── masai_iit_mab_revision.ipynb
    ├── masai_iit_mae.ipynb
    ├── masai_iit_python_fundamentals.ipynb
    ├── masai_iit_recommendation_system.ipynb
    ├── masai_iit_regression.ipynb
    ├── masai_iit_svm_classification.ipynb
    ├── nvdia_building_a_brain.ipynb
    └── iris.csv                        # Dataset for ML exercises
```

## 📚 Exercises

### Part 1: Object-Oriented Programming (OOP) - Exercises q01 to q05

#### q01_oop_book_basics.py - **Basic Class Definition**
**Concepts**: Class definition, constructors, instance methods, string representation
- Define a `Book` class with attributes: `title`, `author`, `price`
- Implement `get_details()` method that returns formatted book information
- Create and display multiple book instances
```bash
python src/q01_oop_book_basics.py
```

#### q02_oop_encapsulation.py - **Encapsulation & Properties**
**Concepts**: Private attributes, property decorators, getters/setters, validation
- Extend `Book` with a private `_discount` attribute (default=0.1)
- Implement `@property` getter and setter with validation (0.1 ≤ discount ≤ 0.9)
- Add `get_price_after_discount()` method
- Demonstrate property assignment and discounted price calculation
```bash
python src/q02_oop_encapsulation.py
```

#### q03_oop_inheritance.py - **Inheritance & Method Overriding**
**Concepts**: Subclassing, super() function, method overriding, inheritance chain
- Create `EBook(Book)` subclass with additional `file_size` (MB) attribute
- Override `get_details()` to include file size information
- Demonstrate inheritance and method overriding
```bash
python src/q03_oop_inheritance.py
```

#### q04_oop_polymorphism.py - **Polymorphism & Duck Typing**
**Concepts**: Duck typing, polymorphic methods, abstract interface behavior
- Implement `print_details(obj)` function that works with any object having `get_details()`
- Create a list containing both `Book` and `EBook` instances
- Iterate and print details using polymorphic behavior
```bash
python src/q04_oop_polymorphism.py
```

#### q05_oop_all_in_one.py - **Composition & Complete OOP Pattern**
**Concepts**: Composition, `@classmethod`, dunder methods (`__eq__`, `__len__`, `__iter__`, `__str__`, `__repr__`)
- `Price` class: value/currency validation, `__str__` and `__repr__`
- `Book` class: `__eq__` comparison, `from_dict()` classmethod
- `Inventory` class: composition pattern, `__len__`, `__iter__`, find by author
- Complete demonstration with multiple operations
```bash
python src/q05_oop_all_in_one.py
```

### Part 2: HTTP API Interactions - Exercises q06 to q12

All API exercises use [JSONPlaceholder](https://jsonplaceholder.typicode.com/) - a free fake JSON API for testing.

#### q06_requests_get.py - **Basic GET Request**
**Concepts**: GET requests, JSON parsing, response status codes
- Perform GET request to fetch a post
- Parse JSON response and extract specific fields
```bash
python src/q06_requests_get.py
```

#### q07_requests_get_params.py - **GET with Query Parameters**
**Concepts**: URL parameters, query strings, response arrays
- GET request with `postId` parameter
- Parse and display multiple comments with pretty JSON formatting
```bash
python src/q07_requests_get_params.py
```

#### q08_requests_post.py - **POST Request with JSON Body**
**Concepts**: POST requests, JSON payload, response validation
- POST request with JSON body containing title, body, and userId
- Capture auto-generated ID from fake API response
```bash
python src/q08_requests_post.py
```

#### q09_requests_put_delete.py - **PUT & DELETE Operations**
**Concepts**: PUT updates, DELETE operations, verification
- PUT request to update existing post
- DELETE request to remove post
- Verify deletion with subsequent GET
```bash
python src/q09_requests_put_delete.py
```

#### q10_http_status_classifier.py - **HTTP Status Code Classification**
**Concepts**: Status code ranges, categorization, error handling
- Classify status codes into categories:
  - `1xx`: Informational
  - `2xx`: Success
  - `3xx`: Redirection
  - `4xx`: Client Error
  - `5xx`: Server Error
```bash
python src/q10_http_status_classifier.py
```

#### q11_fetch_with_status_handling.py - **Fetch with Error Handling**
**Concepts**: Exception handling, retry logic, network errors, URL validation
- Implement `fetch_data(url)` with comprehensive error handling
- Handle `ConnectionError`, `Timeout`, and `RequestException`
- Validate URL format and retry logic (max 3 attempts)
- Test with valid, 404, 500, and invalid URLs
```bash
python src/q11_fetch_with_status_handling.py
```

#### q12_cli_http_client.py - **CLI HTTP Client Tool**
**Concepts**: Command-line interfaces, argument parsing, flexible HTTP client
- Build a CLI tool for making HTTP requests
- Support GET, POST, PUT, DELETE methods
- Accept optional JSON body for POST/PUT operations
- Pretty-print responses with headers and body

**Usage**:
```bash
# GET request
python src/q12_cli_http_client.py GET https://jsonplaceholder.typicode.com/posts/1

# POST request with JSON body
python src/q12_cli_http_client.py POST https://jsonplaceholder.typicode.com/posts '{"title":"Test","body":"Body","userId":1}'

# PUT request
python src/q12_cli_http_client.py PUT https://jsonplaceholder.typicode.com/posts/1 '{"title":"Updated"}'

# DELETE request
python src/q12_cli_http_client.py DELETE https://jsonplaceholder.typicode.com/posts/1
```

## 🔧 Installation & Setup

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Installation Steps

1. **Clone the repository**:
```bash
git clone https://github.com/iitropar/masai_code.git
cd iitropar_masai_code
```

2. **Create a virtual environment** (recommended):
```bash
# macOS/Linux
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
venv\Scripts\activate
```

3. **Install dependencies**:
```bash
pip install -r requirements.txt
```

### Dependencies
- **requests** (≥2.31.0): HTTP library for making web requests

## 🧪 Running Tests

### Smoke Tests
Run all exercises to verify they execute without import errors:
```bash
python tests/smoke_tests.py
```

The smoke test suite will:
- Execute all 12 exercises sequentially
- Capture output and errors
- Report any failures with detailed error messages
- Exit with status 0 (success) or 1 (failure)

### Individual Exercise Execution
Run any exercise individually:
```bash
python src/q01_oop_book_basics.py
python src/q06_requests_get.py
python src/q12_cli_http_client.py GET https://jsonplaceholder.typicode.com/posts/1
```

## 📔 Learning Path

### Recommended Order for Learning:
1. **q01**: Start with basic class definition
2. **q02**: Learn encapsulation with properties
3. **q03**: Understand inheritance
4. **q04**: Practice polymorphism
5. **q05**: Combine all OOP concepts

*Then transition to APIs:*

6. **q06**: Basic GET requests
7. **q07**: Add query parameters
8. **q08**: Learn POST operations
9. **q09**: Practice PUT/DELETE
10. **q10**: Understand status codes
11. **q11**: Add error handling
12. **q13**: Build a CLI tool

## 🎓 Key Concepts Covered

### OOP Fundamentals
| Concept | Exercise | Description |
|---------|----------|-------------|
| **Classes & Objects** | q01 | Basic class definition and instantiation |
| **Encapsulation** | q02 | Private attributes and property decorators |
| **Inheritance** | q03 | Subclassing and method overriding |
| **Polymorphism** | q04 | Duck typing and interface abstraction |
| **Composition** | q05 | Object composition and aggregation |
| **Dunder Methods** | q05 | `__str__`, `__repr__`, `__eq__`, `__len__`, `__iter__` |
| **Class Methods** | q05 | `@classmethod` for factory patterns |

### HTTP & API Fundamentals
| Concept | Exercise | Description |
|---------|----------|-------------|
| **HTTP Methods** | q06-q09 | GET, POST, PUT, DELETE operations |
| **Request Parameters** | q07 | Query strings and URL parameters |
| **JSON Payloads** | q08-q09 | Sending and receiving JSON data |
| **Status Codes** | q10 | Understanding HTTP response status |
| **Error Handling** | q11 | Exception handling and retries |
| **CLI Development** | q12 | Building command-line interfaces |

## 📚 Notebooks

The `notebooks/` directory contains Jupyter notebooks for supplementary learning:
- **Masai_Master_IITRPR2409.ipynb**: Master course materials
- **Masai_Python_Intro.ipynb**: Python fundamentals introduction
- **masai_iit_assignment.ipynb**: Assignment examples
- **masai_iit_python_fundamentals.ipynb**: Python fundamentals deep dive
- **masai_iit_svm_classification.ipynb**: SVM machine learning
- **masai_iit_regression.ipynb**: Regression analysis
- **masai_iit_recommendation_system.ipynb**: Recommendation system implementation
- **iris.csv**: Iris dataset for ML exercises

## 🐛 Troubleshooting

### Import Errors
- Ensure you've installed dependencies: `pip install -r requirements.txt`
- Check Python version: `python --version` (should be 3.7+)

### Network Errors in API Exercises
- Verify internet connection
- Check if JSONPlaceholder is accessible: `curl https://jsonplaceholder.typicode.com`
- API exercises include retry logic; they will attempt up to 3 times

### Status Code Issues
- Ensure URLs are valid and properly formatted
- Check that POST/PUT payloads contain valid JSON
- Review HTTP status code meanings in q10_http_status_classifier.py

## 🤝 Contributing

This is a learning repository. Improvements, bug fixes, and enhancements are welcome!

## 📝 License

This project is part of the MASAI X IIT collaborative training program.

## 👨‍🏫 Learning Outcomes

After completing all exercises, you will understand:
- ✅ How to design and implement classes with proper OOP principles
- ✅ How to make HTTP requests and handle responses
- ✅ How to build resilient APIs with error handling
- ✅ How to create CLI tools for interacting with APIs
- ✅ Best practices for Python code organization and style
