# CRISP-Agile Project Tracker

Herramienta web para gestionar proyectos de ciencia de datos combinando **CRISP-DM** como marco metodológico y prácticas **Agile** para la ejecución iterativa del proyecto.

El tracker fue desarrollado inicialmente para el proyecto académico realizado por **Atlantic Data Consulting** con **Danu Analítica**, pero su estructura está diseñada para poder reutilizarse en futuros proyectos de analítica, Machine Learning, Business Intelligence e Inteligencia Artificial.

---

## Objetivo del repositorio

Centralizar el seguimiento del proyecto de ciencia de datos de Danu Analítica en una sola herramienta que permita:

- Dar seguimiento a las seis fases de CRISP-DM.
- Organizar el trabajo mediante backlog y sprints.
- Visualizar el avance general del proyecto.
- Asignar responsables a actividades.
- Registrar KPIs, riesgos y entregables.
- Mantener evidencia de decisiones, hallazgos y retrospectivas.
- Facilitar la trazabilidad entre el problema de negocio, los datos, el modelado y los entregables finales.

> **CRISP-DM define qué tipo de trabajo se está realizando y Agile define cómo se ejecuta ese trabajo.**

---

# Contexto del proyecto

Danu Analítica trabaja con soluciones relacionadas con datos, Business Intelligence, infraestructura de datos, Machine Learning e Inteligencia Artificial.

Dentro del reto académico, el equipo **Atlantic Data Consulting** desarrolla un proyecto de ciencia de datos siguiendo un proceso estructurado que permita transformar una necesidad de negocio en una solución basada en datos.

## Objetivo general

Convertir una necesidad de negocio en una solución de datos **medible, validada y desplegable**, utilizando CRISP-DM como metodología principal y Agile como modelo de ejecución iterativa.

---

# Metodología

## CRISP-DM

El proyecto utiliza las seis fases de **Cross-Industry Standard Process for Data Mining (CRISP-DM)**:

### 1. Business Understanding

Comprensión del problema y del contexto de negocio.

Incluye:
- definición del problema;
- objetivos;
- stakeholders;
- alcance;
- recursos;
- restricciones;
- requerimientos;
- criterios de éxito;
- beneficios esperados para Danu Analítica.

### 2. Data Understanding

Exploración y comprensión de las fuentes de datos.

Incluye:
- identificación de fuentes;
- acceso a datos;
- descripción del dataset;
- diccionario de datos;
- análisis exploratorio;
- evaluación de calidad;
- valores faltantes;
- duplicados;
- outliers;
- relaciones y patrones preliminares.

### 3. Data Preparation

Construcción del dataset final para análisis o modelado.

Incluye:
- limpieza;
- integración;
- transformación;
- normalización;
- selección de variables;
- feature engineering;
- tratamiento de valores faltantes.

### 4. Modeling

Construcción y comparación de soluciones analíticas o modelos.

Puede incluir:
- modelo baseline;
- selección de algoritmos;
- entrenamiento;
- validación;
- comparación de modelos;
- ajuste de hiperparámetros;
- experimentación.

### 5. Evaluation

Evaluación de los resultados desde dos perspectivas.

**Técnica**
- desempeño del modelo;
- métricas;
- estabilidad;
- calidad de predicción.

**Negocio**
- utilidad para Danu;
- alineación con el problema original;
- cumplimiento de criterios de éxito;
- aplicabilidad del resultado.

### 6. Deployment

Entrega y uso de la solución.

Puede incluir:
- dashboard;
- reporte;
- modelo;
- pipeline;
- API;
- automatización;
- documentación;
- recomendaciones;
- estrategia de mantenimiento.

---

# Integración CRISP-DM + Agile

CRISP-DM no se utiliza como un proceso estrictamente lineal.

```text
Backlog
   ↓
Sprint Planning
   ↓
Sprint
   ↓
Entrega parcial
   ↓
Sprint Review
   ↓
Retroalimentación
   ↓
Retrospectiva
   ↓
Siguiente iteración
```

