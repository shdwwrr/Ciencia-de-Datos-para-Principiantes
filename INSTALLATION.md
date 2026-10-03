# Guía de Instalación y Configuración del Entorno

Esta guía paso a paso te ayudará a configurar tu entorno de desarrollo para trabajar con el currículo de **Ciencia de Datos para Principiantes**. 

Está orientada a estudiantes, autodidactas y docentes de toda América Latina, considerando sistemas operativos Windows, macOS y Linux.

---

## Tabla de Contenidos

- [Requisitos Previos](#requisitos-previos)
- [Opción 1: En la Nube con GitHub Codespaces (Sin Instalación Local)](#opción-1-en-la-nube-con-github-codespaces-sin-instalación-local)
- [Opción 2: Instalación Local con Python y VS Code (Recomendada)](#opción-2-instalación-local-con-python-y-vs-code-recomendada)
- [Opción 3: Instalación con Anaconda o Miniconda](#opción-3-instalación-con-anaconda-o-miniconda)
- [Librerías Esenciales de Ciencia de Datos](#librerías-esenciales-de-ciencia-de-datos)
- [Verificación del Entorno](#verificación-del-entorno)
- [Consejos para Evitar Problemas Comunes](#consejos-para-evitar-problemas-comunes)

---

## Requisitos Previos

Antes de comenzar la instalación local, asegúrate de contar con:
- Una computadora con Windows 10/11, macOS (11+) o una distribución moderna de Linux (Ubuntu, Debian, Fedora, etc.).
- Conexión a Internet para descargar instaladores y paquetes.
- Una cuenta gratuita de [GitHub](https://github.com/) (necesaria para clonar el repositorio, enviar tareas o usar Codespaces).
- Nociones básicas del uso de la terminal o línea de comandos.

---

## Opción 1: En la Nube con GitHub Codespaces (Sin Instalación Local)

Si tu computadora tiene recursos limitados o no deseas instalar software localmente en este momento, GitHub Codespaces es la alternativa ideal:

1. Ve a la página principal de este repositorio en GitHub.
2. Haz clic en el botón verde **Code** y selecciona la pestaña **Codespaces**.
3. Haz clic en **Create codespace on main**.
4. En cuestión de 1 o 2 minutos, se abrirá un entorno completo de Visual Studio Code en tu navegador web con Linux, Python y las extensiones necesarias listas para trabajar.
5. Puedes abrir cualquier archivo `.ipynb` o `.md` y comenzar inmediatamente.

---

## Opción 2: Instalación Local con Python y VS Code (Recomendada)

Esta es la configuración estándar utilizada por profesionales y científicos de datos en la industria.

### Paso 1: Instalar Python (Versión 3.10 o superior)

- **Windows**:
  1. Descarga el instalador oficial desde [python.org](https://www.python.org/downloads/).
  2. **¡Muy importante!** En la primera pantalla del instalador, marca la casilla:  
     ☑ **Add Python.exe to PATH** (Agregar Python al PATH).
  3. Haz clic en **Install Now**.
  4. Para verificar la instalación, abre PowerShell o la Terminal y ejecuta:
     ```powershell
     python --version
     ```
- **macOS**:
  - Puedes descargarlo desde [python.org](https://www.python.org/downloads/) o usar [Homebrew](https://brew.sh/):
    ```bash
    brew install python
    ```
- **Linux (Ubuntu/Debian)**:
  ```bash
  sudo apt update
  sudo apt install python3 python3-pip python3-venv
  ```

### Paso 2: Instalar Visual Studio Code

1. Descarga e instala **Visual Studio Code** desde [code.visualstudio.com](https://code.visualstudio.com/).
2. Abre VS Code y dirígete a la pestaña de Extensiones (`Ctrl + Shift + X` o `Cmd + Shift + X`).
3. Instala las siguientes extensiones oficiales de Microsoft:
   - **Python** (soporte de lenguaje, depuración y autocompletado).
   - **Jupyter** (permite abrir, ejecutar y crear Jupyter Notebooks directamente en VS Code).
   - **Pylance** (análisis estático y autocompletado inteligente).
   - *(Opcional pero muy útil)* **Data Wrangler** (visualización e inspección interactiva de DataFrames de Pandas).

### Paso 3: Clonar el Repositorio y Crear un Entorno Virtual

1. Abre tu terminal y clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/Ciencia-de-Datos-para-Principiantes.git
   cd Ciencia-de-Datos-para-Principiantes
   ```
2. Crea un entorno virtual aislado (`.venv`) para no alterar los paquetes globales de tu sistema:
   - **En Windows:**
     ```powershell
     python -m venv .venv
     .venv\Scripts\activate
     ```
   - **En macOS / Linux:**
     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     ```
3. Una vez activado el entorno, notarás el prefijo `(.venv)` en tu terminal.

---

## Opción 3: Instalación con Anaconda o Miniconda

Si prefieres una distribución científica todo-en-uno que incluya paquetes matemáticos optimizados:

1. Descarga e instala [Miniconda](https://docs.conda.io/en/latest/miniconda.html) (versión ligera) o [Anaconda](https://www.anaconda.com/).
2. Abre la terminal de Conda (*Anaconda Prompt* en Windows) y crea un nuevo entorno:
   ```bash
   conda create -n cienciadatos python=3.11
   conda activate cienciadatos
   ```
3. Instala las librerías necesarias con conda:
   ```bash
   conda install -c conda-forge numpy pandas matplotlib seaborn scipy scikit-learn jupyterlab
   ```

---

## Librerías Esenciales de Ciencia de Datos

Si estás utilizando la Opción 2 con `pip`, instala las dependencias fundamentales ejecutando:

```bash
pip install --upgrade pip
pip install numpy pandas matplotlib seaborn scipy scikit-learn requests jupyter
```

### ¿Qué hace cada librería en nuestro curso?

| Librería | Propósito en el Currículo |
|:---|:---|
| `numpy` | Computación numérica de alto rendimiento y operaciones con vectores y matrices multidimensionales. |
| `pandas` | Manipulación, filtrado, limpieza y análisis estructurado con DataFrames y Series temporales. |
| `matplotlib` | Gráficos estadísticos fundamentales en 2D (barras, líneas, histogramas, dispersión). |
| `seaborn` | Visualización estadística avanzada con paletas atractivas y gráficos de relaciones complejos. |
| `scipy` | Algoritmos científicos, pruebas de hipótesis estadísticas (*t-test*, ANOVA) y funciones matemáticas. |
| `scikit-learn` | Modelos de Machine Learning (regresión, clasificación, clustering, métricas de evaluación). |
| `requests` | Descarga de datos vía HTTP y consumo de APIs web en tiempo real. |
| `jupyter` | Servidor y soporte para cuadernos interactivos con celdas de código y Markdown. |

---

## Verificación del Entorno

Para asegurarte de que todo está correctamente instalado y funcionando, puedes ejecutar el siguiente comando en tu terminal con el entorno activado:

```bash
python -c "
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import sklearn

print('¡Configuración exitosa!')
print(f'- NumPy: {np.__version__}')
print(f'- Pandas: {pd.__version__}')
print(f'- Scikit-Learn: {sklearn.__version__}')
"
```

Si el comando muestra los números de versión sin errores de importación, tu entorno está 100% listo para comenzar la **Semana 1**.

---

## Consejos para Evitar Problemas Comunes

1. **Selección de Kernel en VS Code**: Cuando abras un notebook (`.ipynb`), fíjate en la esquina superior derecha del editor. Debe indicar que el Kernel seleccionado es el de tu entorno virtual (`.venv` o `conda: cienciadatos`). Si dice "Select Kernel", haz clic en él y elige el intérprete de tu entorno.
2. **Ejecución de celdas**: Usa `Shift + Enter` para ejecutar una celda y avanzar automáticamente a la siguiente.
3. **Rutas relativas**: Recuerda que las rutas relativas en los notebooks (por ejemplo, `../../data/birds.csv`) toman como referencia la carpeta donde reside el notebook. Siempre abre la carpeta raíz del repositorio en VS Code (`File > Open Folder`).

¿Tienes algún inconveniente? Consulta nuestra [Guía de Solución de Problemas (TROUBLESHOOTING.md)](TROUBLESHOOTING.md).
