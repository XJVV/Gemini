# 🗃️ Esquema de Base de Datos

**Motor:** MySQL / MariaDB (`utf8mb4`)
**Archivo Fuente:** `backend/database.sql`
**Base de Datos:** `diocesis_sde`

## 📊 Tablas Principales

### 1. Estructura Jerárquica (Territorial)
La diócesis se organiza en niveles anidados:
* **`vicarias`**: Las grandes zonas (Ej. "Vicaría I - Villa Duarte").
    * *Campo Clave:* `color` (Hexadecimal, ej: `#89a7b1`) para diferenciar zonas en el mapa.
    * *Campo Clave:* `slug` para URLs amigables.
* **`sectores`**: Subdivisiones geográficas dentro de una Vicaría.
    * Relación: `vicaria_id` (Foreign Key).

### 2. `parroquias` (Tabla Central)
El punto físico final en el mapa.

```sql
CREATE TABLE parroquias (
  id INT PRIMARY KEY AUTO_INCREMENT,
  nombre VARCHAR(255),
  sector_id INT, -- Pertenece a un Sector
  sacerdote_id INT, -- Cura encargado
  latitud DECIMAL(10, 8), -- Coordenadas Mapa
  longitud DECIMAL(11, 8),
  imagen_url TEXT,
  FOREIGN KEY (sector_id) REFERENCES sectores(id)
);

[[00_DiosesisSDE_Home]]