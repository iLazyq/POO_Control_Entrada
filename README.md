Control de Entrada UTS

Sistema desarrollado en Java Swing con PostgreSQL (Railway) para gestionar la entrada y salida de usuarios en una institución.
Incluye autenticación, control de accesos, administración de usuarios y registro histórico alojado en una base de datos en la nube.

Descripción General

El sistema permite que distintos usuarios registren entrada y salida en las instalaciones.
Cuenta con autenticación por rol, paneles específicos según el tipo de usuario y registro histórico de accesos.

Roles del Sistema
Administrador

Gestiona usuarios (crear, editar, desactivar).

Visualiza estadísticas.

Revisa historial general.

Acceso al AdminPanel.

Operador

Registra entrada y salida de usuarios.

Consulta accesos recientes.

Acceso al OperadorPanel.

Usuario

Consulta su información y su historial.

Acceso al UsuarioPanel.

Funcionalidades Principales

Autenticación mediante LoginFrame.

Manejo de sesión con SessionManager.

Registro de entrada y salida con fecha y hora automática.

Consulta de historial de accesos.

Administración de usuarios (Administrador).

Exportación de datos (si se usa ExportService).

Estructura del Proyecto
/db
    DatabaseHandler.java
    ResultSetHandler.java

/interfaz
    AdminPanel.java
    CreateUserDialog.java
    InterfazGUI.java
    LoginFrame.java
    MainFrame.java
    OperadorPanel.java
    UsuarioPanel.java
    VentanaEditarUsuario.java

/main
    Main.java

/modelos
    Acceso.java
    Estadisticas.java
    Persona.java
    Tecnico.java
    Usuario.java

/servicios
    AccesoService.java
    ExportService.java
    UsuarioService.java

/utils
    SessionManager.java
    Validator.java

Base de Datos (Sin tuplas)
Tabla usuarios

id

nombre

documento

username

password

rol

activo

Tabla accesos

id

usuario_id

fecha_hora

tipo_movimiento
