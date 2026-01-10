> [!INFO] Metadatos
> * **Plataforma:** Microsoft Learn (Azure AI Foundry)
> * **Estado:** #Completado 🟢
> * **Tema Central:** LLMs, RAG y Agentes Autónomos.

> [!NOTE] La Gran Idea
> "La IA Generativa no es magia, es estadística."
> No entiende lo que dice; predice la siguiente palabra (token) basándose en probabilidades matemáticas (Vectores).

---

## 🧠 Diccionario Técnico (Ingeniería de LLMs)

### 1. El Motor (Cómo funciona)
* **Tokenización:** El LLM no lee palabras, lee números. Rompe el texto en *Tokens* (palabras o sílabas).
* **Embeddings (Incrustaciones):** Convierte tokens en *Vectores* numéricos (listas de coordenadas).
    * *Clave:* Palabras con significados similares ("Perro" y "Cachorro") tienen vectores matemáticamente cercanos.
* **Transformer:** La arquitectura neuronal que hace posible todo esto. Usa **Atención** para saber qué palabras son importantes en el contexto (ej. relaciona "Ladrido" con "Perro" aunque estén lejos en la frase).

### 2. Prompt Engineering (Control)
* **System Prompt (Instrucción del Sistema):** Define el *Rol* y las *Reglas*. (Ej: "Eres un experto financiero cínico").
* **User Prompt:** La pregunta o tarea actual.

### 3. Técnicas Avanzadas (Lo vital para mis proyectos)
* **RAG (Generación Aumentada por Recuperación):**
    * *Problema:* El LLM alucina o no conoce mis datos privados.
    * *Solución:* Le inyecto documentos reales (PDFs, Excels) en el contexto antes de que responda. "Responde usando SOLO este archivo".
* **Agentes de IA:**
    * *Definición:* LLM + Instrucciones + **Herramientas**.
    * *Diferencia:* Un Chatbot *habla*. Un Agente *actúa* (envía emails, busca en SQL, reserva vuelos).

---

## 💡 Ideas de Aplicación (Proyectos VITA)

### 🤖 Para el #Proyectos/SmartBot  (Agentes)
* **Concepto:** En lugar de programar `if obstaculo then girar`, crear un Agente.
* **Herramientas:** Darle al Agente control sobre los motores.
* **Prompt:** "Tu objetivo es llegar a X sin chocar. Tienes herramientas para 'Ver' y 'Moverte'. Úsalas."

### 💰 Para #Finanzas  (New Princes - RAG)
* **Sistema RAG Financiero:**
    * Cargar los PDFs anuales de *New Princes Group* en un vector store.
    * Preguntar: "¿Cuál fue el flujo de caja libre en 2024 según la página 40?"
    * *Resultado:* Respuesta exacta basada en datos, cero alucinaciones.

### 🏛️ Para la Diócesis (Agente Administrativo)
* **Agente de Gastos:** Igual que en el ejercicio del curso.
* **System Prompt:** "Eres un contable estricto. Revisa si la solicitud de gasto cumple las normas del PDF 'Política Parroquial 2025'."

---

## ✅ Validación de Conocimiento (Quiz)
*Respuestas correctas del módulo:*

- [x] **LLM:** Un tipo de modelo de IA diseñado para generar texto similar al humano.
- [x] **Tokenización:** Para dividir el texto en unidades más pequeñas.
- [x] **Embeddings:** Representaciones basadas en vectores que capturan significado semántico.
- [x] **Capa de Atención:** Examina las relaciones entre cada token y los que lo rodean (Contexto).
- [x] **System Prompt:** Proporcionar contexto, tono e instrucciones al modelo.
- [x] **Agente:** Un sistema de IA que puede realizar tareas (usar herramientas) en nombre de un usuario.

[[Data Science]]
