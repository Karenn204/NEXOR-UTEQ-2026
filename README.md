# NEXOR - Sistema de Gestión de Proyectos

## 📁 Estructura del Proyecto

Este repositorio contiene tanto el **backend** como el **frontend** del sistema NEXOR.

---

# 🔧 BACKEND - NEXOR-BACK

Backend construido con **Node.js** y **Express.js**, siguiendo una arquitectura MVC con controladores, rutas, middlewares y servicios.

## 📋 Requisitos Previos
- Node.js (v14 o superior recomendado)
- npm o yarn
- Base de datos (MySQL, PostgreSQL o MongoDB)
- Git (opcional)

## 🚀 Cómo Ejecutar el Backend

### 1. Instalar dependencias
- npm install o yarn intall

### 2.Configurar variables de entorno
Crea un archivo .env en el directorio raíz del backend:

----------------------------
PORT=3000
DB_HOST=localhost
DB_USER=tu_usuario
DB_PASSWORD=tu_contraseña
DB_NAME=tu_base_datos
JWT_SECRET=tu_clave_secreta
----------------------------

### 4. Configurar la base de datos
Crea la base de datos sgp_db e importa su script

5. Ejecutar la aplicación
# Modo desarrollo
npm run dev
# Modo producción
npm start

## 📦 Dependencias Principales
- Express.js: Framework web
- Sequelize/Mongoose: ORM/ODM-
- JWT: Autenticación
- Multer: Carga de archivos
- Nodemailer: Servicio de correo
- bcrypt: Hash de contraseñas

## 📂 Estructura del Backend

BACKEND/
 ├── node_modules/
 ├── src/
 │   ├── config/           # Configuraciones (DB, JWT)
 │   ├── controllers/      # Controladores de la lógica de negocio
 │   ├── middlewares/      # Middlewares de autenticación y roles
 │   ├── models/           # Modelos de datos
 │   ├── routes/           # Rutas de la API
 │   ├── services/         # Servicios (email, archivos)
 │   ├── uploads/          # Archivos subidos
 │   │   └── documents/    # Documentos por proyecto
 │   ├── utils/            # Utilidades (JWT, multer)
 │   ├── app.js            # Configuración de Express
 │   └── server.js         # Punto de entrada
 ├── .env
 ├── .gitignore
 ├── package.json
 └── package-lock.json

---

# 🎨 FRONTEND - NEXOR-FRONT

Frontend desarrollado con React y JSX, utilizando Vite como herramienta de build.

## 🛠️ Tecnologías y Dependencias
- React: Biblioteca principal
- Vite: Herramienta de build y desarrollo
- React Router: Navegación
- ESLint: Linter para código
- CSS: Estilos

## 📋 Requisitos para Ejecutar el Frontend
1. Instalar Node.js (versión >= v16)
2. Instalar dependencias
- npm install

3. Ejecutar la aplicación
# Modo desarrollo
npm run dev
# Modo producción
npm run build

## 📂 Estructura del Frontend
FRONTEND/
├── node_modules/
├── public/
│   ├── pdf.worker.min.mjs
│   └── vite.svg
├── src/
│   ├── assets/           # Imágenes y recursos estáticos
│   ├── components/       # Componentes reutilizables
│   │   ├── Messages/     # Componentes de mensajes
│   │   ├── Modals/       # Modales (crear cuenta, reset password)
│   │   ├── Navbars/      # Barra de navegación
│   │   ├── Notifications/# Sistema de notificaciones
│   │   └── Sidebars/     # Sidebars por rol de usuario
│   ├── contexts/         # Contextos (AuthContext)
│   ├── guards/           # Guards de rutas y roles
│   ├── hooks/            # Hooks personalizados
│   ├── layouts/          # Layouts por tipo de usuario
│   ├── pages/            # Páginas por rol
│   │   ├── Administrator/# Páginas de administrador
│   │   ├── Auth/         # Login y registro
│   │   ├── Cliente/      # Páginas de cliente
│   │   ├── Colaborador/  # Páginas de colaborador
│   │   └── Superadministrador/ # Páginas de superadmin
│   ├── routes/           # Configuración de rutas (AppRoutes.jsx)
│   ├── services/         # Servicios para API calls
│   ├── App.jsx           # Componente principal
│   └── main.jsx          # Punto de entrada
├── .gitignore
├── eslint.config.js
├── index.html
├── package.json
├── vite.config.js
└── README.md

## 👥 Roles del Sistema
- Super Administrador: Control total del sistema
- Administrador: Gestión de proyectos, tareas y usuarios
- Colaborador: Visualización y actualización de tareas asignadas
- Cliente: Seguimiento de proyectos y documentos

# 📝 Notas Importantes
- Asegúrate de que el backend esté ejecutándose antes de iniciar el frontend
- Configura correctamente las variables de entorno en ambos proyectos
- Los archivos subidos se almacenan en BACKEND/src/uploads/documents/
- Verifica los permisos de escritura en la carpeta uploads
