## 🧠 Ramas Principales

### 🛡️ [[00_Core_Management]]
*Habilidades blandas, productividad y gestión.*
* [[Soft Skills]] | [[Productividad y Hábitos]]

### ⚡ [[01_Hard_Engineering]]
*Habilidades técnicas duras.*
* [[Data Science]] | [[Electrónica]]

### 📊 [[03_Financial_Analytics]]
*Análisis financiero y valoración.*
* [[Valoración]] | [[Contabilidad]]

## 🌱 Habilidades Activas (Mapa Limpio)
*Muestra solo las notas principales de cada habilidad.*

```dataview
TABLE file.folder as "Rama", file.mtime as "Último Repaso"
FROM "Vita/🚀 Desarrollo y Carrera/𖣂 Skill Tree"
WHERE file.name != this.file.name 
AND contains(file.name, regexreplace(file.folder, ".*\/", ""))
SORT file.folder ASC
```


[[🚀 Desarrollo y Carrera]]
