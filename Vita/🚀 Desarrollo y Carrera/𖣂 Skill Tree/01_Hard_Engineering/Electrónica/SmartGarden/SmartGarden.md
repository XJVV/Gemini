# 🌿 Proyecto: AI Core - Minihuerto Autónomo

**Estado:** #En_Progreso
**Tags:** #Mechatronics #TinyML #Python #Simulation #EmbeddedAI
**Fecha de Inicio:** 2026-01-10
**Meta:** Diseñar y validar la lógica de control y la IA en un entorno simulado antes del hardware.

---

## 📅 Fase 1: Fundamentos y Parametrización Agronómica
*Objetivo: Definir las "Reglas del Juego" y el "Ground Truth" para la IA.*

- [ ] **Definición de Perfiles de Cultivo (Dataset Maestro)**
    - Crear una tabla/JSON con rangos óptimos (Min/Max/Ideal) para:
        - [[Perfil_Tomate_Cherry]]
        - [[Perfil_Lechuga]]
        - [[Perfil_Albahaca]]
    - *Variables a definir:* Temp ($^\circ C$), Humedad Relativa (%), Humedad Suelo (%), PAR/DLI (Luz).
- [ ] **Modelado Matemático del Entorno (Física Básica)**
    - Investigar y anotar fórmulas para la simulación térmica:
        - [[Ecuacion_Perdida_Calor]] (¿Qué tan rápido se enfría la caja sin calefacción?)
        - [[Ecuacion_Evapotranspiracion]] (¿Qué tan rápido se seca el suelo según la Temp?)
- [ ] **Modelo de Energía Solar**
    - Definir curva de generación solar teórica (06:00 a 18:00).
    - Definir capacidad de batería y consumo de actuadores (W/h).

---

## 💻 Fase 2: El Gemelo Digital (Python Simulation)
*Objetivo: Crear un script en Python que genere datos sintéticos para entrenar la IA.*

- [ ] **Configuración del Entorno de Desarrollo**
    - Configurar entorno virtual `venv` en Linux.
    - Librerías clave: `pandas`, `numpy`, `scikit-learn`.
- [ ] **Desarrollo del Simulador de Ambiente (`sim_env.py`)**
    - [ ] Programar clase `Greenhouse`:
        - Inputs: Estado de actuadores (Bomba ON/OFF, Luz ON/OFF).
        - Outputs: Nuevos valores de sensores ($T+1$, $H+1$).
    - [ ] Implementar "Ruido de Sensores" (Gaussian noise) para realismo.
- [ ] **Generación de Dataset Sintético**
    - Correr la simulación por "30 días virtuales".
    - Exportar datos a `.csv`: `timestamp, temp, hum_suelo, luz, bateria, accion_tomada, resultado_cultivo`.

---

## 🧠 Fase 3: TinyML & Entrenamiento de Modelos
*Objetivo: Crear el cerebro que predice y clasifica, optimizado para microcontroladores.*

- [ ] **Pre-procesamiento de Datos**
    - Normalización de datos (escala 0 a 1 para redes neuronales).
    - [[Feature_Engineering]]: Crear variables como "Tendencia de Temperatura" (¿Sube o baja?).
- [ ] **Modelo 1: Predicción de Recursos (Regresión)**
    - *Input:* Hora del día + Nivel de Batería + Luz Actual.
    - *Output:* Predicción de "Energía Disponible en 4 horas".
    - *Herramienta:* TensorFlow / Keras (exportar a TFLite).
- [ ] **Modelo 2: Detección de Anomalías (Autoencoder)**
    - Entrenar modelo para reconocer "Funcionamiento Normal".
    - Si el error de reconstrucción es alto -> ¡Alerta! (Sensor roto o puerta abierta).

---

## ⚙️ Fase 4: Lógica de Control y Gestión Energética
*Objetivo: El sistema de toma de decisiones (El "Árbitro").*

- [ ] **Diseño de Máquina de Estados Finitos (FSM)**
    - Definir estados en [[Diagrama_Estados]]:
        - `IDLE` (Reposo/Ahorro)
        - `ACTIVE_GROWTH` (Condiciones ideales)
        - `CRITICAL_BATTERY` (Modo supervivencia)
        - `EMERGENCY` (Fallo de sensores)
- [ ] **Algoritmo de Priorización Energética**
    - Implementar lógica de costes:
    $$Costo = (w_1 \cdot DesviaciónCultivo) + (w_2 \cdot GastoBateria)$$
    - Si Batería < 30%, $w_2$ aumenta drásticamente (ahorrar es más importante que crecer).
- [ ] **Fuzzy Logic Controller (Opcional pero recomendado)**
    - Mapear variables difusas: "Si hace *un poco de calor* y hay *mucha batería* -> *Ventilador Medio*".

---

## 📦 Fase 5: Validación y Preparación para Hardware
*Objetivo: Asegurar que el código es portable a C++/Arduino.*

- [ ] **Conversión a C++**
    - Convertir modelos `.h5` a Arrays de C (usando `xxd` o herramientas de TFLite Micro).
- [ ] **Selección de Hardware Teórico**
    - [[Seleccion_Microcontrolador]]: (e.g., ESP32-S3 o Arduino Portenta H7).
    - [[Sensores_Actuadores]]: Lista de BOM (Bill of Materials).
- [ ] **Prueba de "Hardware-in-the-Loop" Simulado**
    - Ejecutar el código C++ en el PC recibiendo datos del script de Python (simulando comunicación Serial).

---

## 📝 Notas y Recursos
* Enlace a documentación de TensorFlow Lite Micro.
* Enlace a repositorios de simulación de invernaderos.
[[01_Hard_Engineering]]