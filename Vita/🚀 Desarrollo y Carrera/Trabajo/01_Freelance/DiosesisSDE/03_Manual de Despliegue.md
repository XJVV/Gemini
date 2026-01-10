# 🚀 Manual de Despliegue y Configuración

> [!TIP] Objetivo
> Guía para llevar el proyecto de "Localhost" a un Servidor de Producción (Ubuntu/DigitalOcean/AWS).

## 1. Requisitos del Servidor
* **Node.js:** v18 o superior.
* **Base de Datos:** MySQL o MariaDB.
* **Process Manager:** PM2 (Para mantener el backend vivo).
* **Web Server:** Nginx (Proxy inverso).

## 2. Variables de Entorno (.env)
Crear un archivo `.env` en la carpeta `backend/` con las credenciales reales de producción:

```bash
PORT=3000
DB_HOST=localhost
DB_USER=usuario_prod
DB_PASS=contraseña_segura_prod
DB_NAME=diocesis_sde
[[00_DiosesisSDE_Home]]