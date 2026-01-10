

> [!INFO] Resumen
> Robot móvil autónomo diseñado para la navegación en entornos desconocidos. Utiliza sensores ultrasónicos para detectar obstáculos y un algoritmo de conteo de vueltas para tomar decisiones de evasión complejas (no solo reactivas).

## 🛠️ Tech Stack (Hardware & Software)
* **Microcontrolador:** Arduino / ESP32.
* **Sensores:** Sensor de distancia Ultrasónico (HC-SR04).
* **Actuadores:** Motores DC con caja reductora + Driver L298N (Puente H).
* **Alimentación:** Baterías Li-ion 18650.
* **Lenguaje:** C++ (Arduino IDE).

---

## 🧠 Lógica de Control (Máquina de Estados)
*Basado en el diagrama de flujo del diseño original.*

### 1. Ciclo Principal (Loop)
1.  **Lectura:** El sensor mide la distancia (`SD`).
2.  **Decisión Simple:**
    * Si `SD >= 10cm`: **Avanza** (El camino está libre).
    * Si `SD < 10cm`: **Detenerse** (Obstáculo detectado).

### 2. Algoritmo de Evasión (Lógica de "NVueltas")
El robot cuenta cuántas veces ha tenido que girar recientemente para no quedarse atrapado en esquinas.

* **Contador:** Cada vez que encuentra un obstáculo, `NVueltas = NVueltas + 1`.
* **Caso A (Primeros intentos):** Si `NVueltas < 2`, hace un giro estándar de **90°**.
* **Caso B (Atasco moderado):** Si `NVueltas >= 2`, asume que es una esquina cerrada y gira **180°** (media vuelta).
* **Caso C (Atasco crítico):** Si `NVueltas >= 3`, ejecuta maniobra de escape girando **270°** y reinicia el contador.

---

## 📝 Aprendizajes Clave
* **Control de Motores:** Aprendí a usar el driver L298N para controlar no solo el encendido/apagado, sino la dirección de giro mediante la inversión de polaridad.
* **Lógica No Bloqueante:** Implementación de contadores de estado (`NVueltas`) para que el robot tenga una especie de "memoria a corto plazo" y no repita el mismo error infinitamente.
* **Mecánica:** Importancia de la tracción diferencial (tank drive) para girar sobre su propio eje.

## 🔗 Recursos y Código
* **Repositorio:** https://github.com/XJVV/Julio-Mechatronics-Projects.git 
* **Diagrama Original:** [[Diagrama de flujo.drawio]] 
 [[Electrónica]] #Proyectos/SmartBot 