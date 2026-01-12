# 🧠 Modelos de IA (Model Zoo)

**Propósito:** Almacenamiento de los modelos entrenados y sus metadatos. Control de versiones de tu "cerebro".

### Estructura de Archivos:
* **`.h5` / `.keras`**: Modelos completos de TensorFlow (pesos + arquitectura) para guardar progresos.
* **`.tflite`**: Modelos cuantizados y optimizados para TinyML (Lite).
* **`.cc` / `.h`**: Los modelos convertidos a Arrays de C++ listos para copiar al microcontrolador.

### Nomenclatura Recomendada:
Usa el formato: `[TipoModelo]_[Version]_[Fecha].ext`
* Ejemplo: `PrediccionEnergia_v2_20260110.tflite`

[[🌿 SmartGarden]]