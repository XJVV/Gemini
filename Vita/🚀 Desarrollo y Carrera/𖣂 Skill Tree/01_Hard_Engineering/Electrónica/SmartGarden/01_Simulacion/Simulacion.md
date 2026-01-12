# 💻 Entorno de Simulación (Gemelo Digital)

**Propósito:** Espacio de trabajo para el código Python que corre en el PC, no en el microcontrolador. Aquí "jugamos a ser Dios" simulando el clima y el huerto.

### Contenido Típico:
* **`sim_env.py`**: El script principal que simula la física de la caja (calor, humedad, batería).
* **`generador_datos.py`**: Script para correr la simulación mil veces y generar CSVs.
* **`/datasets`**: Carpeta para guardar los `.csv` generados (e.g., `entrenamiento_v1.csv`).

### Flujo de Trabajo:
1.  Modificar parámetros en `sim_env.py`.
2.  Ejecutar para generar datos.
3.  Usar datos en la fase de entrenamiento.
[[🌿 SmartGarden]]