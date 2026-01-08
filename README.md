# Análisis de Experimento A/B y Embudo de Eventos

## 📌 Descripción del proyecto
Este proyecto analiza el comportamiento de los usuarios a partir de registros de eventos con el objetivo de evaluar un **experimento A/A/B** y entender el desempeño del **embudo de conversión**.  
Se estudian tres grupos experimentales (dos de control y uno de prueba) para validar cambios en el producto y determinar si estos generan diferencias estadísticamente significativas en el comportamiento de los usuarios.

---

## 🎯 Objetivos
- Analizar la actividad de los usuarios mediante eventos registrados.
- Construir y evaluar el embudo de eventos.
- Identificar en qué etapas se pierde la mayor cantidad de usuarios.
- Evaluar si existen diferencias estadísticamente significativas entre grupos experimentales.
- Validar la correcta división de los grupos de control (test A/A).
- Extraer conclusiones sobre el impacto del experimento A/B.

---

## 🗂️ Descripción de los datos
Cada registro corresponde a una acción o evento generado por un usuario.

### Columnas principales
- `event_name`: nombre del evento.
- `device_id_hash`: identificador único del usuario.
- `event_timestamp`: fecha y hora del evento.
- `exp_id`: identificador del experimento  
  - 246 y 247: grupos de control  
  - 248: grupo de prueba  

---

## 🧪 Metodología

### 1. Preparación de datos
- Carga y revisión inicial del dataset.
- Normalización de nombres de columnas.
- Conversión de tipos de datos.
- Creación de columnas de fecha y hora.
- Análisis de valores ausentes.

### 2. Exploración de datos
- Cálculo del número total de eventos y usuarios.
- Promedio de eventos por usuario.
- Análisis del período cubierto por los datos.
- Identificación del intervalo temporal con datos completos.
- Evaluación de la pérdida de usuarios y eventos al filtrar datos antiguos.
- Verificación de usuarios en todos los grupos experimentales.

### 3. Análisis del embudo de eventos
- Identificación y frecuencia de los eventos.
- Número de usuarios únicos por evento.
- Cálculo de la proporción de usuarios por etapa.
- Definición del orden lógico de eventos.
- Cálculo de la conversión entre etapas del embudo.
- Identificación del punto de mayor abandono.
- Proporción de usuarios que completan todo el recorrido hasta el pago.

### 4. Análisis del experimento A/A/B
- Comparación del tamaño de los grupos experimentales.
- Validación estadística entre los grupos de control (A/A).
- Comparación del grupo de prueba contra cada grupo de control.
- Comparación del grupo de prueba contra los controles combinados.
- Evaluación de diferencias estadísticas por evento.
- Ajuste del nivel de significancia considerando múltiples pruebas.

---

## 🛠️ Herramientas utilizadas
- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook

---

## 📊 Resultados y conclusiones
El análisis permite validar la correcta división de los grupos experimentales y evaluar el impacto del cambio probado en el experimento.  
Los resultados estadísticos y el análisis del embudo proporcionan evidencia clara para decidir si la modificación introducida genera mejoras reales en el comportamiento de los usuarios.

---

## 📁 Estructura del repositorio
- `logs_exp_us.csv`: registros de eventos de usuario.
- `Proyecto - Sprint 12.ipynb`: notebook con el análisis completo.
- `README.md`: documentación del proyecto.

---

## 👤 Autor
**Carlos Jaramillo**  
Analista de Datos