Durante una iteración es posible regresar a cualquier fase de CRISP-DM.

```text
Data Understanding
        ↓
Data Preparation
        ↓
Modeling
        ↓
Evaluation
        ↓
Se descubre un problema
        ↓
Data Understanding
```

---

# Funcionalidades del tracker

La aplicación actual incluye:

## Dashboard
- avance global;
- fase CRISP-DM actual;
- sprint activo;
- riesgos abiertos;
- progreso por fase;
- distribución de tareas;
- próximas tareas;
- decisiones y evidencias recientes.

## CRISP-DM
Para cada fase se puede registrar:
- estado;
- porcentaje de avance;
- tareas relacionadas;
- Definition of Done;
- notas;
- entregables.

## Agile / Sprints
Cada sprint contiene:
- nombre;
- objetivo;
- fecha de inicio;
- fecha de cierre;
- estado;
- tareas;
- retrospectiva.

## Kanban

```text
Por hacer → En progreso → En revisión → Terminado
```

## Backlog
Cada tarea puede incluir:
- título;
- fase CRISP-DM;
- sprint;
- estado;
- prioridad;
- owner;
- fecha límite;
- estimación;
- criterio de aceptación;
- notas.

## Equipo
Permite registrar:
- nombre;
- rol;
- correo electrónico.

Los integrantes pueden utilizarse como Owner de tareas, KPIs y riesgos.

## KPIs
Cada KPI puede contener:
- nombre;
- categoría;
- meta;
- valor actual;
- unidad;
- frecuencia;
- owner;
- notas.

## Riesgos
Cada riesgo contiene:
- descripción;
- probabilidad;
- impacto;
- score;
- owner;
- mitigación;
- estado.

```text
Score de riesgo = Probabilidad × Impacto
```

## Entregables
Cada entregable puede contener:
- nombre;
- fase;
- fecha;
- estado;
- enlace;
- notas;
- Definition of Done.

## Notas y evidencia
Tipos disponibles:
- Decisión
- Evidencia
- Hallazgo
- Review
- Retrospectiva
- Supuesto

---

# Estructura recomendada del repositorio

```text
danu-data-science-project/
│
├── README.md
├── index.html
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── external/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_preparation.ipynb
│   ├── 03_modeling.ipynb
│   └── 04_evaluation.ipynb
│
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   └── utils/
│
├── reports/
│   ├── figures/
│   └── deliverables/
│
├── docs/
│   ├── business_understanding/
│   ├── data_dictionary/
│   ├── decisions/
│   └── meeting_notes/
│
└── models/
```

---

# Ejecución del tracker

Actualmente el tracker es una aplicación web contenida en un único archivo HTML.

## Abrir directamente

Abrir:

```text
index.html
```

en un navegador.

## Servidor local con Python

```bash
python -m http.server 8000
```

Después abrir:

```text
http://localhost:8000
```

---

# Persistencia actual

Actualmente la información se almacena mediante:

```javascript
localStorage
```

Esto significa que los datos permanecen en el navegador del usuario.

```text
Usuario A → localStorage A
Usuario B → localStorage B
```

Por lo tanto, los cambios **todavía no se sincronizan automáticamente entre diferentes computadoras o navegadores**.

Publicar el HTML en GitHub Pages permite compartir la herramienta, pero no convierte por sí solo el tracker en una aplicación colaborativa.

---

# Backups

El tracker permite:

- exportar respaldo;
- importar respaldo.

Los datos se exportan como JSON.

Se recomienda crear un respaldo:
- al cierre de cada sprint;
- antes de cambios importantes;
- antes de eliminar información;
- antes de modificar la estructura del tracker.

---

# Publicación sin dominio

El frontend puede publicarse mediante **GitHub Pages**.

Ejemplo:

```text
https://usuario.github.io/danu-data-science-project/
```

No es necesario comprar un dominio.

---

# Arquitectura colaborativa futura

Una evolución gratuita propuesta para el proyecto es:

