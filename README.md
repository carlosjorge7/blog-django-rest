# blog-django-rest

# crear entorno virtual y activarlo

virtualenv venv  
source ./venv/Scripts/activate

# Instalar las dependencias

pip install -r requirements.txt

# Generar django proyect

django-admin startproject core .

# generate blog api

python manage.py startapp blog

# Añadir al fichero de core/settings

'blog'

# Hacemos las migraciones (en /api)

python manage.py makemigrations
python manage.py migrate

# Creamos un superusuario para crear post (en /api)

python manage.py createsuperuser

# Ejecutamos el servidor

python manage.py runserver 5000
