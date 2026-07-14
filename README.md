# Herramienta de Evaluación de Metodologías de Gestión de Riesgos

> Herramienta web de evaluación computacional que compara las metodologías **ISO/IEC 27005**, **NIST SP 800-30** y **MAGERIT v3** mediante un modelo multicriterio ponderado, con el propósito de recomendar la metodología más adecuada según las características y el nivel de madurez digital de una organización.

---

## Descripción

Esta herramienta fue desarrollada como parte del trabajo de titulación de la **Universidad Politécnica Salesiana — Sede Guayaquil**, en la carrera de Ingeniería de Sistemas.

El sistema evalúa cinco criterios técnicos ponderados mediante el método de centroide por orden de rango (ROC):

| Criterio | Peso base |
|---|---|
| Precisión en la valoración del riesgo | 26% |
| Alineación con la tríada CIA | 24% |
| Adaptabilidad organizacional | 19% |
| Facilidad de implementación | 16% |
| Pertinencia contextual | 15% |

Los pesos se ajustan dinámicamente según el perfil organizacional ingresado por el usuario, considerando el sector de actividad, el tamaño de la organización, el nivel de madurez digital, el tipo de activos críticos y los recursos disponibles.

---

## Uso

No requiere instalación. Solo necesitas un navegador web moderno.

**Opción 1 — Uso directo:**
1. Descarga el archivo `herramienta_gestion_riesgos.html`
2. Ábrelo con cualquier navegador (Chrome, Firefox o Edge)
3. Responde las cinco preguntas del cuestionario
4. Revisa la recomendación generada

**Opción 2 — Clonar el repositorio:**
```bash
git clone https://github.com/carlosorrala95/herramienta-web-para-la-comparaci-n-de-metodolog-as.git
cd herramienta-web-para-la-comparaci-n-de-metodolog-as
```
Luego abre el archivo `herramienta_gestion_riesgos.html` en tu navegador.

---

## Tecnologías utilizadas

- **HTML5** — estructura del contenido
- **CSS3** — diseño visual de la interfaz
- **JavaScript** — lógica de cálculo y comportamiento dinámico

No requiere dependencias externas, frameworks ni conexión a servidores. Todo el procesamiento ocurre localmente en el navegador.

---

## Metodologías evaluadas

| Metodología | Organismo | Año | Idioma oficial |
|---|---|---|---|
| ISO/IEC 27005:2022 | ISO/IEC | 2022 | Inglés (traducción al español disponible) |
| NIST SP 800-30 Rev. 1 | NIST — EE. UU. | 2012 | Inglés |
| MAGERIT v3 | Gobierno de España | 2012 | Español |

---

## Estructura del repositorio

```
herramienta-web-para-la-comparaci-n-de-metodolog-as/
│
├── herramienta_gestion_riesgos.html   # Herramienta principal
└── README.md                          # Este archivo
```

---

## Cómo funciona

La herramienta sigue un proceso de tres etapas:

**1. Cuestionario de perfil organizacional**
El usuario responde cinco preguntas sobre su organización: sector de actividad, tamaño, nivel de madurez digital, tipo de activos críticos y recursos disponibles para implementar la metodología.

**2. Cálculo del índice de adecuación ponderado**
Con base en las respuestas, la herramienta ajusta los pesos de los cinco criterios y calcula el índice de adecuación de cada metodología mediante la fórmula:

```
Índice(M) = Σ [ Puntuación(M, criterio_i) × Peso(criterio_i) ]   para i = 1 a 5
```

En caso de empate se aplica una regla de desempate en cascada de cuatro niveles basada en los criterios de mayor peso del perfil.

**3. Presentación de resultados**
La herramienta muestra al usuario:
- La metodología recomendada con su índice de adecuación y justificación textual
- Un gráfico de barras comparativo de los tres índices
- Una tabla con las puntuaciones individuales por criterio y sus pesos
- El ranking final con el porcentaje del máximo alcanzado por cada metodología

---

## Privacidad

La herramienta **no almacena, transmite ni registra** ningún dato ingresado por el usuario. Todo el procesamiento ocurre localmente en el navegador sin conexión a servidores externos.

---

## Autor

**Carlos Alberto Orrala Mesias**
Estudiante de Ingeniería de Sistemas
Universidad Politécnica Salesiana — Sede Guayaquil
Ecuador, 2026


