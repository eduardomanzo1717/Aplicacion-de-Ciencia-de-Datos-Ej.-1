# Aplicacion-de-Ciencia-de-Datos-Ej.-1
Aplicacion de Ciencia de Datos, para Deteccion de Diabetes
# 🩺 Detección de Diabetes con Árboles de Decisión

¡Hola! 👋 Este es un proyecto que usa inteligencia artificial para ayudar a detectar diabetes analizando diferentes factores de salud de las personas.

## ¿De qué va esto?

Básicamente, este proyecto toma información sobre la salud de las personas (como su edad, presión arterial, niveles de azúcar, etc.) y usa un modelo llamado "Árbol de Decisión" para predecir si alguien tiene diabetes o no.

El proyecto está inspirado en un ejemplo del libro "Principles of Data Science" y usa datos reales de 100,000 personas que puedes encontrar en Kaggle.

### ¿Qué hace especial a este proyecto?

- **Limpia y organiza los datos**: Convierte la información en un formato que el modelo pueda entender
- **Balancea los datos**: Asegura que haya suficientes casos de personas con y sin diabetes para que el modelo aprenda bien
- **Entrena un modelo inteligente**: Crea un árbol de decisión que aprende patrones en los datos
- **Evalúa qué tan bueno es**: Muestra gráficas y números que te ayudan a entender qué tan confiable es el modelo

### ¿Qué tan bueno es el modelo?

¡Bastante bueno! 🎯

- Acierta en el **85.6%** de los casos cuando le muestras datos nuevos
- Detecta correctamente al **96%** de las personas que realmente tienen diabetes (esto es muy importante para no pasar por alto casos reales)
- Tiene un puntaje general de **0.93** en una escala de 0 a 1 (donde 1 es perfecto)

Los factores más importantes que el modelo encontró son:
- El nivel de hemoglobina A1c (HbA1c)
- El nivel de glucosa en la sangre
- La edad
- El índice de masa corporal (BMI)

## 📁 Archivos que necesitas

Para que todo funcione, necesitas estos tres archivos en la misma carpeta:

- `Version_2_de_Diabetes__Eduardo_Ruiz.ipynb` - Este es el archivo principal con todo el código
- `diabetes_prediction_dataset.csv.zip` - Los datos de las 100,000 personas (viene comprimido)
- `Aplicación de técnicas de ciencia de datos para la detección de la diabetes.pdf` - Documentación adicional (opcional, pero útil)

## 🛠️ Lo que necesitas tener instalado

Antes de empezar, asegúrate de tener:

- **Python 3.7 o más reciente** (si no lo tienes, puedes descargarlo de python.org)
- **Jupyter Notebook** o **JupyterLab** (esto es como un editor especial para trabajar con notebooks)
- Algunas librerías de Python que te explico cómo instalar abajo

## 📦 Cómo instalar todo

### Paso 1: Prepara los archivos

Primero, asegúrate de tener todos los archivos en la misma carpeta. Es importante que el archivo `.zip` con los datos esté en el mismo lugar que el notebook, porque el código lo busca ahí.

### Paso 2: Instala las librerías necesarias

Abre tu terminal (o PowerShell en Windows) y navega hasta la carpeta donde tienes el proyecto. Luego ejecuta este comando:

```bash
pip install pandas scikit-learn matplotlib seaborn numpy jupyter
```

Esto instalará todas las herramientas que necesitas. Si ya tienes algunas instaladas, no te preocupes, solo actualizará las que falten.

**Tip**: Si prefieres ser más organizado, puedes crear un archivo llamado `requirements.txt` con este contenido:

```
pandas>=1.3.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
numpy>=1.21.0
jupyter>=1.0.0
```

Y luego instalar todo con:

```bash
pip install -r requirements.txt
```

### Paso 3: Verifica que todo esté bien

Para asegurarte de que todo se instaló correctamente, puedes probar ejecutando esto en Python:

```python
import pandas as pd
import sklearn
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
print("¡Todo está listo! 🎉")
```

Si no sale ningún error, ¡estás listo para continuar!

## 🚀 Cómo usar el proyecto

### Paso 1: Abre Jupyter Notebook

