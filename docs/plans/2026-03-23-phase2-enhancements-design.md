# Phase 2 Enhancements — Design

## Features

### 1. SVG Eje Mecanico reutilizable (`renderMechAxis`)
- Esquema frontal: lineas femur + tibia + linea articular + eje mecanico
- viewBox 200x400, responsive
- Dos modos: visualizacion (preop+postop superpuestos) y Miniaci (interactivo)
- Preop: trazo discontinuo rojo/azul. Postop: trazo solido verde
- Arcos de angulo con labels mLDFA, mMPTA

### 2. Miniaci interactivo
- Toggle segmentado iOS `[Feucht] [Miniaci]` dentro de correction-card
- Ambos escriben en `#inp-target`
- Click en tibia para fulcrum (marcador naranja) + drag para angulo correccion
- Inputs numericos como fallback (fulcrum % + angulo)
- Chip resultado debajo del SVG

### 3. Simulacion before/after
- Mismo SVG en modo visualizacion tras calcular correccion
- Eje preop punteado + eje postop solido verde
- Se renderiza automaticamente al calcular Phase 2

### 4. Comparador 2 escenarios
- Dos SVGs lado a lado (grid 1fr 1fr, stack en movil)
- Escenario A = planificacion actual (auto-rellenado)
- Escenario B = input manual de HKA alternativo
- Tabla comparativa: mMPTA, mLDFA, JLO, cuna, slope, warnings

## Arquitectura
- Enfoque A: SVG unico reutilizable para todo
- Ubicacion: dentro de Phase 2 actual
- Sin dependencias nuevas (D3 ya disponible, fallback CSS existente)
