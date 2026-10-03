# Guía de Solución de Problemas (Troubleshooting)

Esta guía ofrece diagnósticos y soluciones claras para los problemas técnicos más frecuentes que suelen enfrentar estudiantes y docentes al trabajar con este currículo de Ciencia de Datos.

---

## Tabla de Contenidos

- [1. Problemas con Python y Entornos Virtuales](#1-problemas-con-python-y-entornos-virtuales)
- [2. Problemas con Jupyter Notebooks y Selección de Kernel](#2-problemas-con-jupyter-notebooks-y-selección-de-kernel)
- [3. Error de Módulos No Encontrados (ModuleNotFoundError)](#3-error-de-módulos-no-encontrados-modulenotfounderror)
- [4. Error de Rutas de Archivos (FileNotFoundError)](#4-error-de-rutas-de-archivos-filenotfounderror)
- [5. Problemas de Codificación de Caracteres (Unicode / UTF-8) en Windows](#5-problemas-de-codificación-de-caracteres-unicode--utf-8-en-windows)
- [6. Problemas con la Aplicación de Cuestionarios (`quiz-app`)](#6-problemas-con-la-aplicación-de-cuestionarios-quiz-app)
- [7. Problemas con Git y Sincronización](#7-problemas-con-git-y-sincronización)

---

## 1. Problemas con Python y Entornos Virtuales

### Síntoma: "'python' no se reconoce como un comando interno o externo" (en Windows)
- **Causa**: Python no fue agregado a las variables de entorno del sistema (`PATH`) durante la instalación.
- **Solución**:
  1. Vuelve a ejecutar el instalador de Python descargado de `python.org`.
  2. Selecciona la opción **Modify** (Modificar).
  3. Asegúrate de marcar la casilla **Add Python to environment variables** (o *Add Python to PATH*).
  4. Alternativamente, abre la terminal y escribe `py` en lugar de `python`.

### Síntoma: "La ejecución de scripts está deshabilitada en este sistema" (PowerShell)
- **Causa**: La directiva de ejecución de PowerShell bloquea la activación de entornos virtuales (`activate.ps1`).
- **Solución**:
  Abre PowerShell como Administrador y ejecuta:
  ```powershell
  Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
  ```
  Luego, vuelve a tu terminal habitual y activa tu entorno:
  ```powershell
  .venv\Scripts\activate
  ```

---

## 2. Problemas con Jupyter Notebooks y Selección de Kernel

### Síntoma: El notebook no ejecuta código o se queda en "Connecting to kernel..."
- **Causa**: VS Code no tiene asignado el intérprete de Python correcto para el notebook o falta el paquete `ipykernel`.
- **Solución**:
  1. En VS Code, abre el notebook (`.ipynb`).
  2. Mira en la esquina superior derecha del editor y haz clic sobre el botón de Kernel (puede decir *Select Kernel* o mostrar una versión de Python diferente).
  3. Selecciona **Python Environments...** y elige el entorno virtual que creaste (`.venv (Python 3.x)`).
  4. Si VS Code te solicita instalar `ipykernel`, pulsa **Install** y espera unos segundos.

### Síntoma: Las variables se comportan de forma impredecible o dan errores inesperados
- **Causa**: Las celdas del notebook se ejecutaron en un orden diferente al secuencial de arriba a abajo.
- **Solución**:
  Haz clic en el botón **Restart** (Reiniciar Kernel) en la barra superior del notebook y luego haz clic en **Run All** (Ejecutar todo) o ejecuta las celdas secuencialmente con `Shift + Enter`.

---

## 3. Error de Módulos No Encontrados (ModuleNotFoundError)

### Síntoma: `ModuleNotFoundError: No module named 'pandas'` (o `numpy`, `matplotlib`, `seaborn`)
- **Causa**: La librería se instaló en el entorno global del sistema o en otro entorno diferente al que está ejecutando el notebook.
- **Solución**:
  1. Abre la terminal integrada de VS Code (`Ctrl + ~`).
  2. Verifica que tu entorno virtual esté activo (debe verse el prefijo `(.venv)`).
  3. Instala los paquetes requeridos directamente en ese entorno:
     ```bash
     pip install pandas numpy matplotlib seaborn scikit-learn scipy requests
     ```
  4. En el notebook, reinicia el kernel y vuelve a ejecutar la celda de importación.

---

## 4. Error de Rutas de Archivos (FileNotFoundError)

### Síntoma: `FileNotFoundError: [Errno 2] No such file or directory: '../../data/birds.csv'`
- **Causa**: La ruta relativa depende del directorio actual de trabajo (*current working directory*). Si abres únicamente la carpeta de una lección individual en lugar de la raíz del proyecto, las rutas que suben niveles (`../../`) no encontrarán la carpeta `data/`.
- **Solución**:
  1. En VS Code, abre siempre la carpeta raíz del repositorio:  
     **File > Open Folder... > Selecciona la carpeta 'Ciencia de Datos para Principiantes'**.
  2. Verifica que la carpeta `data/` se encuentre directamente en la raíz con sus archivos (`birds.csv`, `honey.csv`, `mushrooms.csv`, etc.).
  3. En Python puedes verificar cuál es tu directorio de trabajo actual ejecutando:
     ```python
     import os
     print("Directorio actual:", os.getcwd())
     ```

---

## 5. Problemas de Codificación de Caracteres (Unicode / UTF-8) en Windows

### Síntoma: Símbolos extraños al leer archivos CSV o al imprimir en consola (`UnicodeDecodeError`)
- **Causa**: Algunos datasets o terminales en Windows usan por defecto la codificación heredada `Windows-1252` o `cp437` en lugar del estándar moderno `UTF-8`.
- **Solución**:
  1. Al leer archivos de texto o CSV en Python con `pandas` o la función `open()`, especifica siempre explícitamente `encoding='utf-8'`:
     ```python
     df = pd.read_csv('../../data/birds.csv', encoding='utf-8')
     ```
  2. Si un archivo fue guardado con otra codificación regional, prueba alternativamente con `encoding='latin1'` o `encoding='cp1252'`.
  3. Para configurar la consola de PowerShell en UTF-8:
     ```powershell
     [Console]::OutputEncoding = [System.Text.Encoding]::UTF8
     ```

---

## 6. Problemas con la Aplicación de Cuestionarios (`quiz-app`)

### Síntoma: Quiero presentar los cuestionarios en mi computadora sin conexión a Internet
- **Solución**:
  La aplicación de cuestionarios se encuentra en la carpeta [`quiz-app/`](quiz-app/). Para ejecutarla localmente:
  1. Asegúrate de tener instalado [Node.js](https://nodejs.org/) (versión 16+).
  2. Abre tu terminal en la carpeta `quiz-app`:
     ```bash
     cd quiz-app
     npm install
     npm run serve
     ```
  3. Abre `http://localhost:8080/` en tu navegador. Todos los cuestionarios y opciones se cargarán en español latino por defecto.

---

## 7. Problemas con Git y Sincronización

### Síntoma: `error: Your local changes to the following files would be overwritten by merge`
- **Causa**: Modificaste un notebook localmente (ej. ejecutaste celdas y se guardaron los resultados) y hay cambios entrantes en el repositorio remoto.
- **Solución**:
  Guarda temporalmente tus cambios con `git stash` o crea una rama de trabajo propia para tus experimentos:
  ```bash
  git stash
  git pull origin main
  git stash pop
  ```

---

¿Tu problema no está listado aquí? Abre un **Issue** en el repositorio describiendo detalladamente tu sistema operativo, el comando ejecutado y el mensaje de error completo. ¡La comunidad y tus docentes estamos para ayudarte!