En la terminal, dentro de la carpeta del proyecto, escribe:

```bash
jupyter notebook
```

O si prefieres JupyterLab (que tiene una interfaz más moderna):

```bash
jupyter lab
```

Esto abrirá una ventana en tu navegador. ¡No cierres la terminal! Déjala abierta mientras trabajas.

### Paso 2: Abre el notebook

En el navegador que se abrió, busca el archivo `Version_2_de_Diabetes__Eduardo_Ruiz.ipynb` y haz clic en él para abrirlo.

**Importante**: Asegúrate de que el archivo `diabetes_prediction_dataset.csv.zip` esté en la misma carpeta. Si no está ahí, el código no podrá encontrar los datos.

### Paso 3: Ejecuta el código

El notebook está dividido en "celdas" (cajas con código). Puedes ejecutarlas de dos formas:

**Opción A - Ejecutar todo de una vez:**
- Ve al menú y selecciona `Cell > Run All`
- Esto ejecutará todo el código desde el principio hasta el final

**Opción B - Ejecutar paso a paso (recomendado la primera vez):**
- Ve celda por celda
- Presiona `Shift + Enter` en cada celda para ejecutarla
- Esto te permite ver qué hace cada parte del código

### ¿Qué hace cada parte?

El notebook está organizado así:

1. **Al principio**: Carga las herramientas necesarias y los datos
2. **Exploración**: Te muestra información sobre los datos (cuántos hay, qué columnas tiene, etc.)
3. **Limpieza**: Convierte los datos a un formato que el modelo pueda usar
4. **Visualización**: Crea gráficas bonitas para que veas cómo se distribuyen los datos
5. **Balanceo**: Ajusta los datos para que haya igual cantidad de casos con y sin diabetes
6. **Entrenamiento**: Enseña al modelo a reconocer patrones
7. **Evaluación**: Te muestra qué tan bueno es el modelo con gráficas y números

## 📊 Sobre los datos

El conjunto de datos tiene información de 100,000 personas con estas características:

- **gender**: El género de la persona
- **age**: La edad
- **hypertension**: Si tiene hipertensión (0 = No, 1 = Sí)
- **heart_disease**: Si tiene enfermedad cardíaca (0 = No, 1 = Sí)
- **smoking_history**: Si fuma o ha fumado
- **bmi**: El índice de masa corporal
- **HbA1c_level**: El nivel de hemoglobina A1c (importante para diabetes)
- **blood_glucose_level**: El nivel de glucosa en la sangre
- **diabetes**: Si tiene diabetes o no (esto es lo que queremos predecir)

## 📈 ¿Cómo sabemos si el modelo es bueno?

El proyecto incluye varias formas de evaluar el modelo:

- **Matriz de confusión**: Una tabla que muestra cuántas veces acertó y cuántas se equivocó
- **Curva ROC**: Una gráfica que muestra qué tan bien distingue entre personas con y sin diabetes
- **AUC**: Un número del 0 al 1 que resume qué tan bueno es (0.93 es muy bueno)
- **Reporte de clasificación**: Te dice la precisión, sensibilidad y otros números importantes
- **Sensibilidad**: Qué tan bien detecta a las personas que realmente tienen diabetes (96% es excelente)

## 💡 Algunas cosas técnicas (pero explicadas simple)

- Los datos originales tienen muchos más casos sin diabetes que con diabetes (91,500 vs 8,500), así que el código "balancea" los datos tomando una muestra igual de cada grupo
- El modelo usa un árbol de decisión con profundidad máxima de 4 niveles para evitar que "memorice" los datos en lugar de aprender patrones reales
- Los datos se dividen en dos grupos: 75% para enseñarle al modelo y 25% para probar qué tan bien aprendió

## 👤 Autor

Eduardo Ruiz

## 📚 Referencias

- El proyecto está basado en el ejemplo 10.3 del libro "Principles of Data Science" de OpenStax
- Los datos vienen de este dataset en Kaggle: [Diabetes Prediction Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)

## 📝 Nota final

Este es un proyecto educativo. Aunque el modelo es bastante bueno, **no debe usarse para diagnósticos médicos reales**. Siempre consulta con un profesional de la salud para cualquier tema relacionado con tu salud.

