clear

Proyecto Web: - ODS 4
Este proyecto es una propuesta tecnológica para mejorar la calidad educativa (ODS 4) desde la perspectiva del Desarrollo de Aplicaciones Web (DAW).

1. Análisis del Problema y Sostenibilidad (Responsable: Alumno A)
El "Bug" Educativo
[Alumno A: Escribe aquí el problema. Ejemplo: "Actualmente, muchos estudiantes rurales no tienen acceso a libros físicos y el gasto de papel en fotocopias es insostenible para el medio ambiente".]

Nuestro "Parche" (Impacto ODS 4)
[Alumno A: Explica la solución y la medida técnica. Ejemplo: "Nuestra web digitaliza los recursos. Como medida de sostenibilidad, usaremos un diseño 'Mobile First' y carga diferida de imágenes para reducir el consumo de datos y energía".]

2. Arquitectura de la Solución Web (Responsable: Alumno B)
Funcionalidades Principales
Nuestra plataforma web permitirá:

Funcionalidad 1: [Ejemplo: Registro de usuarios con perfiles de Alumno/Profesor].

Funcionalidad 2: [Ejemplo: Repositorio de materiales educativos en formato ligero].

Funcionalidad 3: [Ejemplo: Sistema de tutorías por chat de bajo consumo].

Entidades de Datos Básicas
Para que esta web funcione, almacenaremos:

Usuarios: Nombre, email, contraseña y rol.

Materiales: Título, descripción, archivo y categoría ODS.

1. Funcionalidades Principales
Sistema de Autenticación y Autorización (RBAC): Gestión completa de usuarios con control de acceso basado en roles (Admin, Editor, Viewer) y seguridad mediante tokens JWT para proteger las rutas del API.

Motor de Procesamiento de Datos en Lote: Capacidad para que el usuario cargue grandes volúmenes de información que el backend procesará en segundo plano, notificando al finalizar.

API Gateway Interoperable: Una interfaz RESTful estandarizada que permite que otros servicios o aplicaciones móviles consuman los datos de NovaCore de forma eficiente y documentada (vía Swagger/OpenAPI).

2. Entidades Principales (Base de Datos)
Para que el sistema sea escalable, la estructura de datos se dividirá en las siguientes tablas/colecciones:

Users (Usuarios): Almacena las credenciales y perfiles.

Campos: UUID, email, password_hash, status, last_login.

Resources (Recursos): El contenido central que gestiona la web.

Campos: resource_id, owner_id, title, description, storage_url, tags.

Logs / Transactions (Historial): Registro de auditoría de todos los cambios realizados en el sistema.

Campos: event_id, user_id, action_type (CREATE/UPDATE/DELETE), timestamp.

Permissions (Permisos): Define qué puede hacer cada rol sobre los recursos.

Campos: role_id, resource_type, access_level.

3. Stack Tecnológico Propuesto
Base de Datos: PostgreSQL (Relacional) para integridad de datos y Redis para gestión de sesiones en caché.

Backend: Node.js con el framework NestJS por su arquitectura modular y soporte nativo para TypeScript.

Infraestructura: Docker para la contenerización y despliegue consistente en cualquier entorno.

Mensajes: Emisor, receptor, contenido y fecha.




# Reto-ODS4-WebSostenible
  Hola
