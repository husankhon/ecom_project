# Django E-Commerce Web Application

A full-featured e-commerce web platform built with Django, featuring user authentication with email verification, dynamic product catalog, session-based shopping cart, and order checkout management.

---

## 🚀 Features

- **Product Catalog (`myapp`)**: Browse products, view detailed product pages, image uploads, dynamic slugs, and stock status.
- **Shopping Cart (`cart`)**: Session-based cart with AJAX support to add, update, and remove items with real-time totals.
- **User Authentication (`users`)**:
  - User registration with email activation link verification
  - Login / Logout & Profile management
  - Password reset via email flow
- **Orders & Checkout (`orders`)**:
  - Shipping address management
  - Order creation and order items tracking
- **Django Admin**: Manage products, users, orders, and addresses with built-in admin dashboard.

---

## 🛠️ Tech Stack

- **Backend:** Python, Django
- **Database:** SQLite (default for development)
- **Image Processing:** Pillow
- **Frontend:** HTML5, CSS3, JavaScript (AJAX)

---

## 📦 Getting Started

### 1. Prerequisites
- Python 3.10+ installed
- Git

### 2. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 3. Create and Activate a Virtual Environment
- **macOS / Linux:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```
- **Windows (Command Prompt):**
  ```cmd
  python -m venv venv
  venv\Scripts\activate
  ```
- **Windows (PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\Activate.ps1
  ```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Apply Migrations
```bash
python manage.py migrate
```

### 6. Create a Superuser (Admin)
```bash
python manage.py createsuperuser
```

### 7. Run the Development Server
```bash
python manage.py runserver
```

Open your browser and navigate to `http://127.0.0.1:8000/`.

To access the admin panel, go to `http://127.0.0.1:8000/admin/`.

---

## 📁 Project Structure

```text
├── cart/               # Shopping cart app (sessions, views, context processors)
├── myapp/              # Product catalog and store views
├── orders/             # Order processing, address handling, and checkout
├── users/              # Authentication, registration, and email tokens
├── media/              # Uploaded product images
├── mysite/             # Project settings, routing, and WSGI/ASGI configs
├── manage.py           # Django management utility
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

---

## ⚠️ Important Note Before Pushing to GitHub

Make sure not to commit sensitive credentials (such as your `SECRET_KEY` and email SMTP passwords) directly to GitHub. Consider using environment variables (e.g., via `python-decouple` or `python-dotenv`) in `mysite/settings.py` for sensitive credentials.
