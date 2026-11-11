# UrbanIntel

Sistema de gestión de deterioro urbano para municipalidades. Proyecto de Título, Duoc UC 2025.

UrbanIntel permite a los ciudadanos reportar fallas en la ciudad (alumbrado público, baches, etc.) y a los funcionarios municipales gestionarlas desde un panel de administración.

## Funcionalidades

**Ciudadano**
- Reporte de fallas urbanas por categoría.
- Seguimiento de las solicitudes enviadas.

**Funcionario municipal**
- Atención de solicitudes y asignación de estados.
- Vista de reportes con gráficos de barras (solicitudes por tipo, categorías predominantes) y filtros por criterios.
- Exportación de datos a PDF y Excel.

## Tecnologías

- **Frontend:** Angular 18, TypeScript
- **Backend:** ASP.NET Core (.NET 8), API REST documentada con Swagger
- **Autenticación:** JWT
- **Base de datos:** SQL Server (scripts en `Documentos UrbanIntel/Scripts DB`)
- **Servicios:** Azure Blob Storage (imágenes de solicitudes), SMTP (correos)

## Mi participación

## Mi participación

Trabajé en equipo en este proyecto. Me encargué del desarrollo del frontend en Angular y de su integración con la API REST:

**Módulo de Reportes**
- Tabla y gráficos de barras interactivos alimentados con datos de la API.
- Filtros funcionales, formato de fechas y barra de búsqueda que filtra por cualquier campo.
- Exportación de los datos a PDF y Excel.

**Módulo Home**
- Vista conectada al backend, con filtros y pines de colores según el tipo de reparación.

**Solicitudes**
- Exportación a PDF de la información de cada solicitud y del listado de solicitudes realizadas.

**Auditorías**
- Finalización del módulo con exportación a Excel.
- Definición de la paleta de colores para dar uniformidad visual al resto de las vistas.

**Interfaz general**
- Diseño del frontend y de la barra de navegación lateral del funcionario municipal.

## Requisitos

- Node.js 20.x
- Angular CLI 18.x
- .NET 8.0
- Visual Studio 2022
- SQL Server

## Ejecución

### Backend (UrbanIntelAPI)
1. Abrir `UrbanIntelAPI` en Visual Studio y restaurar los paquetes NuGet.
2. Configurar `appsettings.json` con tus propios valores (base de datos, clave JWT, Azure Storage y SMTP).
3. Ejecutar el proyecto (`Ctrl + F5`). Swagger queda disponible en `http://localhost:5016/`.

### Frontend (UrbanIntelWEB)
1. Entrar a la carpeta `UrbanIntelWEB/urbanintelweb`.
2. Ejecutar `npm install`.
3. Ejecutar `ng serve`. La aplicación queda disponible en `http://localhost:4200/`.

## Nota sobre el despliegue

El sistema se desplegó originalmente con base de datos y almacenamiento en Azure. La suscripción expiró, por lo que esos servicios ya no están disponibles. Para ejecutarlo localmente hay que crear la base de datos con los scripts incluidos y configurar `appsettings.json`.



<!-- Agregar aquí capturas del panel de reportes y de la vista del ciudadano -->
