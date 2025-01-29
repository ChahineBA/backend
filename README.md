# FastAPI User Management API

## 📌 Overview

This FastAPI-based API provides authentication and user management functionalities, including user registration, login, fetching user details, and deleting users from a MongoDB database.

---

## 📂 Project Structure

```
/project_root
│── main.py            # Main FastAPI application
│── auth.py            # Authentication functions (login, register)
│── dash.py            # Dashboard utilities (fetching users, stats)
│── .env               # Environment variables
│── requirements.txt   # Dependencies list
│── README.md          # Documentation
```

---

## ⚙️ Setup & Installation

### 1️⃣ Prerequisites

- Python 3.8+
- MongoDB instance (local or cloud)
- Virtual environment (recommended)

### 2️⃣ Clone the Repository

```sh
git clone https://github.com/yourusername/yourproject.git
cd yourproject
```

### 3️⃣ Create and Activate a Virtual Environment

```sh
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate     # On Windows
```

### 4️⃣ Install Dependencies

```sh
pip install -r requirements.txt
```

### 5️⃣ Configure Environment Variables

Create a `.env` file in the root directory and add:

```ini
MONGO_URI=mongodb+srv://your_mongo_uri
MONGO_DB=your_database_name
MONGO_COLLECTION=your_collection_name
```

### 6️⃣ Run the API

```sh
uvicorn main:app --reload
```

The API will be available at:
📍 `http://127.0.0.1:8000`

---

## 🚀 API Endpoints

### 🔐 Authentication

| Method | Endpoint    | Description       |
| ------ | ----------- | ----------------- |
| `POST` | `/login`    | User login        |
| `POST` | `/register` | User registration |

### 👥 User Management

| Method   | Endpoint           | Description           |
| -------- | ------------------ | --------------------- |
| `GET`    | `/users`           | Fetch all users       |
| `GET`    | `/users/total`     | Get total users count |
| `GET`    | `/users/new`       | Get new users count   |
| `DELETE` | `/users/{user_id}` | Delete user by ID     |

---

## 🛠️ Dependencies

- FastAPI
- Uvicorn
- Pydantic
- PyMongo
- Python-Dotenv

To install all dependencies:

```sh
pip install -r requirements.txt
```

---

## 🔹 Future Enhancements

✅ Add JWT authentication  
✅ Implement role-based access control  
✅ Improve error handling

---

## 📄 License

This project is licensed under the MIT License.
