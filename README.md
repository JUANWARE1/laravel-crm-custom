---------------------------------------------------- CRM LARAVEL HIBRIDO ----------------------------------------------------------------

Este proyecto es un CRM híbrido construido sobre Laravel como framework base, integrando módulos desarrollados en PHP. Esta arquitectura permite aprovechar las ventajas de Laravel (seguridad, configuración, estructura, middlewares) mientras se mantiene compatibilidad con módulos existentes o desarrollados fuera del flujo MVC estándar.
El sistema está diseñado para ser escalable, mantenible y comprensible para nuevos ingenieros que se integren al proyecto.

--------------------------------------------------- ARQUITECTURA DEL SISTEMA -------------------------------------------------------------

El proyecto se divide en tres capas principales:

 ■ Capa Framework (Laravel)
 ■ Manejo de configuración general
 ■ Autenticación de usuarios
 ■ Middlewares y seguridad
 ■ Rutas base del sistema

Ubicación principal:
/app
/routes
/config
/database 

Capa Core CRM (Legacy):

 ■ Logica de negocio desarrollada en PHP tradicional
 ■ Vistas renderizadas sin Blade
 ■ Includes, helpers y flujos personalizados

      Nota: Estas secciones no siguen estrictamente el Modelo Vista Controlador (MVC).

Capa de Presentación:

 ■ HTML / CSS / JavaScript
 ■ Assets públicos
 ■ Formularios y dashboards
 
Stack Tecnológico: 

 ■ Backend: PHP 8.x, Laravel
 ■ Frontend: HTML, CSS, JavaScript
 ■ Base de Datos: MySQL
 ■ Servidor: Apache / Nginx
 ■ Gestor de dependencias: Composer

--------------------------------------------------- Requisitos del Sistema -------------------------------------------------------------------

Desarrollo:

 ■ PHP >= 8.0
 ■ Composer
 ■ MySQL >= 8
 ■ Laragon / XAMPP / Docker
 ■ Producción
 ■ Linux recomendado
 ■ Apache o Nginx
 ■ Extensiones PHP habilitadas:
 ■ pdo
 ■ mbstring
 ■ openssl
 ■ tokenizer

Instalación del Proyecto:

 ■ git clone <repositorio>
 ■ cd laravel-crm
 ■ composer install
 ■ cp .env.example .env
 ■ php artisan key:generate
 ■ php artisan migrate
 ■ php artisan serve

      Nota: Configurar las credenciales de base de datos en el archivo .env.

--------------------------------------------------- Estructura del Proyecto ------------------------------------------------------------------

Laravel estándar:

app/
routes/
database/
config/

Carpetas personalizadas (Legacy):

 ■ Estas carpetas contienen la lógica y vistas del CRM fuera del flujo Laravel tradicional:

     Nota: Estas carpetas deben ser documentadas cuidadosamente antes de realizar cualquier refactor.

Seguridad:

 ■ Autenticación gestionada por Laravel
 ■ Protección CSRF habilitada
 ■ Validaciones de entrada obligatorias
 ■ Control de acceso por middleware


Flujo General del Sistema:

 ■ Usuario accede al sistema
 ■ Autenticación vía Laravel
 ■ Redirección a módulos del CRM
 ■ Carga de vistas legacy y lógica de negocio


Extensión del Sistema:

 ■ Para agregar nuevas funcionalidades:
 ■ Preferentemente usar Laravel (Controllers + Models)
 ■ Evitar agregar más lógica legacy
 ■ Documentar cualquier excepción

Roadmap Técnico:

 ■ Migración progresiva de módulos legacy a Laravel
 ■ Centralización de vistas en Blade
 ■ Refactor de lógica procedural a Services


Documentación Adicional:

Ver carpeta /docs para documentación detallada:

 ■ Arquitectura
 ■ Flujo del CRM
 ■ Módulos
 ■ Convenciones

Autoría:

Proyecto documentado para uso interno y clientes finales.