# ⚙️ Arquitectura Técnica (DiosesisSDE)

## 🖥️ Frontend (Cliente)
Construido con **Vite + React**.
* **Entrada:** `src/main.jsx` monta la app en el DOM.
* **Estilos:** TailwindCSS configurado en `tailwind.config.js` y `postcss.config.js`.
* **Componente Principal:** `App.jsx` gestiona la carga del mapa y la interfaz de usuario.
* **Assets:** Iconos SVG en `src/assets/` y `public/`.

## 🔌 Backend (API REST)
Servidor en **Node.js + Express** (`backend/server.js`).

### Estructura del Servidor
* **Puerto:** Por defecto `3000` (Configurable en `.env`).
* **Seguridad:** Uso de `cors` para permitir peticiones desde el dominio del frontend.
* **Conexión DB:** Utiliza driver `mysql2` o similar para conectar con la base de datos `diocesis_sde`.

### Endpoints Principales (Ejemplos)
* `GET /api/vicarias` -> Obtiene la lista de zonas mayores.
* `GET /api/parroquias` -> Devuelve JSON con lat/long para el mapa.
* `GET /api/sacerdotes` -> Lista el clero disponible.

> [!WARNING] Nota de Desarrollo
> El proyecto utiliza `ESLint` para mantener la calidad del código. Ejecutar `npm run lint` antes de cada commit.


[[00_DiosesisSDE_Home]]