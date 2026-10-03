# Guía de Contribución

¡Muchas gracias por tu interés en contribuir a **Ciencia de Datos para Principiantes** en español latino! 

Apreciamos inmensamente las contribuciones de la comunidad académica, profesional y de estudiantes de toda Hispanoamérica para mantener este currículo actualizado, riguroso y accesible para todos.

---

## Tabla de Contenidos

- [Código de Conducta](#código-de-conducta)
- [¿Cómo Puedes Contribuir?](#cómo-puedes-contribuir)
  - [Reportar Errores o Inconsistencias](#reportar-errores-o-inconsistencias)
  - [Sugerir Mejoras Pedagógicas o Nuevos Ejemplos](#sugerir-mejoras-pedagógicas-o-nuevos-ejemplos)
  - [Mejorar Cuadernos de Jupyter o Código](#mejorar-cuadernos-de-jupyter-o-código)
- [Pautas de Estilo y Terminología](#pautas-de-estilo-y-terminología)
- [Flujo de Trabajo para Pull Requests](#flujo-de-trabajo-para-pull-requests)
- [Licencia](#licencia)

---

## Código de Conducta

Este proyecto fomenta un ambiente colaborativo, respetuoso, inclusivo y libre de discriminación. Consulta nuestro [Código de Conducta](CODE_OF_CONDUCT.md) para más detalles.

---

## ¿Cómo Puedes Contribuir?

### Reportar Errores o Inconsistencias
Si encuentras un error tipográfico, un enlace roto, un error de código en un notebook o una discrepancia matemática:
1. Revisa los **Issues** existentes para confirmar que no haya sido reportado previamente.
2. Abre un nuevo **Issue** detallando:
   - Lección o archivo afectado.
   - Descripción clara del error observado.
   - Propuesta de corrección o comportamiento esperado.

### Sugerir Mejoras Pedagógicas o Nuevos Ejemplos
- ¿Conoces un conjunto de datos abierto de América Latina relevante para ilustrar una lección?
- ¿Tienes una explicación intuitiva para un concepto matemático complejo (ej. p-valores, gradiente descendente, matriz de confusión)?
- ¡Abre una discusión o propuesta en un Issue!

### Mejorar Cuadernos de Jupyter o Código
- Si actualizas un notebook (`.ipynb`), asegúrate de limpiar las salidas de celda innecesarias antes de hacer commit, o conservar únicamente las salidas que sirvan de guía visual para los estudiantes.
- Verifica que el notebook se ejecute sin errores de principio a fin (`Kernel > Restart & Run All`).

---

## Pautas de Estilo y Terminología

Para preservar la coherencia pedagógica y técnica del repositorio, solicitamos seguir estas directrices:

1. **Español Latinoamericano Neutral**:
   - Usa un tono cordial, motivador y profesional en segunda persona singular ("tú").
   - Emplea vocabulario estándar de la región: "computadora", "archivo", "ejecutar", "seleccionar".
2. **Terminología Nativa de Ciencia de Datos**:
   - No traduzcas términos de la industria tecnológica donde el estándar internacional sea el término en inglés (*DataFrame*, *Feature Engineering*, *Overfitting*, *Underfitting*, *EDA*, *Pipeline*, *Outliers*, *Clustering*, *Random Forest*, *Cross-Validation*).
   - El código en Python, nombres de variables, argumentos de funciones y llamadas a librerías **nunca** deben traducirse.
3. **Formato Markdown y Matemáticas**:
   - Emplea sintaxis LaTeX estándar para fórmulas matemáticas: `$x$` para matemáticas en línea y `$$...$$` para fórmulas en bloque.
   - Mantén enlaces relativos precisos para imágenes y datos.

---

## Flujo de Trabajo para Pull Requests

1. Haz un **Fork** de este repositorio en tu cuenta de GitHub.
2. Clona tu fork localmente:
   ```bash
   git clone https://github.com/tu-usuario/Ciencia-de-Datos-para-Principiantes.git
   ```
3. Crea una rama descriptiva para tu cambio:
   ```bash
   git checkout -b mejora/leccion-08-limpieza-datos
   ```
4. Realiza tus modificaciones con mensajes de commit claros y concisos en español:
   ```bash
   git commit -m "Corrige enlace de dataset en lección 08"
   ```
5. Sube tu rama a tu repositorio remoto:
   ```bash
   git push origin mejora/leccion-08-limpieza-datos
   ```
6. Abre un **Pull Request** (PR) hacia la rama `main` de este repositorio describiendo tus cambios.

---

## Licencia

Al contribuir a este proyecto, aceptas que tus contribuciones se licencien bajo la misma [Licencia MIT](LICENSE) que rige este repositorio.
