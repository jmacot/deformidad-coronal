# 🦴 Knee Align — Analisis de Alineacion

Herramienta de analisis de alineacion coronal de rodilla basada en los algoritmos AKUMA (varo) y AKULA (valgo) de Ollivier et al. (KSSTA 2025). Planificacion preoperatoria completa para osteotomias.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![D3.js](https://img.shields.io/badge/D3.js-F9A03C?logo=d3.js&logoColor=white)
![pdfmake](https://img.shields.io/badge/pdfmake-PDF-red)
![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-grey)

---

## Acceso

> Acceso directo — no requiere autenticacion.

[Abrir la aplicacion](https://jmacot.github.io/knee-align/)

No requiere instalacion. Funciona en cualquier navegador, incluyendo movil y tablet.

---

## Funcionalidades

- **Analisis AKUMA/AKULA**: descomposicion de la deformidad (IAD%, EAD%, contribucion tibial y femoral)
- **Disclaimer AKULA** con desplegable explicativo para deformidades en valgo
- **Diagnostico diferencial**: HTO vs DFO vs DLO vs UKA segun parametros del paciente
- **Planificacion de correccion**: metodo Mikulicz y correccion Micicoi (α = (JLCA−2)/2)
- **Correccion osea real**: correccion total → efecto seesaw (partes blandas) → correccion osea real
- **Flechas didacticas**: mMPTA actual → (+X°) → mMPTA postop
- **Cuna tibial de Hernigou**: D × tan(α) con anchura tibial editable
- **Slope tibial posterior** (PPTA) segun variante quirurgica (MOWHTO/MCWHTO)
- **Recomendacion de placa** (3+3 vs 4+4 orificios) segun Ollivier et al. (OTSR 2024)
- **Tooltip de variante quirurgica** con implicaciones clinicas
- **Popover educativo** sobre efecto seesaw
- **Clasificacion CPAK** (MacDessi 2021)
- **Zonas de Feucht** para seleccion de objetivo HKA segun grado de artrosis (KL)
- **Visualizadores de rango interactivos** para cada parametro
- **Explicacion paso a paso** del razonamiento clinico
- **Stepper de progreso** visual (Analisis → Correccion)
- **Exportacion PDF** con pdfmake (informe preoperatorio completo)
- **Modo oscuro** con deteccion automatica
- **Estilos de impresion** optimizados (Ctrl+P)

---

## Como usar

1. Abre la aplicacion en el navegador
2. Introduce los **valores radiologicos** del paciente (mLDFA, mMPTA, JLCA, HKA)
3. Pulsa **Analizar** para obtener el diagnostico de alineacion
4. Revisa la **descomposicion** de la deformidad y el diagnostico diferencial
5. Consulta la **planificacion de correccion** con cuna, slope y placa recomendada
6. **Exporta el informe PDF** para documentar la planificacion preoperatoria

---

## Estructura del proyecto

```
knee-align/
├── index.html        ← aplicacion principal
├── icon.svg          ← icono de la app
├── .gitignore
├── LICENSE           ← MIT
└── README.md         ← este archivo
```

---

## Tecnologia

- **HTML5 + CSS3 + JavaScript vanilla** (Sistema B "Radiologia Glass")
- [D3.js](https://d3js.org/) para graficas de contribucion y visualizadores de rango (cargado por CDN con fallback)
- [pdfmake](http://pdfmake.org/) cargado de forma diferida para exportacion de informes PDF
- Tipografias: Source Serif 4 + Source Sans 3 + Source Code Pro (Google Fonts)
- Glassmorphism con `backdrop-filter`, mesh gradient animado de fondo y sky toggle CSS puro para modo oscuro
- Accesibilidad: skip link, focus-visible, smooth scroll, reduced-motion
- Sin frameworks, sin build tools, sin backend

---

## Referencias

- Ollivier et al. — AKUMA/AKULA algorithms (KSSTA 2025)
- Ollivier et al. — Plate recommendation (OTSR 2024)
- MacDessi et al. — CPAK classification (Bone Joint J 2021)
- Feucht et al. — HKA target zones (KSSTA 2024)
- Hernigou — Tibial wedge height formula

---

## Licencia

MIT
