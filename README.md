# 📚 Student Result Management System

A modern, user-friendly web application for managing student examination results with automatic grade calculation and persistent data storage.

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![Flask](https://img.shields.io/badge/Flask-3.0+-green?style=flat-square&logo=flask)
![SQLite](https://img.shields.io/badge/SQLite-Lightweight-orange?style=flat-square&logo=sqlite)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 🎯 Features

- ✅ **Easy Result Entry** - Simple form-based interface for entering student marks
- 🧮 **Automatic Grade Calculation** - Calculates total, percentage, and grade instantly
- 💾 **Data Persistence** - All results stored securely in SQLite database
- 📊 **Grade System** - Intelligent grading based on percentage scoring
- 🎨 **Responsive Design** - Clean and modern UI with CSS styling
- ✔️ **Unit Tests** - Comprehensive test suite included
- ⚡ **Real-time Processing** - Instant result calculation and display

---

## 🛠️ Tech Stack

| Component             | Technology   |
| --------------------- | ------------ |
| **Backend Framework** | Flask 3.0.3  |
| **Database**          | SQLite 3     |
| **Frontend**          | HTML5 & CSS3 |
| **Testing**           | Pytest 8.2.0 |
| **Language**          | Python 3.8+  |

---

## 📋 Grade Calculation System

The system automatically assigns grades based on the following criteria:

| Percentage Range | Grade  |
| ---------------- | ------ |
| ≥ 90%            | **A+** |
| 75 - 89%         | **A**  |
| 60 - 74%         | **B**  |
| 40 - 59%         | **C**  |
| < 40%            | **F**  |

> **Note:** Percentage is calculated as the average of three exam marks.

---

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone or download the project**

   ```bash
   cd student-result-management-fresh
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**

   ```bash
   python app.py
   ```

4. **Access the application**
   - Open your browser and navigate to: `http://localhost:5000`

---

## 📖 Usage

### Submitting a Result

1. Fill in the student's **name** and **roll number**
2. Enter marks for **three exams** (out of 100)
3. Click the **Submit** button
4. View the calculated results including:
   - Total marks
   - Percentage
   - Final grade

### Example

```
Student Name: John Doe
Roll Number: 101
Exam 1: 85
Exam 2: 90
Exam 3: 78

Result:
Total: 253
Percentage: 84.33%
Grade: A
```

---

## 📁 Project Structure

```
student-result-management-fresh/
├── app.py                    # Main Flask application
├── database.py               # Database operations & queries
├── requirements.txt          # Project dependencies
├── README.md                 # This file
├── static/
│   └── style.css            # Application styling
├── templates/
│   ├── index.html           # Result entry form
│   └── result.html          # Results display page
└── tests/
    └── test_app.py          # Unit tests
```

### File Descriptions

| File                    | Purpose                                               |
| ----------------------- | ----------------------------------------------------- |
| `app.py`                | Main Flask application with routes and business logic |
| `database.py`           | SQLite database initialization and CRUD operations    |
| `static/style.css`      | Responsive styling for web interface                  |
| `templates/index.html`  | Student information & marks input form                |
| `templates/result.html` | Displays calculated results                           |
| `tests/test_app.py`     | Automated tests for core functionality                |

---

## 🧪 Testing

Run the automated test suite using pytest:

```bash
pytest tests/test_app.py -v
```

This will execute all unit tests and display detailed results.

---

## 🔧 API Endpoints

### GET `/`

- **Description:** Displays the result entry form
- **Response:** HTML form page

### POST `/submit`

- **Description:** Processes student result submission
- **Parameters:**
  - `name` (string): Student name
  - `roll_no` (string): Student roll number
  - `marks1` (integer): First exam marks
  - `marks2` (integer): Second exam marks
  - `marks3` (integer): Third exam marks
- **Response:** Displays calculated results

---

## 📊 Database Schema

### Results Table

```sql
CREATE TABLE results (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    roll_no TEXT NOT NULL,
    marks1 INTEGER NOT NULL,
    marks2 INTEGER NOT NULL,
    marks3 INTEGER NOT NULL,
    total INTEGER NOT NULL,
    percentage REAL NOT NULL,
    grade TEXT NOT NULL
)
```

---

## 💡 Key Features Explained

### 1. **Automatic Grading**

- Intelligent algorithm assigns grades based on percentage
- Standardized grading scale

### 2. **Data Storage**

- All results persisted in SQLite database
- Lightweight, file-based database (no external setup needed)

### 3. **User Experience**

- Simple, intuitive interface
- Instant result calculation
- Professional styling

---

## 🐛 Troubleshooting

| Issue                      | Solution                               |
| -------------------------- | -------------------------------------- |
| Port 5000 already in use   | Modify `app.run(port=5001)` in app.py  |
| Dependencies not installed | Run `pip install -r requirements.txt`  |
| Database file missing      | Delete `results.db` and re-run the app |

---

## 🎓 Future Enhancements

- [ ] User authentication & login system
- [ ] Admin dashboard with result analytics
- [ ] Bulk result import (CSV/Excel)
- [ ] Result export functionality
- [ ] Email notifications
- [ ] Advanced filtering and search
- [ ] Mobile app version

---

## 📝 License

This project is licensed under the MIT License - feel free to use it for educational and commercial purposes.

---

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and enhancement requests.

---

## 📧 Support

For questions or issues, please create an issue in the project repository.

---

<div align="center">

**Made with ❤️ for better student result management**

Happy Coding! 🚀

</div>
