## 📌 Operatoria del Script de Búsqueda de CUIT en Excel

### 📝 Introducción
Este script tiene como finalidad encontrar la CUIT exacta en una planilla de Excel o, en su defecto, determinar la que más se asemeja utilizando un margen de aproximación del 95% al 100%. Dado que
los valores en la planilla pueden corresponder a CUIT's completas o a fragmentos de ellas, es crucial identificar la coincidencia más precisa. En el caso de que hubiese un valor preesxistente 
en la columna CUIT no se realizara ninguna modificacion y se continuara con la fila siguiente. 

### 🔎 Proceso de Búsqueda
1. **Búsqueda Exacta (100%)**
   - Se inicia revisando la columna "Clave de referencia 1" de la planilla; en busca de una coincidencia entre el valor de la fila y las CUIT's que tenemos proporcionadas.
   - Si no se encuentra una coincidencia en la primera columna, se continúa con la siguiente ("Clave de refrencia 2") y así sucesivamente.
   - Este enfoque evita el cálculo innecesario de porcentajes de coincidencia en cada instancia, optimizando el rendimiento.

2. **Búsqueda por Aproximación (≥95%)**
   - Si no se encuentra una coincidencia exacta, el script procede a calcular el porcentaje de aproximación de cada valor en las columnas.
   - Dado que en la planilla pueden existir CUIT's completas o solo partes de ellas, el algoritmo analiza cada dato para determinar el que más se asemeja a la CUIT buscada.
   - Si todos los valores superan el umbral del 95% (o el porcentaje configurado por defecto), se selecciona el que tenga la mayor similitud.
   - Este procedimiento se repite en cada fila de la planilla, asegurando que todos los registros sean evaluados.

### 🔄 Validación de CUIT Duplicadas
- Se verifica que no existan CUIT duplicadas en la pestaña **"Base del mes anterior"**.
- En caso de encontrar duplicaciones, estas serán reportadas en la pestaña principal.

### 🎯 Objetivos
✔️ Optimizar la búsqueda de CUIT en la planilla.  
✔️ Reducir el tiempo de procesamiento.  
✔️ Garantizar la precisión en la selección de la CUIT más adecuada.  
✔️ Adaptarse a la estructura de los datos, considerando CUITs completas o parciales.  
✔️ Detectar y reportar posibles duplicados.  


![](https://github.com/cgzanfa/Busqueda_cuit_por_aproximacion/blob/main/Cuit_finder_1.png)
