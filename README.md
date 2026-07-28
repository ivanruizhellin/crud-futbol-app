# ⚽ Aplicación Web CRUD de Fútbol

> Desarrollo de una aplicación web con Python y Flask para gestionar competiciones de fútbol, temporadas, clubes, selecciones y usuarios. El proyecto implementa un sistema CRUD completo con autenticación, control de acceso, búsqueda, filtros y gestión de imágenes, siguiendo una estructura modular y buenas prácticas de desarrollo.

---

## 📑 Índice

- [📖 Descripción](#-descripción)
- [✨ Funcionalidades](#-funcionalidades)
- [📂 Estructura del proyecto](#-estructura-del-proyecto)
- [⚙️ Tecnologías utilizadas](#️-tecnologías-utilizadas)
- [🗄️ Modelo de datos](#️-modelo-de-datos)
- [🔐 Seguridad](#-seguridad)
- [🚀 Instalación](#-instalación)
- [📷 Capturas](#-capturas)
- [🚀 Mejoras futuras](#-mejoras-futuras)
- [👨‍💻 Autor](#-autor)

---

# 📖 Descripción

Este proyecto corresponde al trabajo final de la asignatura **Programación de Aplicaciones utilizando frameworks** del ciclo formativo de **Administración de Sistemas Informáticos en Red (ASIR)**.

La aplicación permite gestionar de forma centralizada la información relacionada con diferentes módulos. Permitiendo crear, consultar, modificar y eliminar información sobre:

Competiciones.
Temporadas.
Clubes de fútbol.
Selecciones nacionales.
Usuarios del sistema.

Cada competición puede contener múltiples temporadas, y cada temporada puede estar formada por diferentes clubes o selecciones según el tipo de competición.

Durante su desarrollo se aplicaron buenas prácticas de organización del código siguiendo el patrón **MVC** adaptado a Flask, así como mecanismos de validación, seguridad, gestión de archivos y documentación.

---

# ✨ Funcionalidades

| Funcionalidad | Descripción |
|--------------|-------------|
| 🔐 **Autenticación** | Inicio y cierre de sesión mediante Flask-Login. |
| 👥 **Gestión de usuarios** | Administración de usuarios con control de acceso. |
| ⚽ **CRUD completo** | Operaciones de creación, consulta, edición y eliminación para todas las entidades de la aplicación. |
| 🖼️ **Gestión de imágenes** | Subida, sustitución y eliminación de escudos, banderas y logotipos. |
| ✅ **Validaciones** | Control de campos obligatorios, prevención de registros duplicados y validación de extensiones de imágenes. |
| 🔍 **Búsqueda** | Búsqueda global de información. |
| 🎯 **Filtros** | Filtrado por país, continente, tipo y alcance de las competiciones. |
| ↕️ **Ordenación** | Ordenación de registros por diferentes criterios. |
| 📊 **Exportación** | Exportación de datos en formato CSV. |

---

# 📂 Estructura del proyecto

```text
app/
│
├── static/
│   ├── css/
│   └── img/
│
├── templates/
│
├── __init__.py
├── app.db
├── forms.py
├── models.py
├── routes.py
└── utils.py
│
migrations/
│
.env
requirements.txt
run.py
```

La aplicación sigue una estructura basada en el patrón **MVC (Modelo - Vista - Controlador)**, separando la lógica de negocio, los modelos de datos, los formularios y la interfaz de usuario para facilitar el mantenimiento y la escalabilidad del proyecto.

---

# ⚙️ Tecnologías utilizadas

| Categoría | Tecnologías |
|-----------|-------------|
| 🐍 **Backend** | Python · Flask |
| 🎨 **Frontend** | Jinja2 · HTML5 · CSS3 · Bootstrap 5 · Bootstrap Icons |
| 🗄️ **Base de datos** | SQLite |
| 📦 **ORM** | SQLAlchemy |
| 📝 **Formularios** | Flask-WTF |
| 🔐 **Autenticación** | Flask-Login |
| 🔄 **Migraciones** | Flask-Migrate |
| 🛡️ **Seguridad** | Werkzeug · python-dotenv |

---

# 🗄️ Modelo de datos

La aplicación utiliza una base de datos relacional implementada con **SQLite** y gestionada mediante **SQLAlchemy** como ORM.

Entre las principales entidades del sistema se encuentran:

- 👤 Usuarios
- ⚽ Competiciones
- 📅 Temporadas
- 🏆 Clubes
- 🌍 Selecciones

Las relaciones entre entidades incluyen asociaciones **1:N** y **N:M**, permitiendo modelar correctamente la información y garantizar su integridad.

> *(Aquí añadiré el diagrama entidad-relación de la base de datos.)*

---

# 🔐 Seguridad

Durante el desarrollo de la aplicación se implementaron diferentes mecanismos para mejorar la seguridad:

- Hash de contraseñas mediante **Werkzeug**.
- Protección **CSRF** en todos los formularios.
- Control de acceso mediante **Flask-Login**.
- Protección de rutas para usuarios autenticados.
- Validación de formularios y datos introducidos por el usuario.
- Renombrado de imágenes utilizando **UUID** para evitar conflictos de nombres.
- Almacenamiento de variables sensibles mediante archivos **.env**.

---

# 🚀 Instalación

## 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/ivanruizhellin/nombre-del-repositorio.git
```

## 2️⃣ Acceder al proyecto

```bash
cd nombre-del-repositorio
```

## 3️⃣ Crear un entorno virtual

```bash
python -m venv venv
```

## 4️⃣ Activar el entorno virtual

### Windows

```bash
venv\Scripts\activate
```

### Linux

```bash
source venv/bin/activate
```

## 5️⃣ Instalar las dependencias

```bash
pip install -r requirements.txt
```

## 6️⃣ Configurar las variables de entorno

Crear un archivo `.env` con la configuración necesaria.

## 7️⃣ Ejecutar la aplicación

```bash
flask run
```

o

```bash
python run.py
```

---

# 📷 Capturas

> *(Aquí añadiré las principales capturas de la aplicación.)*

- Pantalla de inicio de sesión
- Panel principal
- Gestión de competiciones
- Gestión de clubes
- Gestión de selecciones
- Gestión de temporadas
- Gestión de usuarios
- Exportación de datos

---

# 🚀 Mejoras futuras

- Implementación de roles y permisos avanzados.
- Panel de estadísticas con gráficos.
- API REST para integración con aplicaciones externas.
- Migración a PostgreSQL o MySQL.
- Contenerización mediante Docker.
- Pruebas automatizadas.
- Despliegue en un servidor Linux.

---

# 👨‍💻 Autor

**Iván Ruiz García**

Técnico Superior en Administración de Sistemas Informáticos en Red (ASIR)

- 💼 LinkedIn: https://linkedin.com/in/ivanruizhellin
- 🐙 GitHub: https://github.com/ivanruizhellin
