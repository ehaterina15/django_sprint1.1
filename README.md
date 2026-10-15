# Blogicum v1

**The first iteration of Blogicum, a blogging site built with Django.** This version has no database: posts are stored in a Python list and rendered through Django's URL routing, views and template inheritance.

![Python](https://img.shields.io/badge/Python-3.9-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-3.2-092E20?logo=django&logoColor=white)
![pytest](https://img.shields.io/badge/tests-pytest-0A9EDC?logo=pytest&logoColor=white)

## What it shows

- A Django project split into two apps: `blog` (posts) and `pages` (static pages)
- Namespaced URLs with path converters: `posts/<int:id>/`, `category/<slug:category_slug>/`
- Function-based views, plus `TemplateView` for the static pages
- A template hierarchy (`base.html` + `includes/` for the header, footer and post list)
- A 404 response for posts that don't exist

## Pages

| URL | Page |
|---|---|
| `/` | Feed with all posts |
| `/posts/<id>/` | Single post |
| `/category/<slug>/` | Posts in a category |
| `/pages/about/` | About the project |
| `/pages/rules/` | Site rules |

## Run it

```bash
git clone https://github.com/ehaterina15/django_sprint1.1.git
cd django_sprint1.1
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
cd blogicum
python manage.py runserver
```

Run the tests from the repository root with `pytest`.

## Context

Sprint 1 of the Django module at [Yandex Practicum](https://practicum.yandex.com/). The finished, database-backed version of the project is in [django_sprint4](https://github.com/ehaterina15/django_sprint4).

## Author

**Ekaterina Mashentseva** · [GitHub](https://github.com/ehaterina15)
