
# 📝 Personal Blog Website (Django)

## 📌 Loyiha haqida

Ushbu loyiha **Django framework** yordamida yaratilgan **shaxsiy blog web sayt** hisoblanadi. Sayt orqali men o‘zim haqimda ma’lumot beraman va blog postlar joylayman. Loyihada **backend (Django)** va **frontend (HTML, CSS)** alohida tartibda tashkil qilingan.

---

## 🎯 Loyihaning maqsadi

* Django’da to‘liq ishlaydigan blog web site yaratish
* Backend va frontendni to‘g‘ri struktura bilan ajratish
* `templates` papkasi orqali frontend kodlarni boshqarish
* Blog postlar qo‘shish, ko‘rish va boshqarish

---

## ⚙️ Ishlatilgan texnologiyalar

* **Python 3**
* **Django**
* **HTML5**
* **CSS3**

* **PostgreSQL** (database)

---

## 📂 Loyiha strukturasi

```bash
blog_project/
│
├── config/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── blog/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── about.html
│   └── blog_detail.html
│
├── static/
│   ├── css/
│   └── images/
│
├──.env.example
├── manage.py
└── README.md
```

---

## 🧩 Asosiy sahifalar

* **Home** – Blog postlar ro‘yxati
* **About Me** – O‘zim haqimda ma’lumot
* **Blog Detail** – Har bir postning alohida sahifasi
* **Admin Panel** – Postlarni qo‘shish va tahrirlash

---

## 🗃️ Model (misol)

```python
from django.db import models

class Blog(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    created_at = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

---

## ▶️ Loyihani ishga tushirish

1. Virtual environment yaratish:

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

2. Django o‘rnatish:

```bash
pip install django
```

3. Migratsiya qilish:

```bash
python manage.py makemigrations
python manage.py migrate
```

4. Superuser yaratish:

```bash
python manage.py createsuperuser
```

5. Serverni ishga tushirish:

```bash
python manage.py runserver
```

Brauzerda ochish:

```
http://127.0.0.1:8000/
```

Admin panel:

```
http://127.0.0.1:8000/admin/
```

---

## 🎨 Templates haqida

Frontend kodlar **`templates/`** papkasida joylashgan.
Har bir HTML fayl Django template syntax’dan foydalanadi:

```html
{% extends 'base.html' %}
{% block content %}
<h1>Mening blogimga xush kelibsiz</h1>
{% endblock %}
```

---

## ✅ Xulosa

Ushbu loyiha Django’da **to‘g‘ri struktura**, **templates papkasi**, va **oddiy blog funksionallik** asosida qurilgan. Vazifa yoki portfolio uchun juda qulay.

---
