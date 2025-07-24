

## Project Goals

- Set up a Django project & app  
- Create a model with constraints  
- Use Django REST Framework for API development  
- Perform CRUD operations  
- Test APIs with Postman  
- Use version control with `.gitignore` and virtual environments  

---

## PROJECT 

```
TASK3,4_TMRC/
│
├── myproject/              # Main Django project
│   └── settings.py         # Project settings
│
├── myapp/                  # Django app (API logic)
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── serializers.py
│
├── db.sqlite3              # SQLite3 database (default)
├── manage.py               # Django command-line utility
├── requirements.txt        # Dependencies
└── .gitignore              # Ignored files
```

---



### Set Up Virtual Environment

```bash
python -m venv venv
```

Then activate it:

- **Windows:** `venv\Scripts\activate`  
- **Mac/Linux:** `source venv/bin/activate`

---

### Install Requirements

```bash
pip install -r requirements.txt
```

---

###  Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

### Run Server

```bash
python manage.py runserver
```

Visit in browser: [http://127.0.0.1:8000/api/products/](http://127.0.0.1:8000/api/products/)

---

### 6️⃣ Access Admin Panel (Optional)

1. Create admin user:

```bash
python manage.py createsuperuser
```

2. Visit: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

---

## API Endpoints (Test with Postman)

| Method   | Endpoint              | Description                |
| -------- | --------------------- | -------------------------- |
| `GET`    | `/api/products/`      | Retrieve all products      |
| `POST`   | `/api/products/`      | Create a new product       |
| `GET`    | `/api/products/<id>/` | Retrieve a product by ID   |
| `PUT`    | `/api/products/<id>/` | Fully update a product     |
| `PATCH`  | `/api/products/<id>/` | Partially update a product |
| `DELETE` | `/api/products/<id>/` | Delete a product           |


---

##  Technologies used

- Python 3.x  
- Django  
- Django REST Framework  
- SQLite3 (default DB)

---

## Concepts

- **Virtual Environment**: Keeps project dependencies isolated  
- **`.gitignore`**: Prevents uploading unnecessary files (e.g., `venv/`, `.pyc`, `db.sqlite3`)  
- **Serializers**: Convert model data to JSON & validate input  
- **PUT vs PATCH**:  
  - `PUT` = Replace entire record  
  - `PATCH` = Update only specific fields  


