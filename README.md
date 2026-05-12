# Tienda Perritos DevOps

Proyecto académico orientado a la implementación de una arquitectura DevOps utilizando AWS, Docker, GitHub Actions y CI/CD para el despliegue automatizado de una aplicación web CRUD de productos para una tienda de mascotas.

---

# Objetivo del Proyecto

Implementar una solución basada en microservicios desplegada en AWS utilizando:

- Docker
- Amazon EC2
- Amazon ECR
- AWS Systems Manager (SSM)
- GitHub Actions
- CI/CD automatizado
- MySQL
- Node.js
- Frontend HTML/CSS/JS

El sistema permite gestionar productos de una tienda de mascotas mediante operaciones CRUD.

---

# Arquitectura

La solución se encuentra separada en 3 instancias EC2:

| Servicio | Función |
|---|---|
| Frontend | Interfaz web |
| Backend | API REST Node.js |
| DB | Base de datos MySQL |

---

# Infraestructura AWS

## Servicios utilizados

- Amazon EC2
- Amazon ECR
- AWS Systems Manager (SSM)
- VPC personalizada
- Security Groups
- Elastic IP
- GitHub Actions

---

# Contenedores Docker

## Frontend

- Nginx
- HTML/CSS/JavaScript

## Backend

- Node.js
- Express
- MySQL2

## Base de Datos

- MySQL 8
- Script de inicialización automático (`init.sql`)

---

# CI/CD

El proyecto utiliza GitHub Actions para automatizar:

- Build de imágenes Docker
- Push a Amazon ECR
- Despliegue automático en EC2 mediante SSM

---

# Estructura del Proyecto

```bash
.
├── backend/
│   ├── server.js
│   ├── Dockerfile
│   └── package.json
│
├── frontend/
│   ├── app.js
│   ├── index.html
│   ├── style.css
│   └── Dockerfile
│
├── db/
│   ├── init.sql
│   └── Dockerfile
│
└── .github/
    └── workflows/
        ├── cicd-tienda-backend.yml
        ├── cicd-tienda-frontend.yml
        └── cicd-tienda-db.yml