```text
GitHub Pages
      │
      ▼
CRISP-Agile Tracker
      │
      ▼
Google Apps Script
      │
      ▼
Google Sheets
```

La idea sería utilizar Google Sheets como **source of truth** de:

- proyectos;
- tareas;
- sprints;
- KPIs;
- riesgos;
- entregables;
- notas;
- integrantes del equipo.

Esta arquitectura todavía no forma parte de la versión actual del tracker.

---

# Convenciones de trabajo para Danu

## Antes de cada sprint

Definir:
1. Sprint Goal.
2. tareas seleccionadas;
3. responsables;
4. criterios de aceptación;
5. entregable esperado;
6. fases CRISP-DM involucradas.

## Durante el sprint

Actualizar:
- estado de tareas;
- hallazgos;
- bloqueos;
- riesgos;
- decisiones;
- evidencia.

## Sprint Review

Evaluar:
- qué se terminó;
- qué quedó pendiente;
- qué evidencia se obtuvo;
- qué aprendió el equipo;
- qué supuestos cambiaron;
- si es necesario regresar a alguna fase CRISP-DM;
- qué debe entrar en el siguiente sprint.

## Retrospectiva

Usar una estructura simple:

### Keep
¿Qué funcionó y debe mantenerse?

### Improve
¿Qué debe mejorar?

### Stop
¿Qué no está generando valor?

### Start
¿Qué nuevas prácticas debemos comenzar?

---

# Definition of Done

Una tarea no debe considerarse terminada solamente porque el código funciona.

Dependiendo del tipo de trabajo, puede requerir:
- código ejecutable;
- resultado validado;
- documentación;
- evidencia;
- revisión;
- archivo almacenado en el repositorio;
- criterio de aceptación cumplido.

---

# Gestión de datos y seguridad

No subir al repositorio:
- credenciales;
- passwords;
- API keys;
- tokens;
- datos confidenciales;
- información personal identificable;
- datasets privados del socio formador sin autorización.

Ejemplo de `.gitignore`:

```gitignore
.env
*.key
credentials.json
data/private/
data/raw/confidential/
```

---

# Buenas prácticas de Git

## Branch principal

```text
main
```

Debe contener versiones funcionales y revisadas.

## Branches de trabajo

Ejemplos:

```text
feature/data-cleaning
feature/eda
feature/model-baseline
feature/dashboard
fix/missing-values
docs/business-understanding
```

## Commits

Ejemplos:

```text
feat: add initial EDA notebook
data: clean duplicated records
model: add baseline model
docs: update business understanding
fix: correct date parsing
tracker: update sprint tasks
```

---

# Trazabilidad recomendada

```text
Problema de negocio
        ↓
Objetivo
        ↓
KPI / criterio de éxito
        ↓
Datos
        ↓
Análisis
        ↓
Modelo / solución
        ↓
Evaluación
        ↓
Recomendación / despliegue
```

Cada decisión técnica debe poder relacionarse con una necesidad del negocio.

---

# Tecnologías previstas

## Análisis
- Python
- Pandas
- NumPy
- Jupyter / Google Colab

## Datos
- SQL

## Machine Learning
- Scikit-learn

## Visualización
- Matplotlib
- Power BI / Tableau, según necesidades del proyecto

## Control de versiones
- Git
- GitHub

## Gestión
- CRISP-Agile Project Tracker

---

# Equipo

**Atlantic Data Consulting**

Socio formador:

**Danu Analítica**

---

# Filosofía del proyecto

El objetivo no es únicamente entrenar un modelo.

El proyecto debe ser capaz de responder:

> ¿Qué problema de negocio estamos resolviendo?

> ¿Qué evidencia tenemos?

> ¿Los datos son suficientes y confiables?

> ¿La solución genera valor?

> ¿Cómo medimos que funcionó?

> ¿Cómo puede utilizarse el resultado fuera de un notebook?

CRISP-DM proporciona la estructura para responder estas preguntas y Agile permite hacerlo de manera iterativa conforme aparece nueva información.

---

## License

Uso académico y de desarrollo interno del proyecto.
