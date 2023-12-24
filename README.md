# Payments
Тествое задание
***
## Stack
### Backend
    Python
    DRF
    Django
    Docker
### Frontend
    HTML
    CSS
### Web-server
    Nginx
### WSGI-server
    Gunicorn
***
## Repository content
    
- ./requirements.txt - a set of modules required for the application
- ./DjangoService/ - Django app 
- ./DjangoProject/ - source directory
- ./manage.py - application startup script

***
## Startup Examples
### Windows
#### Step 0
##### Клонируйте репозиторий.
```bash
git clone https://github.com/HySuren/Restoran_SYSTEM.git
```
#### Step 1
##### Измените STRIPE_PUBLIC_KEY и STRIPE_SECRET_KEY на ваш(dockerfile).
```bash
...

# Set Django environment variables
ENV DJANGO_SECRET_KEY=your_secret_key
ENV DEBUG=True
ENV ALLOWED_HOSTS=localhost,127.0.0.1
# Ваш публичный ключ от STRIPE
ENV STRIPE_PUBLIC_KEY=...
# Ваш приватный ключ от STRIPE
ENV STRIPE_SECRET_KEY=...

...
```
#### Step 2
##### Измените STRIPE_PUBLIC_KEY и STRIPE_SECRET_KEY на ваш(.env).
```bash
DJANGO_SECRET_KEY=your_secret_key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
STRIPE_PUBLIC_KEY=...
STRIPE_SECRET_KEY=...
```
#### Step 3
```bash
docker build -t название вашего image .     
```
#### Step 4
```bash
 docker run -p 8000:8000 название вашего image
```
***
### API endpoints
#### Django admin panel.
##### Дефолтный логин=admin; пароль=1234;
    127.0.0.1:8000/admin

#### GET /buy/{id}/
    127.0.0.1:8000/buy/{id}/

#### GET /item/{id}/
    127.0.0.1:8000/item/{id}/
