Control de Entrada UTS

Descripción General:

El sistema permite registrar accesos (entradas y salidas) de personas a zonas específicas.
Gestiona usuarios con roles (ADMIN, OPERADOR, USUARIO) y ofrece estadísticas de uso del sistema.

El proyecto está estructurado según buenas prácticas, separando interfaz, lógica y modelos.


Tecnologías Utilizadas:

Java 8+

Patrón MVC simplificado

JDBC (conexión a PostgreSQL)

Interfaz

Java Swing

JPanel, JFrame y componentes personalizados

Base de Datos

PostgreSQL 14+

Servidor desplegado en Railway

Otros

Apache NetBeans (Proyecto Ant)

Exportación a CSV



Estructura del Proyecto:
src/
 ├── db/               # Manejo de conexión y ejecución SQL
 ├── interfaz/         # Paneles gráficos (Admin, Operador, Usuario…)
 ├── main/             # Clase Main de inicio
 ├── modelos/          # Entidades del negocio con CRUD
 ├── servicios/        # Lógica de aplicación (Usuario, Acceso, Exportación)
 └── utils/            # Utilidades (sesión, validación)


 

Módulos Principales:


1. Gestión de Usuarios

Incluye roles:

ADMIN: administra usuarios y consulta estadísticas

OPERADOR: registra accesos

USUARIO: aparece en la base de datos pero no tiene permisos en la interfaz



Funciones:

Registrar personas

Actualizar sus datos

Definir rol

Eliminar usuarios



2. Registro de Accesos

El operador registra:

Documento de la persona

Zona visitada

Tipo de acceso (permitido = entrada, no permitido = salida)



Cada registro incluye:

Fecha automática

Validación en BD

Relación con la tabla usuarios



3. Estadísticas

El sistema genera:

Conteo total de Entradas / Salidas

Accesos por día

Exportación a CSV




Instalación y Configuración

1. Clonar el repositorio
git clone https://github.com/tu-repo/control-entrada-uts.git

2. Importar proyecto en NetBeans

Abrir NetBeans → Open Project

Seleccionar la carpeta raíz del proyecto

3. Ejecutar

Ejecutar Main.java.

Funciones del Sistema
Para Administrador

Crear, editar, eliminar usuarios

Asignar roles

Revisar registros de accesos

Consultar estadísticas

Para Operador

Registrar entradas y salidas

Ver historial reciente

Para Usuario (nivel básico)

Solo existe en BD como entidad registrada

Exportación

El sistema permite exportar registros a CSV mediante:

ExportService.exportarCSV(...)

Licencia

Proyecto académico — UTS (Uso libre para fines educativos).
