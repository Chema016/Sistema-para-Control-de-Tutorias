# Sistema de Control de Tutorías

Este proyecto es un sistema web desarrollado para facilitar el seguimiento de las tutorías académicas en una institución educativa. Permite al administrador gestionar tutores y alumnos, mientras que los tutores pueden organizar citas, registrar el seguimiento de sus alumnos y generar reportes relacionados con su desempeño académico.

**Tecnologías utilizadas:**

* HTML5
* CSS3
* JavaScript
* PHP 8
* Supabase (PostgreSQL)

---

# 1. Crear la base de datos en Supabase

1. Ingresa a tu cuenta de Supabase y crea un proyecto nuevo.
2. Espera a que el proyecto termine de crearse.
3. En el menú lateral selecciona **SQL Editor** y crea una nueva consulta.
4. Abre el archivo **sql/schema.sql** que se encuentra dentro del proyecto.
5. Copia todo su contenido, pégalo en el editor de Supabase y presiona **Run**.

Con esto se crearán todas las tablas necesarias para que el sistema funcione correctamente.

---

# 2. Configurar el proyecto

El proyecto viene configurado con una base de datos de ejemplo. Si deseas utilizar tu propia base de datos, solo debes editar el archivo:

`config/config.php`

y reemplazar los siguientes datos:

```php
define('SUPABASE_URL', 'https://TU-PROYECTO.supabase.co');
define('SUPABASE_SERVICE_KEY', 'TU_SERVICE_ROLE_KEY');
```

No es necesario modificar ningún otro archivo.

---

# 3. Credenciales del administrador

El sistema cuenta con un administrador principal para acceder al panel de administración.

**Usuario**

```
admin@tutorias.com
```

**Contraseña**

```
Admin123!
```

Si deseas cambiar estas credenciales, puedes hacerlo desde el archivo:

`config/config.php`

Los profesores o tutores sí se almacenan en la base de datos y pueden ser creados desde el panel del administrador.

---

# 4. Ejecutar el proyecto

Desde la carpeta principal del proyecto abre una terminal y ejecuta:

```bash
php -S localhost:8000
```

Después abre tu navegador e ingresa a:

```
http://localhost:8000
```

Aparecerá la pantalla de inicio de sesión.

---

# 5. ¿Cómo utilizar el sistema?

### Como administrador

* Iniciar sesión.
* Registrar profesores o tutores.
* Registrar alumnos mediante un archivo de Excel o de forma manual.
* Asignar alumnos a un tutor.
* Consultar la información registrada por los tutores.

### Como tutor

Después de iniciar sesión podrá:

* Consultar los alumnos que tiene asignados.
* Programar citas de tutoría.
* Registrar la asistencia de los alumnos.
* Llevar una bitácora de cada sesión.
* Crear reportes de canalización cuando sea necesario.
* Registrar alertas para alumnos que presenten riesgo académico o de deserción.

---

# 6. Estructura del proyecto

```
Sistema para Control de Tutorías/

├── sql/
├── config/
├── includes/
├── api/
├── admin/
├── tutor/
├── assets/
└── index.php
```

---

