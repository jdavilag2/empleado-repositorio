# Employee CRUD – SQL Server · .NET Web API · Angular 17

Este proyecto es una aplicación completa de gestión de empleados (CRUD: Create, Read, Update, Delete) desarrollada bajo una **arquitectura por capas**, utilizando:

- **Microsoft SQL Server** – Base de datos relacional  
- **.NET Web API** – Backend REST  
- **Angular 17** – Frontend moderno e interactivo  

---

## Arquitectura General

El desarrollo se realizó en **tres etapas principales**:

---

## Creación de la Base de Datos — SQL Server

Se creó la base de datos **EmployeesDB**, con la tabla principal **Employees**:

### **Tabla: Employees**

| Columna  | Tipo             | Descripción            |
|----------|------------------|------------------------|
| Id       | INT (PK, IDENTITY) | Identificador único |
| Name     | VARCHAR(100)     | Nombre del empleado   |
| Email    | VARCHAR(100)     | Correo electrónico    |
| Phone    | VARCHAR(20)      | Número telefónico     |
| Position | VARCHAR(50)      | Cargo                 |
| Salary   | DECIMAL(10,2)    | Salario               |

Además, se configuraron permisos básicos y conexión local para el backend.

---

## Desarrollo del Backend — .NET Web API

El backend se construyó con **ASP.NET Core Web API**, aplicando buenas prácticas:

- Inyección de dependencias (DI)  
- **Entity Framework Core** para acceso a SQL Server  
- Controladores REST organizados por entidad  
- DTOs y modelos de dominio  
- Configuración de CORS para permitir acceso desde Angular  

### **Endpoints principales**

| Método | Ruta                     | Descripción               |
|--------|---------------------------|---------------------------|
| GET    | `/api/employees`          | Obtener lista de empleados |
| GET    | `/api/employees/{id}`     | Obtener empleado por ID   |
| POST   | `/api/employees`          | Registrar empleado        |
| PUT    | `/api/employees/{id}`     | Actualizar empleado       |
| DELETE | `/api/employees/{id}`     | Eliminar empleado         |

---

## Desarrollo del Frontend — Angular 17

El frontend se construyó utilizando:

- **Standalone Components**
- Angular Material (opcional)
- Servicios para consumir la API
- Ruteo modular
- **Reactive Forms**

La aplicación permite:

- Listar empleados  
- Crear nuevos empleados  
- Editar registros  
- Eliminar empleados  
- Validar campos del formulario  

---

## Requisitos del Sistema

### **Backend (.NET)**  
- .NET 8 SDK o superior  
- SQL Server  
- Entity Framework Core  
- Visual Studio / VS Code  

### **Frontend (Angular)**  
- Node.js 18+  
- Angular CLI 17+  

---

## Configuración del Proyecto

### **1. Clonar el repositorio**

```bash
git clone <URL-del-repositorio>
cd employee-crud
