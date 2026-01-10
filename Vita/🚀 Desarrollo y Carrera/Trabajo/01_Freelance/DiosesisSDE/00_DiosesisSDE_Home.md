# 🌍 #Proyectos/DiosesisSDE : Sistema de Gestión Pastoral

> [!WARNING] Estado Actual: 🟡 En Proceso (Esperando Datos)
> * **Cliente:** Diócesis Local
> * **Tech Stack:** React + Node.js + MySQL
> * **Bloqueo Actual:** Esperando archivo Excel oficial con el censo real de parroquias/sacerdotes.

## 📌 Visión General
Plataforma web Full Stack para geolocalización de parroquias. El sistema está funcional a nivel de código (`v1.0`), pero la base de datos opera actualmente con **Mock Data** (datos de prueba) a la espera de la migración final.

## 📂 Documentación del Sistema
* [[01_Arquitectura Técnica]] -> Cómo funciona el código.
* [[02_Base de Datos]] -> Estructura SQL (Tablas y Relaciones).
* [[03_Manual de Despliegue]] -> Guía para servidor VPS.

## 📋 Lista de Tareas Pendientes (ToDo)
- [x] Desarrollo Frontend (Mapa e Interfaz).
- [x] Desarrollo Backend (API REST).
- [x] Diseño de Base de Datos Relacional.
- [ ] **MIGRACIÓN DE DATOS:**
    - [ ] Recibir Excel del cliente.
    - [ ] Crear script de conversión (Excel -> SQL INSERTs).
    - [ ] Limpiar/Normalizar datos (nombres mal escritos, coordenadas faltantes).
    - [ ] Poblar base de datos de Producción.
- [ ] Despliegue final en servidor.

## 💡 Notas para la Migración
Cuando llegue el Excel, recordar:
1.  Verificar que las coordenadas (`lat`, `long`) vengan en formato decimal.
2.  Asegurar que los nombres de `Sectores` coincidan exactamente con los IDs de la base de datos para no romper las relaciones.
[[01_Freelance]]