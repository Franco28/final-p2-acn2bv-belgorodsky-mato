# Billie Eilish Discografia — Final Programación Web II
Aplicación CRUD con PHP que administra la discografía de Billie Eilish con filtros, paginación y cambio de tema. La UI trabaja vía AJAX para no recargar la página y usa SweetAlert2 para dar feedback de las respuestas.

## Partes principales
- `index.php`: vista principal con listado, buscador/filtros y paginación; crea/edita/borra discos; cambia entre tema oscuro y claro sin recargar.
- `api.php`: capa de datos; conecta a la base, trae la discografía y recibe las acciones de alta/edición/baja con validaciones de servidor (ej. `if (empty(...))`).
- `style.css`: estética inspirada en Billie Eilish (acento neón/oscuro) y variantes light/dark; diseño responsive.
- Validaciones completas: `required` en el HTML y chequeos de backend para evitar campos vacíos.
- SweetAlert2: alertas/confirmaciones para formularios y errores.
- AJAX/fetch: todas las consultas al backend y actualizaciones del DOM sin refrescar.

## Tecnologías
- PHP 8+, MySQL/MariaDB o compatible.
- HTML5, CSS3, JavaScript (fetch).
- SweetAlert2 como librería externa.
- XAMPP como servidor local.

## Cómo levantar el proyecto
1) Configurá las credenciales de base de datos en `db/config.php` (host, usuario, contraseña y nombre de la base).  
2) Importa el script de billie_discografia.sql en el gestor de base de datos.  
3) Iniciá un servidor local XAMPP por ejemplo.  
4) Abrí `http://localhost:8000/index.php` en el navegador.

## Funcionalidades a probar
- Listar la discografía con filtros y paginación desde `index.php`.
- Crear un nuevo disco; validar campos requeridos y ver la alerta de éxito/error.
- Editar y eliminar registros (confirma con SweetAlert2).
- Cambiar de tema claro/oscuro y navegar la app en móviles para ver el layout responsive.
