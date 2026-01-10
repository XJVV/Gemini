> [!INFO] Metadatos
> * **Plataforma:** Microsoft Learn (Azure)
> * **Estado:** #Completado 🟢
> * **Tema:** Fundamentos de Nube (AZ-900 Parte 1)


> [!NOTE] La Gran Idea
> "La nube no es más que el ordenador de otro."
> La clave no es la tecnología, es el modelo económico: Dejamos de comprar servidores (Activos Fijos) para alquilar servicios (Gastos Operativos).

---

## 🧠 Conceptos Clave (Diccionario Cloud)

### 1. Modelos Económicos (Crucial para Inversión y Negocios)
* **CapEx (Gastos de Capital):** Gasto por adelantado. Comprar el servidor físico, el edificio, el aire acondicionado.
    * *Problema:* Si compras de más, tiras dinero. Si compras de menos, te quedas sin servicio.
* **OpEx (Gastos Operativos):** Gasto recurrente (pago por uso). Alquilar la nube.
    * *Ventaja:* Escalas según demanda. No hay costo inicial. **Mejora el Cash Flow.**

### 2. Modelos de Nube
* **Nube Pública:** Multitenant (compartes hardware con otros, pero tus datos están aislados). Ej: Azure, AWS.
* **Nube Privada:** Un centro de datos dedicado solo a ti. (Más control, más caro).
* **Nube Híbrida:** Conectar tu servidor local con la nube pública. (Lo mejor de ambos mundos).

### 3. Modelo de Responsabilidad Compartida
* *¿De quién es la culpa si hackean el sistema?*
* **On-Premise (Tu servidor):** Tú eres responsable de TODO (desde la seguridad física hasta los datos).
* **IaaS (Infraestructura):** Azure pone el hardware, tú pones el SO y las Apps. (Mayor responsabilidad para ti).
* **PaaS (Plataforma):** Azure pone el hardware y el SO, tú solo pones la App y los Datos. (Equilibrado).
* **SaaS (Software):** Azure hace casi todo. Tú solo configuras usuarios y datos. (Ej. Microsoft 365).

---

## 💡 Ideas de Aplicación (Proyectos VITA)

### 💰 Para mis #Finanzas  (Análisis Fundamental)
* **Análisis de Empresas:** Cuando analice empresas tecnológicas (como *Vertiv* o *New Princes*), debo fijarme si están gastando en CapEx (construyendo data centers) o migrando a OpEx.
* **Azure Arc & VMware:** Entender que Azure permite gestionar nubes híbridas explica por qué Microsoft sigue creciendo en empresas antiguas que no pueden migrar todo al 100%.

### 🏛️ Para el #Proyectos/DiosesisSDE  (Freelance)
* **Elección de Modelo:** Para la web de la Diócesis, no debo usar una VM (IaaS) porque tendría que mantener el Windows/Linux actualizado.
* **Mejor opción:** Usar **PaaS** (Azure App Service) o **SaaS** (Si hay una solución hecha). Solo me preocupo del código y la base de datos, no del servidor.
* **Costo:** Al ser OpEx, la Diócesis no paga $5,000 por un servidor, paga $20/mes.

### 🤖 Para el #Proyectos/SmartBot 
* **Escalabilidad:** El robot (Edge) puede enviar datos a la nube. Si fabrico 1000 robots, la nube escala sola (Elasticidad) sin que yo tenga que comprar hardware nuevo.

---

## ✅ Validación de Conocimiento (Quiz)
*Respuestas correctas del módulo:*

- [x] **¿Qué es informática en la nube?:** Brindar servicios informáticos a través de Internet.
- [x] **Modelo Público + Privado:** Nube híbrida.
- [x] **Mayor responsabilidad para el cliente:** Infraestructura como servicio (IaaS).

[[Data Science]]