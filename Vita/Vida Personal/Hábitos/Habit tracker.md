### Últimos 7 días   
```dataview
TABLE WITHOUT ID
  link(file.link, file.name) as "Fecha",
  choice(Leer, "📘", "❌") as "Leer",
  choice(Ejercicio, "💪", "❌") as "Ejercicio",
  choice(NoFap, "🛡️", "❌") as "NoFap"
FROM "Vita/Vida Personal/Hábitos/Dias"
WHERE file.name != "Plantillas"
SORT file.name DESC
LIMIT 7
```




---

### 🟢 Ejercicio
```tracker
searchType: frontmatter
searchTarget: Ejercicio
folder: Vita/Vida Personal/Hábitos/Dias
datasetName: Ejercicio
startDate: 2025-12-01
endDate: 2026-12-31
month:
    startWeekOn: 'Mon'
    color: '#40a02b'
    headerMonthColor: '#40a02b'
    todayRingColor: '#40a02b'
    selectedRingColor: '#40a02b'
    showSelectedValue: false
summary:
    template: "🔥 Racha: {{currentStreak()}} días  |  🏆 Máxima: {{maxStreak()}} días"
    style: "color: #40a02b; font-weight: bold;"
```

### 🔵 Lectura
```tracker
searchType: frontmatter
searchTarget: Leer
folder: Vita/Vida Personal/Hábitos/Dias
datasetName: Leer
startDate: 2025-12-01
endDate: 2026-12-31
month:
    startWeekOn: 'Mon'
    color: '#1e66f5'
    headerMonthColor: '#1e66f5'
    todayRingColor: '#1e66f5'
    selectedRingColor: '#1e66f5'
    showSelectedValue: false
summary:
    template: "🔥 Racha: {{currentStreak()}} días  |  🏆 Máxima: {{maxStreak()}} días"
    style: "color: #1e66f5; font-weight: bold;"
```

### 🟣 NoFap
```tracker
searchType: frontmatter
searchTarget: NoFap
folder: Vita/Vida Personal/Hábitos/Dias
datasetName: NoFap
startDate: 2025-12-01
endDate: 2026-12-31
month:
    startWeekOn: 'Mon'
    color: '#8839ef'
    headerMonthColor: '#8839ef'
    todayRingColor: '#8839ef'
    selectedRingColor: '#8839ef'
    showSelectedValue: false
summary:
    template: "🔥 Racha: {{currentStreak()}} días  |  🏆 Máxima: {{maxStreak()}} días"
    style: "color: #8839ef; font-weight: bold;"
```
[[Vida Personal]] 
[[Dashboard Hábitos.canvas|Dashboard Hábitos]]
