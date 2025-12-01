📌 Employee CRUD – SQL Server · .NET Web API · Angular 17

Este proyecto es una aplicación completa de gestión de empleados (CRUD: Create, Read, Update, Delete) desarrollada en una arquitectura por capas, donde se emplean las siguientes tecnologías:

Microsoft SQL Server – Base de datos relacional.

.NET Web API – Backend para exponer servicios REST.

Angular 17 – Frontend moderno para interacción del usuario.

🚀 Arquitectura General

El flujo de desarrollo se realizó en tres etapas principales:

1️⃣ Creación de la Base de Datos — SQL Server

Se creó una base de datos llamada EmployeesDB, la cual contiene una tabla principal:

Tabla: Employees

Columna	Tipo	Descripción
Id	INT (PK, IDENTITY)	Identificador único
Name	VARCHAR(100)	Nombre del empleado
Email	VARCHAR(100)	Correo electrónico
Phone	VARCHAR(20)	Número telefónico
Position	VARCHAR(50)	Cargo
Salary	DECIMAL(10,2)	Salario

Además, se configuraron permisos básicos y conexión local para el backend.

2️⃣ Desarrollo del Backend — .NET Web API

El backend se desarrolló con ASP.NET Core Web API, siguiendo buenas prácticas como:

Inyección de dependencias (DI)

Entity Framework Core para comunicación con SQL Server

Controladores REST organizados por entidad

DTOs y modelos de dominio

Manejo de CORS para permitir el acceso desde Angular

Endpoints principales
Método	Ruta	Descripción
GET	/api/employees	Obtener lista de empleados
GET	/api/employees/{id}	Obtener empleado por ID
POST	/api/employees	Registrar empleado
PUT	/api/employees/{id}	Actualizar empleado
DELETE	/api/employees/{id}	Eliminar empleado
3️⃣ Desarrollo del Frontend — Angular 17

La interfaz fue creada con Angular 17 utilizando:

Standalone Components

Angular Material para UI (opcional)

Servicios para consumir la API

Ruteo modular

Formularios reactivos (Reactive Forms)

La aplicación permite:

✔ Listar empleados
✔ Crear un nuevo empleado
✔ Editar un registro existente
✔ Eliminar empleados
✔ Validar campos del formulario

🛠 Requisitos del Sistema
Backend (.NET)

.NET 8 SDK o superior

SQL Server (local o remoto)

Entity Framework Core

Visual Studio / VS Code

Frontend (Angular)

Node.js 18+

Angular CLI 17+

🔧 Configuración del Proyecto
1. Clonar el repositorio
git clone <URL-del-repositorio>
cd employee-crud

🗄 Configurar la Base de Datos (SQL Server)

Ejecutar el script SQL incluido en la carpeta /database o crear manualmente la tabla:

CREATE DATABASE EmployeesDB;

USE EmployeesDB;

CREATE TABLE Employees (
    Id INT IDENTITY PRIMARY KEY,
    Name VARCHAR(100),
    Email VARCHAR(100),
    Phone VARCHAR(20),
    Position VARCHAR(50),
    Salary DECIMAL(10, 2)
);

⚙ Configurar Backend (.NET Web API)
Restaurar dependencias
cd backend
dotnet restore

Configurar la cadena de conexión

En appsettings.json:

"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=EmployeesDB;Trusted_Connection=True;"
}

Ejecutar el servidor
dotnet run


La API estará disponible en:

https://localhost:5001
http://localhost:5000

🖥 Configurar Frontend (Angular 17)
Instalar dependencias
cd frontend
npm install

Ejecutar la aplicación
ng serve


La aplicación estará disponible en:

http://localhost:4200

📂 Estructura del Proyecto
employee-crud/
│
├── database/               # Script SQL
├── backend/                # Web API en .NET
│   ├── Controllers/
│   ├── Models/
│   ├── DTOs/
│   ├── Data/
│   └── Services/
│
└── frontend/               # Angular 17
    ├── src/
    │   ├── app/
    │   │   ├── pages/
    │   │   ├── services/
    │   │   ├── components/
    │   │   └── models/
    └── angular.json

🧪 Pruebas

Postman para probar endpoints

SQL Server Management Studio para validar datos

Pruebas manuales desde Angular

📜 Licencia

Este proyecto se comparte únicamente con fines educativos y puede ser modificado libremente.
