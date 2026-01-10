
> [!INFO] Metadatos
> * **Plataforma:** Microsoft Learn
> * **Estado:** #Completado 🟢
> * **Tipo:** Conceptual / Fundamentos


> [!NOTE] Alcance del Curso
> **Objetivo:** Entender QUÉ es posible con IA y sus ramas principales.
> **Enfoque:** Vocabulario técnico, capacidades diferenciadas y ética.

---

## 🧠 Diccionario Técnico (Conceptos Clave)

### 1. IA Generativa (Creatividad)
* **Definición:** Crea contenido *nuevo* (texto, código, imágenes) basado en modelos probabilísticos.
* **LLM (Large Language Model):** Generalistas, potentes, costosos. (Ej. GPT-4).
* **SLM (Small Language Model):** Específicos, más baratos, corren en local. *Ideal para Edge AI / Robots.*

### 2. Computer Vision (Ojos)
* **Clasificación de Imágenes:** Dice *qué* es la imagen. (Ej. "Es un perro").
* **Detección de Objetos:** Dice *dónde* está el objeto (Dibuja un recuadro). *Vital para tu SmartBot.*
* **Segmentación Semántica:** Dice qué *píxeles* exactos son el objeto. (Nivel avanzado).

### 3. Procesamiento de Lenguaje Natural - NLP (Entendimiento)
* **Extracción de Entidades:** Identifica nombres, lugares, empresas en un texto.
* **Análisis de Sentimiento:** Determina si un texto es positivo, negativo o neutro.
* **Clasificación de Texto:** Etiqueta documentos por categoría.

### 4. Voz (Oídos y Boca)
* **Reconocimiento (Speech-to-Text):** Transcribe audio a texto.
* **Síntesis (Text-to-Speech):** Lee texto en voz alta (generación de voz).

### 5. Minería de Conocimiento (Datos)
* **OCR (Reconocimiento Óptico de Caracteres):** Extrae texto de imágenes/papel.

---

## ⚖️ Los 6 Principios de IA Responsable
*Importante para cualquier despliegue que hagas.*

1.  **Equidad (Fairness):** Evitar sesgos en los datos (que no discrimine por raza/género).
2.  **Confiabilidad (Reliability):** Entender que la IA comete errores; no es infalible.
3.  **Privacidad:** Proteger los datos del usuario entrenados.
4.  **Inclusión:** Que sea accesible para todos (discapacitados visuales/auditivos).
5.  **Transparencia:** El usuario debe saber que habla con una IA y cómo funciona.
6.  **Responsabilidad (Accountability):** Debe haber gobernanza humana sobre la IA.

---

## 💡 Ideas de Aplicación (Conexión con Proyectos VITA)

### 🏛️ Para #Proyectos/DiosesisSDE  (Web & Datos)
* **OCR + Extracción:** Digitalizar actas de bautismo antiguas escaneadas automáticamente. ("Digitalización a gran escala").
* **Chatbot NLP:** Un bot simple en la web que responda horarios de misa (usando NLP básico, más barato que Generativa).

### 🤖 Para el #Proyectos/SmartBot 
* **Detección de Objetos (No Clasificación):** El robot necesita saber *dónde* está el obstáculo para esquivarlo, no solo saber que "hay una silla".
* **SLM (Small Models):** Investigar modelos pequeños que puedan correr en la Raspberry Pi del robot sin internet.

### 💰 Para #Finanzas  (New Princes)
* **Sentiment Analysis:** Automatizar lectura de noticias financieras para ver si el sentimiento sobre `NWL.MI` está cayendo antes de que baje el precio.
* **Extracción de Entidades:** Escanear informes anuales (PDFs) para extraer cifras clave automáticamente.

---

## ✅ Validación de Conocimiento (Quiz)
- [x] **IA Generativa:** Usa modelos de lenguaje para crear contenido original.
- [x] **Localizar animales en foto:** Es "Detección de Objetos" (porque necesita ubicación, no solo etiqueta).
- [x] **Leer correo en voz alta:** Es "Síntesis de voz" (Text-to-Speech).

[[Data Science]] 