# 🌍 Agencia de Viajes - Travel Agency

Una aplicación web moderna para una agencia de viajes construida con Node.js, Express y MySQL. Esta aplicación completa incluye tanto backend robusto como frontend dinámico, permitiendo a los usuarios explorar destinos, ver detalles de viajes y enviar testimoniales a través de una interfaz intuitiva.

## 🚀 Características

- **Aplicación Full-Stack**: Backend robusto con frontend integrado
- **Catálogo de Viajes**: Visualización de destinos disponibles con información detallada
- **Sistema de Testimoniales**: Los usuarios pueden compartir sus experiencias
- **Arquitectura MVC**: Separación clara entre Modelo, Vista y Controlador
- **Diseño Responsivo**: Interfaz moderna y adaptable a diferentes dispositivos
- **Base de Datos Relacional**: Gestión eficiente de datos con MySQL y Sequelize ORM
- **Server-Side Rendering**: Renderizado dinámico del lado del servidor con Pug
- **API RESTful**: Endpoints estructurados para gestión de datos

## 🛠️ Stack Tecnológico

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Base de Datos**: MySQL
- **ORM**: Sequelize
- **Variables de Entorno**: dotenv

### Frontend
- **Motor de Plantillas**: Pug (Server-Side Rendering)
- **Estilos**: CSS3, Bootstrap
- **Arquitectura**: MVC Pattern

### Herramientas de Desarrollo
- **Dev Server**: Nodemon
- **Package Manager**: npm

## 📋 Prerrequisitos

Antes de ejecutar este proyecto, asegúrate de tener instalado:

- [Node.js](https://nodejs.org/) (versión 14 o superior)
- [MySQL](https://www.mysql.com/) (versión 5.7 o superior)
- [npm](https://www.npmjs.com/) o [yarn](https://yarnpkg.com/)

## ⚙️ Instalación

1. **Clona el repositorio**
   ```bash
   git clone [URL-del-repositorio]
   cd 25-NODEJS
   ```

2. **Instala las dependencias**
   ```bash
   npm install
   ```

3. **Configura las variables de entorno**
   
   Crea un archivo `.env` en la raíz del proyecto:
   ```env
   DB_URL=mysql://usuario:contraseña@localhost:3306/agenciaviajes
   PORT=3000
   ```

4. **Configura la base de datos**
   
   Importa el archivo de base de datos proporcionado:
   ```bash
   mysql -u tu_usuario -p agenciaviajes < agenciaviajes.dump
   ```

5. **Inicia el servidor**
   
   Para desarrollo:
   ```bash
   npm run dev
   ```
   
   Para producción:
   ```bash
   npm start
   ```

6. **Accede a la aplicación**
   
   Abre tu navegador y ve a `http://localhost:3000`

## 📁 Estructura del Proyecto

```
25-NODEJS/
├── config/
│   └── db.js                 # Configuración de la base de datos
├── controllers/
│   ├── paginasController.js  # Controlador de páginas principales
│   └── testimonialesController.js # Controlador de testimoniales
├── models/
│   ├── Testimonial.js        # Modelo de testimoniales
│   └── Viaje.js             # Modelo de viajes
├── public/
│   ├── css/                 # Archivos de estilos
│   └── img/                 # Imágenes y recursos
├── routes/
│   └── index.js             # Definición de rutas
├── views/
│   ├── layout/              # Plantillas base
│   ├── inicio.pug           # Página de inicio
│   ├── viajes.pug           # Listado de viajes
│   ├── viaje.pug            # Detalle de viaje
│   ├── testimoniales.pug    # Página de testimoniales
│   └── nosotros.pug         # Página sobre nosotros
├── agenciaviajes.dump       # Archivo de base de datos
├── index.js                 # Archivo principal de la aplicación
└── package.json             # Dependencias y scripts
```

## 🗃️ Esquema de Base de Datos

### Tabla: `viajes`
- `id` (bigint, PK): Identificador único del viaje
- `titulo` (varchar): Nombre del destino
- `precio` (varchar): Precio del viaje
- `fecha_ida` (date): Fecha de salida
- `fecha_vuelta` (date): Fecha de regreso
- `imagen` (varchar): Nombre del archivo de imagen
- `descripcion` (text): Descripción detallada del viaje
- `disponibles` (int): Plazas disponibles
- `slug` (varchar): URL amigable

### Tabla: `testimoniales`
- `id` (int, PK, AI): Identificador único
- `nombre` (varchar): Nombre del cliente
- `correo` (varchar): Email del cliente
- `mensaje` (text): Testimonial del cliente

## 🌐 Rutas de la Aplicación

- `/` - Página de inicio
- `/nosotros` - Información sobre la agencia
- `/viajes` - Catálogo de viajes disponibles
- `/viajes/:slug` - Detalle de un viaje específico
- `/testimoniales` - Testimoniales de clientes

## 🤝 Contribución

1. Fork el proyecto
2. Crea una rama para tu característica (`git checkout -b feature/AmazingFeature`)
3. Confirma tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Sube a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia ISC. Ver el archivo `LICENSE` para más detalles.

## 👨‍💻 Autor

**David AGR**

## 📞 Contacto

Si tienes alguna pregunta o sugerencia, no dudes en contactarme.

---

⭐ ¡No olvides dar una estrella al proyecto si te ha sido útil!
