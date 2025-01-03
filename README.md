# M7-L3-ORMDefinicionModelo-Parte2_02-01-2025
Proyecto educativo

# Gestión de Cursos

Este proyecto es una aplicación web desarrollada en Django para gestionar cursos, permitiendo listar, crear, y administrar información relacionada con los cursos.

## Características
- **Gestión de cursos**: Permite crear, listar, y administrar cursos.
- **Formulario dinámico**: Utiliza formularios basados en modelos para facilitar la entrada de datos.
- **Base de datos MySQL**: Conexión y manejo de datos persistentes mediante MySQL.

## Requisitos previos

Asegúrate de tener instalados los siguientes programas y dependencias antes de iniciar el proyecto:

- Python 3.8+
- Django 4.0+
- MySQL
- Pipenv o virtualenv para la gestión de entornos virtuales

## Instalación

Sigue estos pasos para configurar y ejecutar el proyecto en tu entorno local:

1. **Clonar el repositorio**:
   ```bash
   git clone <URL-del-repositorio>
   cd gestion-cursos
   ```

2. **Crear y activar un entorno virtual**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instalar las dependencias**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configurar la base de datos**:
   - Asegúrate de tener MySQL configurado y funcionando.
   - Crea una base de datos llamada `Gestion_Cursos_DB`.
   - Configura las credenciales de usuario en el archivo `settings.py` bajo la sección `DATABASES`.

5. **Aplicar las migraciones**:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Ejecutar el servidor de desarrollo**:
   ```bash
   python manage.py runserver
   ```

## Uso

1. **Página de inicio**: Navega a la URL raíz del servidor (`http://127.0.0.1:8000/`) para acceder a la página principal.
2. **Lista de cursos**: Ve a `http://127.0.0.1:8000/cursos/` para ver los cursos registrados.
3. **Crear un curso**: Navega a `http://127.0.0.1:8000/cursos/crear/` para añadir un nuevo curso utilizando el formulario interactivo.

## Estructura del proyecto

- **`models.py`**: Define el modelo `Curso` con atributos como nombre, descripción, duración en horas, fecha de inicio y fin.
- **`forms.py`**: Contiene el formulario `CursoForm` basado en el modelo `Curso`.
- **`views.py`**: Contiene las vistas para manejar la lógica de la aplicación, incluyendo la creación y listado de cursos.
- **`templates/gestion_cursos`**: Directorio con las plantillas HTML para las vistas.

## Configuración de la base de datos

En el archivo `settings.py`, la configuración de la base de datos utiliza MySQL:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'Gestion_Cursos_DB',
        'USER': 'root',
        'PASSWORD': 'admin1234',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

Asegúrate de cambiar las credenciales por las de tu entorno.

## Tecnologías utilizadas

- **Django**: Framework de desarrollo web.
- **MySQL**: Sistema de gestión de bases de datos relacional.
- **HTML**: Para el diseño de plantillas.

## Contribuciones

Si deseas contribuir al proyecto:
1. Haz un fork del repositorio.
2. Crea una rama con tus cambios: `git checkout -b mi-rama`.
3. Realiza un pull request.

## Licencia

Este proyecto está bajo la licencia MIT. Puedes consultar el archivo `LICENSE` para más detalles.

---

¡Gracias por usar la aplicación Gestión de Cursos!