# 💸 Expense Tracking System

A simple yet powerful expense tracking and budget management system built with **FastAPI** and **MySQL**. This system allows users to track daily expenses, manage monthly budgets, and analyze spending patterns across categories.

---

## 🚀 Features

- ✅ Add, update, and view expenses by date or date range
- 📊 Visualize spending analytics (category-wise)
- 💰 Set and manage monthly budgets
- 📈 Get budget status (Within Budget / Approaching / Over Budget)
- 🧪 Unit testing support for backend and frontend
- 📁 Clean modular codebase (API, DB, UI logic, logging)

---

## 🛠️ Tech Stack

- **Backend**: FastAPI
- **Database**: MySQL
- **Logging**: Python `logging`
- **Dependencies**: `fastapi`, `uvicorn`, `mysql-connector-python`, `pydantic`, `pytest`

---

## 📂 Project Structure
The project is organized into backend, frontend, and tests components:
```plaintext
Project_expense_tracking/
├── backend/
│ ├── server.py # FastAPI app entry point
│ ├── db_helper.py # DB functions to add, fetch, filter expenses
│ ├── logging_setup.py # Centralized logging config
│
├── frontend/
│ ├── app.py # UI launch logic
│ ├── add_update.py # UI for adding/updating expenses
│ ├── analytics_by_category.py # UI for showing analytics by category
│ ├── analytics_by_months.py # UI for showing analytics by category
│
├── tests/
│ ├── backend/
│ │ ├── test_db_helper.py # Unit tests for db_helper functions
│ ├── frontend/
│ │ ├── conftest.py # Fixtures for frontend testing       
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/project_expense_tracker.git
cd project_expense_tracker
```

### 2. Install dependencies

If you have a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

If not, install manually:

```bash
pip install fastapi uvicorn mysql-connector-python pydantic pytest
```

### 3. Configure MySQL Database

Update your credentials in `backend/db_helper.py`:

```python
DB_CONFIG = {
    "host": "localhost",
    "user": "your_user",
    "password": "your_password",
    "database": "expense_manager"
}
```

Then, create the database manually in MySQL:

```sql
CREATE DATABASE expense_manager;
```

### 4. Run the FastAPI Server

```bash
uvicorn backend.server:app --reload
```

API will be live at: [http://127.0.0.1:8000](http://127.0.0.1:8000)

Access interactive API docs at: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)


### 5. Run the Streamlit Frontend

From the project root:

```bash
streamlit run ./app.py
```
---

## ✅ Testing

To run unit tests (if implemented):

```bash
pytest
```
## Usage
### ✏️ Add/Update Expenses

- Navigate to the **"Add/Update"** tab.
- Select a date and enter expense details:
  - Amount
  - Category
  - Notes
- Click **Save** to add new expenses or update existing ones.

### 📈 View Analytics By Category

- Go to the **"Analytics By Category"** tab.
- Select a date range and click **"Get Analytics"**.
- View:
  - A bar chart of spending by category
  - A table summarizing expenses
  
### 📈 View Analytics By Month

- Go to the **"Analytics By Month"** tab.
- Select a date range and click **"Get Analytics"**.
- View:
  - A bar chart of spending by month
  - A table summarizing expenses




---



## 🧑‍💻 Author

Made by Rehan Khan

---


