# :wave: Hola a todxs! y bienvenidos a esta CLASE extra del bootcamp de Backend Avanzando 🚀
En esta demo exploraremos cómo hospedar instancias de bases de datos en entornos de desarrollo y producción utilizando PostgreSQL y SQL Database. Además, aprenderemos a implementar nuestro sitio web mediante Azure App Services y como toque final, integraremos un dominio personalizado :zap:
# Requerimientos
| Lenguaje| Cloud | Editor |
|-----------|-----------|-----------|
| ![Python](https://img.shields.io/badge/python-≥_3.11-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)|![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)|![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)|
# Arquitectura
![Web Site en Azure drawio](https://github.com/CarlaMamaniChavez/starter/assets/66276312/71e1360c-4fb5-4635-8aee-a0d1cdd1f6f3)

# Inicio
👉 Clonamos este repositorio
```git
$ git clone https://github.com/CarlaMamaniChavez/starter.git
```
👉 Creamos nuestro entorno virtual y lo activamos
```bash
$ python -m venv venv
$ source venv/bin/activate
```
👉 Instalamos las dependencias
```bash
$ pip install -r .\requirements.txt
```
## Script para generar el secret_key 
### 👉  Ejecutamos el script secret_key_generator.py
```python
import secrets

def generate_django_secret_key(length=50):
    characters = 'abcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*(-_=+)'
    secret_key = ''.join(secrets.choice(characters) for i in range(length))
    return secret_key

django_secret_key = generate_django_secret_key()
print(django_secret_key)
```
# Implementación de backend con SQLite 3 en el ambiente de desarrollo
👉 Definimos el esquema de la base de datos
```bash
$ python .\manage.py makemigrations
$ python .\manage.py migrate   
```
👉 Creamos el usuario administrador en la base de datos
```bash
$ python .\manage.py createsuperuser 
```
👉 Levantamos el proyecto
```bash
$ python .\manage.py runserver
```
👉 Ingestamos informacion
🐕 Recordemos que un albergue posee varios perritos 🐕
Para ingestar los datos te proporciono un par de ejemplos 🐕

[CATALOGO  MASCOTAS.pdf](https://github.com/user-attachments/files/16056940/CATALOGO.MASCOTAS.pdf)

# Implementación de backend con PostgreSQL y Azure SQL Database en Azure


# Implementación de frontend con Azure App Services en Azure

# Recusos Adicionales
