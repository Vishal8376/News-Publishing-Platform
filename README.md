---
# 📰 News Publishing Platform

A Django-based web platform that allows editors to create, update, delete, and publish news articles. The public frontend displays a list of published articles, while authenticated admins (staff users) can manage articles using form-based views.

---

## 📌 Features

- 📝 Create, Read, Update, Delete (CRUD) operations for news articles
- ✅ Publish/unpublish toggle for each article
- 📅 Automatic or manual publish date
- 🔒 Admin-only access for content management
- 🌐 Frontend displays all published articles in reverse chronological order

---

## 🚀 Tech Stack

- **Backend:** Django (Python)
- **Frontend:** HTML templates (Django Templating Engine)
- **Database:** SQLite (default with Django)
- **Authentication:** Django admin for editor access control

---

## 🔧 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/news-publishing-platform.git
   cd news-publishing-platform
```
```
2. **Create Virtual Environment**

   ```
   python -m venv venv
   source venv/bin/activate    # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install django
   ```

4. **Run Migrations**

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create Superuser (Admin)**

   ```bash
   python manage.py createsuperuser
   ```

6. **Start the Development Server**

   ```bash
   python manage.py runserver
   ```

7. **Visit in Browser**

   * Admin Panel: `http://127.0.0.1:8000/admin/`
   * Public News Feed: `http://127.0.0.1:8000/`

---

## 📂 Project Structure

```
newsportal/
│
├── newsportal/             
│   └── settings.py
│
├── news/                   
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── forms.py
│   └── templates/news/
│       ├── home.html
│       ├── form.html
│       └── confirm_delete.html
│
├── db.sqlite3              
└── manage.py
```

---

## 🧑‍💼 Admin Panel

To manage articles (create/update/delete), log in to the Django admin panel using the superuser credentials:

```plaintext
http://127.0.0.1:8000/admin/
```

Make sure the logged-in user is marked as `staff` in the admin panel.

---

## ✅ Usage Workflow

1. **Admin logs in**
2. **Creates an article** using the form at `/create/`
3. **Marks the article as published**
4. Article becomes visible on the public homepage (`/`)
5. Admin can update or delete it via `/update/<id>/` or `/delete/<id>/`

---

## 🔒 Authentication Rules

* Only staff users can create/update/delete articles.
* Anyone can view the list of published articles.

---

## 🛠 Future Improvements

* Add user roles (Editor, Writer)
* REST API with DRF (Django Rest Framework)
* React frontend with article search
* Pagination and category filtering
* Media/image uploads for news

---
