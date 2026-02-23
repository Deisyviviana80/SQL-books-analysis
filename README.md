# 📚 SQL Books - Análisis de una Plataforma de Lectura

## 📖 Descripción del Proyecto

Este proyecto analiza la base de datos de una plataforma de lectura en línea con el objetivo de extraer información estratégica que apoye la toma de decisiones del negocio. El análisis responde cinco preguntas clave sobre el catálogo de libros, el comportamiento de los usuarios y el desempeño de autores y editoriales.

El proyecto fue desarrollado como parte del programa de formación Bootcamp en análisis de datos de **Tripleten**.

---

## 🎯 Objetivos del Análisis

- Identificar tendencias en la publicación de libros a partir del año 2000.
- Analizar el comportamiento de los usuarios respecto a calificaciones y reseñas.
- Determinar las editoriales y autores con mejor desempeño.
- Explorar el comportamiento de los usuarios más activos en la plataforma.

---

## 🗂️ Estructura de la Base de Datos

La base de datos está compuesta por cinco tablas relacionadas entre sí:

| Tabla | Descripción | Columnas principales |
|-------|-------------|----------------------|
| `books` | Catálogo de libros | book_id, title, author_id, publisher_id, num_pages, publication_date |
| `authors` | Información de autores | author_id, author |
| `publishers` | Información de editoriales | publisher_id, publisher |
| `ratings` | Calificaciones de usuarios | rating_id, book_id, username, rating |
| `reviews` | Reseñas escritas de usuarios | review_id, book_id, username, text |

---

## 🔍 Consultas y Hallazgos

### 1. 📅 Libros publicados después del 1 de enero de 2000
De un total de 1,000 libros en el catálogo, **819 fueron publicados entre 2000 y 2020**, lo que representa el **81.9% del total**. Esto refleja una tendencia clara hacia contenido contemporáneo y una plataforma orientada al lector moderno.

### 2. ⭐ Número de reseñas y calificación promedio por libro
La mayoría de los libros reciben entre 2 y 5 reseñas, y las calificaciones se concentran en el rango de **3.5 a 4.5 sobre 5**, lo que indica una satisfacción general positiva. Los libros con pocas reseñas presentan mayor varianza en calificaciones, evidenciando sesgo estadístico por bajo volumen.

### 3. 🏢 Editorial con más libros de más de 50 páginas
**Penguin Books** lidera el catálogo con **42 títulos** de más de 50 páginas, reflejando su amplia presencia y prestigio en la plataforma.

### 4. ✍️ Autor con la calificación promedio más alta
**J.K. Rowling / Mary GrandPré** obtiene la calificación promedio más alta: **4.28 / 5.0**, calculada sobre libros con al menos 50 calificaciones cada uno, garantizando un resultado estadísticamente representativo (310 calificaciones en total).

### 5. 👥 Comportamiento de los usuarios más activos
Los usuarios que calificaron más de 50 libros escribieron en promedio **24.33 reseñas de texto**, lo que demuestra que los usuarios más activos también son los más comprometidos con la comunidad.

---

## 💡 Recomendaciones Estratégicas

1. **Mantener y ampliar el catálogo contemporáneo**, aprovechando el momentum de publicaciones post-2000.
2. **Implementar mecanismos para fomentar reseñas escritas**, ya que la mayoría de los libros tienen pocas opiniones textuales.
3. **Crear un programa de super usuarios** para retener y potenciar a quienes más contribuyen a la comunidad.
4. **Establecer acuerdos estratégicos con Penguin Books** y otras editoriales líderes para garantizar acceso a nuevas publicaciones.
5. **Destacar a los autores mejor calificados** en sistemas de recomendación para mejorar la experiencia del usuario.

---

## 🛠️ Tecnologías Utilizadas

- **Python 3**
- **pandas** — manipulación y análisis de datos
- **SQLAlchemy** — conexión y ejecución de consultas SQL
- **PostgreSQL** — motor de base de datos
- **matplotlib / seaborn** — visualización de datos
- **Jupyter Notebook** — entorno de desarrollo

---

## 📁 Archivos del Repositorio

```
📦 sql-books-analysis
 ┣ 📓 SQL_mejorado.ipynb   # Notebook principal con el análisis completo
 ┗ 📄 README.md            # Este archivo
```

---

## ▶️ ¿Cómo ejecutar el proyecto?

> ⚠️ Este proyecto se conecta a una base de datos remota académica proporcionada por Practicum/Yandex. La conexión externa puede no estar disponible fuera del entorno del curso.

Para explorar el notebook localmente sin conexión activa, puedes revisar los resultados y visualizaciones ya guardados en el archivo `.ipynb`.

```bash
# Instalar dependencias
pip install pandas sqlalchemy psycopg2-binary matplotlib seaborn

# Abrir el notebook
jupyter notebook SQL_mejorado.ipynb
```

---

## 👩‍💻 Autora

Proyecto desarrollado como parte del programa de **Análisis de Datos — Tripleten**.

---

*Este repositorio forma parte de mi portafolio de proyectos de análisis de datos.*
