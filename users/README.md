# Administración de Libros de la Escuela

## Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar una aplicación web para la administración de reservas de libros de una escuela. La plataforma permitirá a los alumnos y padres de familia realizar reservas de libros y proporcionará a la administración una forma eficiente de gestionar dichas reservas, mejorando la organización y el control del inventario de libros.

## Objetivos Principales

- Permitir a los alumnos y padres reservar libros desde la página web.
- Facilitar la gestión de las reservas por parte de la administración de la escuela.
- Proporcionar notificaciones automáticas y herramientas de seguimiento para mejorar la experiencia del usuario y la administración.

## Esquemática del Proyecto

### Recoger Información
- **Proceso de trabajo**
- **Organización**

### Análisis
- **Actores y Objetivos**
- **Requerimientos funcionales**

### Modelo de Datos
- **Modelo Entidad-Relación (ER)**
- **Base de Datos**
- **Diccionario de Datos**

### Diseño
- **Guías de Estilo**
- **Bocetos**
- **Mockups**

### Desarrollo
- **Modelo**
- **Vista**
- **Controlador**

## Requerimientos Funcionales

**F1 - Inicio de Sesión (Administración)**
- **F1.1 Logins separados:**
  - **F1.1.1** Uno para la administración.
  - **F1.1.2** Uno para el seguimiento de las reservas (ver punto 2.2).

**F2 - Realizar reserva**
- **2.1** El usuario realiza la reserva online sin login, añadiendo la siguiente información:
  - DNI
  - Nombre
  - Apellido
  - Correo electrónico
- **2.2** Si el usuario desea realizar un seguimiento puede activar una cuenta temporal que se vincula a su correo electrónico.
  - **2.2.1** El usuario podrá cambiar su contraseña.
- **2.3** El usuario recibirá un correo cada vez que se actualice el estado de la reserva.
- **2.4** La administración puede realizar la reserva del alumno.
  - **2.4.1** Necesita justificante de pago y los datos del alumno.

**F4 - Gestión de Reservas (Administración)**
- **F4.1** Permitir a la administración actualizar fácilmente los estados de la reserva:
  - **F4.1.1** La aplicación enviará un correo electrónico al tutor cuando el libro llegue.
  - **F4.1.2** Permitir la eliminación de la reserva con un motivo registrado (si la reserva es rechazada).
  - **F4.1.3** Enviar un correo al tutor con la observación sobre el rechazo de la reserva.
  - **F4.1.4** Los estados de la reserva podrán ser modificados por la administración.

**F5 - Obtener los Datos (Sólo Administración)**
- **F5.1** Agrupación de las reservas por libro y curso.
- **F5.2** Poder filtrar la información por parámetros:
  - Curso, fecha de reserva, fecha límite, estado de reserva, etc.
- **F5.3** Permitir visualizar los estados de la reserva.
- **F5.4** Poder exportar los datos a un archivo Excel.
- **F5.5** Hacer un volcado general de la base de datos.

## División Lógica de la Aplicación Web

La aplicación web se dividirá en las siguientes partes lógicas:

### 1. Frontend
- **Tecnologías sugeridas**: HTML, CSS, JavaScript .
- **Funcionalidades**:
  - Formulario de reservas para alumnos y padres.
  - Panel de usuario para realizar el seguimiento de reservas.
  - Interfaz de inicio de sesión para la administración.
  - Visualización de reservas, estados y notificaciones.

### 2. Backend
- **Tecnologías sugeridas**: PHP.
- **Funcionalidades**:
  - Gestión de autenticación y autorización (usuarios y administración).
  - Controlador para manejar reservas y cambios de estado.
  - Envío de correos electrónicos de notificación.
  - Integración con la base de datos para almacenamiento y consultas.

### 3. Base de Datos
- **Tecnologías sugeridas**: MySQL/MariaDB.
- **Funcionalidades**:
  - Almacenamiento de datos de reservas, usuarios y administración.
  - Gestión de estados de reserva y registro de actividad.
  - Volcado de datos y exportaciones a archivos.

### 4. API (Opcional)
- **Funcionalidades**:
  - Exponer endpoints para operaciones CRUD (Crear, Leer, Actualizar, Eliminar) relacionadas con reservas.
  - Integración con servicios externos si es necesario (ej. notificaciones o pagos).

### 5. Seguridad
- **Consideraciones**:
  - Almacenamiento seguro de contraseñas.
  - Control de acceso basado en roles.
