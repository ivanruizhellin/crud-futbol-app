# ⚽ Aplicación Web de Gestión Deportiva

> Desarrollo de una aplicación web para la gestión de competiciones deportivas utilizando **Flask**, **SQLAlchemy** y **SQLite**, con autenticación de usuarios, operaciones CRUD completas y una interfaz responsive basada en Bootstrap.

---

## 📑 Índice

- [📖 Descripción](#-descripción)
- [✨ Funcionalidades](#-funcionalidades)
- [🏗️ Arquitectura](#️-arquitectura)
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

Este proyecto consiste en el desarrollo de una aplicación web para la gestión de competiciones deportivas, realizada como parte de mi formación en **Administración de Sistemas Informáticos en Red (ASIR)**.

La aplicación permite administrar competiciones, temporadas, clubes, selecciones y usuarios mediante una interfaz web intuitiva, implementando operaciones **CRUD** completas, autenticación de usuarios y una base de datos relacional.

Durante su desarrollo se aplicaron buenas prácticas de organización del código siguiendo el patrón **MVC** adaptado a Flask, así como mecanismos de validación, seguridad y gestión de archivos.

---

# ✨ Funcionalidades

| Funcionalidad | Descripción |
|--------------|-------------|
| 🔐 **Autenticación** | Inicio y cierre de sesión mediante Flask-Login. |
| 👥 **Gestión de usuarios** | Administración de usuarios con control de acceso. |
| ⚽ **Competiciones** | Alta, edición, eliminación y consulta de competiciones. |
| 🏆 **Clubes** | Gestión completa de clubes deportivos. |
| 🌍 **Selecciones** | Administración de selecciones nacionales. |
| 📅 **Temporadas** | Gestión de temporadas y validación de duplicados. |
| 🖼️ **Gestión de imágenes** | Subida, sustitución y eliminación de escudos, banderas y logotipos. |
| 🔍 **Búsqueda** | Búsqueda global de información. |
| 🎯 **Filtros** | Filtrado por país, continente, tipo y alcance de las competiciones. |
| ↕️ **Ordenación** | Ordenación de registros por diferentes criterios. |
| 📊 **Exportación** | Exportación de datos en formato CSV. |

---

# 🏗️ Arquitectura

> *(Aquí añadiré un diagrama de la arquitectura de la aplicación.)*

```text
           Usuario
               │
               ▼
     HTML + Bootstrap + Jinja2
               │
               ▼
             Flask
        ┌──────┴──────┐
        │             │
     Routes        Forms
        │             │
        └──────┬──────┘
               ▼
         SQLAlchemy ORM
               │
               ▼
             SQLite
```

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
├── models.py
├── forms.py
└── routes.py
│
migrations/
│
requirements.txt
run.py
.env
```

La aplicación sigue una estructura basada en el patrón **MVC (Modelo - Vista - Controlador)**, separando la lógica de negocio, los modelos de datos, los formularios y la interfaz de usuario para facilitar el mantenimiento y la escalabilidad del proyecto.

---

# ⚙️ Tecnologías utilizadas

| Categoría | Tecnologías |
|-----------|-------------|
| 🐍 **Backend** | Python · Flask |
| 🗄️ **Base de datos** | SQLite · SQLAlchemy |
| 📝 **Formularios** | Flask-WTF |
| 🔐 **Autenticación** | Flask-Login |
| 🔄 **Migraciones** | Flask-Migrate |
| 🎨 **Frontend** | HTML5 · CSS3 · Bootstrap 5 · Bootstrap Icons · Jinja2 |
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
