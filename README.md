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
👉 Ingresamos al portal de Azure
🔗 [Portal Azure](https://portal.azure.com/) 
> 🚨 Si no posees una cuenta en Azure puedes optar por estas opciones:
> - [Crear un cuenta gratuita](https://azure.microsoft.com/es-es/free#all-free-services)
> - [Obtener una cuenta gratuita si eres estudiante](https://github.com/edu/students)

🛰️ Buscar en el marketplace Servidores flexibles de Azure Database for PostgreSQL
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/0a0f1c09-e0f9-46b8-befb-3ac315ef890f)

🛰️ Detalles basicos de la implementacion
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/8952592b-b5cd-44d2-9798-595ac0288906)

🛰️ Detalles del tipo de autentificacion
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/ccb9614a-afb3-4190-89b5-7bd43f28ac9c)

🛰️ Agregamos a nuestro firewal nuestra IP Publica (Solo para fines de ejemplo) en caso de implementarlo en produccion establecer reglas de seguridad.

![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/f32c857c-7554-45a2-89cd-252fe19073e0)

🛰️ Revisar y crear para posteriormente empezar con la implementación
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/452fc6f2-9c5f-47ac-a7be-65b532bfd1b6)

🛰️ Creamos una nueva base de datos en la instancia creada.
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/02b44316-903a-440f-b421-894bcd93259c)
Posteriormente lo conectamos mediante el Azure CLI para obtener las credenciales. 

# Implementación de frontend con Azure App Services en Azure
💡 Creamos el servicio de Web App (Azure App Services)
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/9910bb32-e05e-4ad9-a8e0-b834bddd29cc)

💡 Obtenemos el dominio personalizado
![image](https://github.com/CarlaMamaniChavez/starter/assets/66276312/2af3af80-ef25-4e0e-a209-2392d58f309c)

Y lo configuramos en Azure.py y Settings.py


# Recusos Adicionales
> - 🛩️[Documentación sobre instalacion de dependencias](https://www.freecodecamp.org/news/python-requirementstxt-explained/)
> - 🛩️[Documentación de SQLite](https://www.sqlite.org/index.html)
> - 🛩️[Documentación de Django Settings](https://docs.djangoproject.com/en/3.1/ref/settings/)
> - 🛩️[Documentación sobre Django - Migraciones](https://docs.djangoproject.com/en/5.0/topics/migrations/)
> - 🛩️[Documentación sobre Azure Database for PostgreSQL](https://learn.microsoft.com/es-es/azure/postgresql/)
> - 🛩️[Documentación sobre Azure SQL DataBase](https://learn.microsoft.com/es-es/azure/azure-sql/?view=azuresql)
> - 🛩️[Documentación sobre Azure App Services](https://learn.microsoft.com/es-es/azure/app-service/)

---

Espero de todo corazon que pueda ser util toda esta información en tu vida profesional.

**Hecho con 💚 Codigo Facilito by Carly** ☕


___


