# Laboratorio 01 - Mejore la narrativa de datos con el agente Analyst de Microsoft 365 Copilot

Duración estimada: *10 - 15 minutos*

![Get started with Analyst in Microsoft 365 Copilot - Microsoft
Support](./media/image1.png)

# Objetivo

Este laboratorio utiliza el agente Analyst (Analista) de Microsoft 365
Copilot para analizar la hoja de cálculo de los **resultados de la
encuesta del Proyecto Nexus**. Deberá cargar el archivo al agente
Analyst y ejecutar *prompts* (indicaciones) iniciales para extraer las
tendencias principales, profundizar en los promedios y crear elementos
visuales (gráficos, mapas de calor, etc.).

# Requisitos previos

1.  Acceso a una cuenta de Microsoft 365 con Copilot y agentes
    habilitados (el agente Analyst debe estar disponible).

2.  Navegador: Se recomienda Microsoft Edge (el módulo utiliza Edge para
    las instrucciones).

3.  Archivo CSV / XLSX de los resultados de la encuesta del Proyecto
    Nexus (la página de Learn incluye los enlaces de descarga desde
    GitHub).

# Instrucciones paso a paso

# Ejercicio 1: Configuración y carga del conjunto de datos

1.  Descargue el conjunto de datos: Abra el enlace **"Project Nexus
    Survey Results.xlsx"** proporcionado en la guía del laboratorio y
    descargue el archivo.

    ![](./media/image2.png)

2.  Navegue a Copilot: Abra una nueva pestaña en Microsoft Edge y vaya a
    https://M365copilot.com. Inicie sesión con las credenciales de
    nombre de usuario y contraseña proporcionadas en la pestaña de
    Resources en el panel derecho de su entorno de laboratorio**.**

    ![](./media/image3.png)

    ![](./media/image4.png)

    ![](./media/image5.png)

3.  En Microsoft 365, abra el agente **Analyst** (Agents → Analyst).

    ![](./media/image6.png)

4.  Si no es visible, haga clic en el icono **Expand navigation**,
    seleccione **Agents** y seleccione **Analyst Agent** (Built by
    Microsoft 365 Copilot).

    ![](./media/image7.png)

    ![](./media/image8.png)

5.  Haga clic en el icono **Add content and agents (+)** del campo de
    prompt → **Upload from this device** → seleccione el archivo
    **Project Nexus** descargado.

    ![](./media/image9.png)

    ![](./media/image10.png)

**Nota:** Después de que el archivo se carga, está listo para comenzar a
explorar e interactuar con el **Analyst** **Agent**.

# Ejercicio 2: Ejecutar prompts iniciales

1.  En el campo de prompt, escriba: ***Analyse this spreadsheet and tell
    me the top three trends*.** Espere a que el agente **Analyst**
    ejecute su análisis y valide la respuesta.

    ![](./media/image11.png)

    ![](./media/image12.png)

    **Nota**: la página advierte sobre la posible aparición de un espacio en
    blanco grande en la UI; desplácese hacia arriba para ver los resultados
    si aparece.

    ![](./media/image13.png)

2.  **Prompts de seguimiento:**

    En el campo de prompt, escriba el siguiente prompt y valide la respuesta
del agente.

    ***“ What is the average rating for each survey category?”***

    ![](./media/image14.png)

    ![](./media/image15.png)

    ![](./media/image16.png)

    ![](./media/image17.png)

# Ejercicio 3 : Pruebe prompts adicionales (cuantitativos, cualitativos y de visualización)

Para explorar tipos adicionales de prompts de análisis más allá de los
ejemplos predefinidos y comprender cómo cada categoría (cuantitativa,
cualitativa y de visualización) puede generar diferentes insights a
partir del mismo conjunto de datos.

Prompts de análisis cuantitativo**:**

El agente busca obtener información numérica o medible a partir de los
datos.

### Prompt: 

- **How many participants rated the project satisfaction as 4 or
  higher**?

    ![](./media/image18.png)

### Resumen de la respuesta:

- A total of **22 participants** rated the project satisfaction as **4
  (Good)** or **5 (Excellent)** in the *Project Nexus* survey. Un total
  de **22 participantes** calificaron la satisfacción del proyecto con
  **4 (Good)** o **5 (Excellent)** en la encuesta de *Project Nexus*.

- El desglose detallado de las calificaciones es:

  - (Poor): 11 respuestas

  - (Fair): 7 respuestas

  - (Neutral): 10 respuestas

  - (Good): 14 respuestas

  - (Excellent): 8 respuestas

    - El cálculo: **14 (Good) + 8 (Excellent) = 22 participantes** que
    expresaron satisfacción positiva.

    ![](./media/image19.png)

### Prompt 2: 

- **“Which category received the highest average rating, and which
  received the lowest**?”

![](./media/image20.png)

### Resumen de la respuesta:

    - El **Analyst** analizó los datos del archivo
    **Project_Nexus_survey_results.xlsx** y proporcionó **calificaciones
    promedio** en cuatro categorías clave.

    - 📊 Resumen de calificaciones promedio

    | Categoía  |Calificación promedio   |
    |:------|:------|
    | Satisfacción del proyecto  | 3.02  |
    | Efectividad de la comunicación  | 2.92  |
    |  Cumplimiento del cronograma |  2.98 |
    | Experiencia general  | 2.98  |

![](./media/image21.png)

Prompts de análisis cualitativo**:**

El agente busca explorar **opiniones, experiencias, percepciones o
información descriptiva** a partir de los datos, en lugar de valores
numéricos.

### Prompt 1: 

- “**Summarize the most common themes in the comments section**.”

![](./media/image22.png)

### Resumen de la respuesta: 

- El **Analyst** identificó **temas clave** a partir de los comentarios
  de los participantes relacionados con la satisfacción del proyecto.

- Cada tema incluye el **número de menciones** y **comentarios de
  ejemplo** que representan la retroalimentación de los participantes.

![](./media/image23.png)

![](./media/image24.png)

### Prompt 2: 

- “**Are there any recurring concerns or suggestions mentioned in the
  comments**?”

![](./media/image25.png)

### Resumen de la respuesta: 

- El **Analyst** identificó **inquietudes y sugerencias recurrentes** a
  partir de los comentarios de la encuesta de Project Nexus.

![](./media/image26.png)

![](./media/image27.png)

## Prompts de insights y recomendaciones

El Analyst **interpreta los hallazgos de los datos, extrae conclusiones
significativas** y **sugiere próximos pasos accionables** basados en el
análisis.

### Prompt 1: 

- “**Based on the survey data, what are the top three strengths of
  Project Nexus**?”

![](./media/image28.png)

### Resumen de la respuesta:

- El **Analyst** identificó las **principales** **fortalezas** a partir
  de los datos y comentarios de la encuesta de *Project Nexus*.

![](./media/image29.png)

![](./media/image30.png)

### Prompt 2: 

- **“What are the key areas for improvement suggested by the
  participants**?”

![](./media/image31.png)

### Resumen de la respuesta:

- El **Analyst** destacó **Communication** como el **área**
  **principal** **de** **mejora**, con base en los comentarios de los
  participantes de la encuesta de Project Nexus .

![](./media/image32.png)

## Prompts de visualización cuantitativa

**El Analyst presenta datos numéricos de forma visual** — mediante
gráficos, diagramas o tablas — para facilitar la interpretación y
comparación de los hallazgos cuantitativos.

### Prompt 1: 

- **“Generate a pie chart of overall ratings distribution**.”

![](./media/image33.png)

### Resumen de la respuesta:

- El **Analyst** generó un **gráfico circular** para representar
  visualmente la **distribución de las calificaciones de Overall
  Experience** de la encuesta *Project Nexus*.

![](./media/image34.png)

![](./media/image35.png)

### Prompt 2:

**“ Create a bar chart comparing the average ratings for Project
Satisfaction, Communication Effectiveness, Timeline Adherence, and
Overall Experience**.”

![](./media/image36.png)

![](./media/image37.png)

### Resumen de la respuesta:

- El **Analyst** creó un **gráfico de barras** que visualiza las
  **calificaciones promedio** en cuatro categorías clave de la encuesta
  Project Nexus y proporcionó un resumen numérico.

![](./media/image38.png)

![](./media/image39.png)

# Ejercicio 4: Instrucción para un elemento accionable para el usuario final

Realice un análisis de datos integral de los resultados de la encuesta
*Project Nexus* utilizando diferentes tipos de prompts analíticos. Cada
tipo de prompt se enfoca en extraer insights específicos o
visualizaciones a partir del conjunto de datos.

1.  **Prompts de análisis cuantitativo**

Utilice estos prompts para analizar **datos** **numéricos** e
identificar patrones o relaciones medibles.

- **Prompts:**

  - *“What percentage of participants rated timeline adherence below
    3?”*  
    → Esto calculará la proporción de participantes que otorgaron
    calificaciones bajas al cumplimiento del cronograma.

  - *“Can you identify any correlations between communication
    effectiveness and overall experience?”*  
    → El Analyst calculará el coeficiente de correlación e interpretará
    qué tan fuerte es la relación entre estas dos categorías.

- **Resultado esperado:**  
  Un resumen numérico que muestre porcentajes, promedios o valores de
  correlación que revelen patrones en las calificaciones de los
  participantes.

2.  Prompts de análisis cualitativo

Utilice estos prompts para extraer e interpretar **comentarios textuales
o descriptivos** de las respuestas abiertas de la encuesta.

- **Prompts:**

  - *“Identify any comments that mention issues with communication or
    timeline.”*  
    → Esto filtrará los comentarios que contengan palabras clave
    específicas o preocupaciones relacionadas.

  - Revise los comentarios extraídos para identificar frases o temas
    recurrentes.

- **Resultado esperado:**  
  Una lista categorizada de insights cualitativos que resalten patrones
  de retroalimentación relacionados con la comunicación y el cronograma
  del proyecto.

3.  Prompts de insights y recomendaciones

Utilice estos prompts para **resumir** **los** **hallazgos** y
**generar** **recomendaciones** **accionables** basadas tanto en datos
cuantitativos como cualitativos.

- **Prompts:**

&nbsp;

- *“Provide a summary report of the survey findings with actionable
  recommendations.”*  
  → El Analyst recopilará los puntos clave, destacará fortalezas y
  debilidades, y sugerirá acciones de mejora.

- **Resultado esperado:**  
  Un reporte resumido que contenga insights estratégicos y
  recomendaciones para mejorar el desempeño de proyectos futuros.

4.  Prompts de visualización cuantitativa

Utilice estos prompts para crear **visualizaciones** **de** **datos**
que hagan los resultados numéricos más fáciles de interpretar y listos
para presentarse.

- **Prompts:**

- Ejecute cada uno de los siguientes prompts de forma secuencial para
  generar diferentes tipos de gráficos:

  - *“Plot a histogram of the satisfaction ratings to see the
    distribution of ratings.”*

  - *“Generate a scatter plot to analyze the relationship between
    Communication Effectiveness and Overall Experience.”*

  - *“Create a correlation heatmap for all numeric rating categories.”*

  - *“Make a box plot for each rating category to show the range and
    quartiles.”*

  - *“Plot a line graph showing timeline adherence ratings over
    participants ordered by Participant ID.”*

- Revise cada visualización para identificar tendencias de datos,
  relaciones y valores atípicos.

- **Resultado esperado:**  
  Una serie de gráficos (histograma, gráfico de dispersión, mapa de
  calor, diagrama de caja y gráfico de líneas) que representen
  visualmente los datos de la encuesta y faciliten la comparación y
  extracción de insights.

# Ejercicio 4: Exportar y reutilizar la respuesta del Analyst Agent

## Qué puede hacer con la respuesta

A continuación, se presenta una breve descripción de las tareas
asociadas a cada icono que se muestra en su captura de pantalla:

![](./media/image40.png)

1.  **📋 Icono de Clipboard** – Probablemente se utiliza para **copiar o
    pegar contenido**.

2.  **👍 Icono de Thumbs-Up** – Normalmente indica que se da **“me
    gusta”** o **se** **aprueba** un elemento o acción.

3.  **👎 Icono de Thumbs-Down** – Generalmente se utiliza para
    **indicar** **que** **no** **gusta** o se **desaprueba** algo.

4.  **🔊 Icono de Speaker** – Representa **configuraciones de audio o
    control de volumen**.

5.  **✏️ Icono de Pencil** – Se utiliza comúnmente para tareas de
    **edición** **o** **escritura**.

6.  **🕒 Icono de Clock with Arrow** – El tooltip indica **“Add to
    recent page”**, lo que significa que agrega el elemento actual a las
    **páginas accedidas recientemente** para una referencia rápida.

## Botón Copy (icono 📋)

- Permite al usuario **copiar** directamente el **texto del resumen, la
  explicación o los datos** desde la respuesta del Analyst.

- **Uso:**

Cuando se selecciona, copia la **parte de texto** de la respuesta del
Analyst (no la imagen del gráfico) al portapapeles.

Esto es útil si **desea pegar los datos o el resumen** en un reporte,
documento o presentación.

- **Ejemplo de caso de uso:**  
  Puede copiar “22 participants rated the project satisfaction as 4 or
  higher” para incluirlo en su archivo de resumen del proyecto.

> ![](./media/image41.png)
>
> ![](./media/image42.png)

## Botón Download (⤓ o icono ⬇)

- **Propósito:** Permite al usuario **descargar** **la**
  **visualización** (como el **gráfico** **circular**) como un archivo
  de **imagen (por ejemplo, PNG)**.

- **Uso:**

Al hacer clic, se guarda la imagen del gráfico en el sistema local.

Posteriormente, se puede insertar en **diapositivas de PowerPoint,
documentos de Word o informes** para su representación visual.

- **Ejemplo de uso:**  
  Puede descargar el gráfico circular **“Distribution of Overall
  Experience Ratings”** para incluirlo en su presentación de análisis de
  la encuesta.

# ![](./media/image35.png)

# Sugerencias de solución de problemas y validación

- Si la UI del agente muestra un gran espacio en blanco: desplácese
  hacia arriba o hacia abajo; el contenido normalmente está presente (el
  módulo lo indica como un problema conocido).

- Si las columnas numéricas se tratan como texto: abra la hoja de
  cálculo, asegúrese de que las columnas de calificación sean numéricas
  y vuelva a cargar el archivo.

- Si los gráficos no aparecen, solicítelo explícitamente al agente:
  Please generate a bar chart comparing average ratings for \[list
  categories\].

# Aprendizajes clave

1.  **Conexión y carga de datos:**  
    Aprendió a abrir el Analyst Agent, cargar el archivo de Excel
    *Project Nexus Survey Results* e iniciar el proceso de análisis
    dentro de Microsoft 365 Copilot.

2.  **Ejecución de prompts iniciales:** Practicó el uso de prompts
    básicos para identificar las **principales** **tendencias** y
    calcular **promedios**, asegurando que puede obtener rápidamente
    insights cuantitativos a partir de conjuntos de datos cargados.

3.  **Exploración de diferentes tipos de prompts:**  
    Realizó una exploración más profunda de los datos utilizando cuatro
    categorías clave de prompts analíticos:

    - **Prompts cuantitativos** – para calcular métricas, promedios y
      correlaciones.

    - **Prompts cualitativos** – para interpretar los comentarios de los
      participantes e identificar temas.

    - **Prompts de insights y recomendaciones** – para resumir hallazgos
      y sugerir acciones de mejora.

    - **Prompts de visualización cuantitativa** – para crear
      representaciones visuales claras de resultados numéricos (por
      ejemplo, gráficos circulares, gráficos de barras y mapas de
      calor).

4.  **Ejecución de un análisis integral:**  
    Mediante el ejercicio de elementos accionables, integró todos los
    tipos de prompts para realizar un **análisis** **de** **extremo**
    **a** **extremo**, combinando hallazgos numéricos, descriptivos y
    visuales para una interpretación integral.

5.  **Exportación y reutilización de resultados:**  
    Aprendió a usar los botones **Copy (📋)** y **Download (⬇)** en el
    Analyst Agent para extraer resúmenes de texto o guardar
    visualizaciones de gráficos para informes y presentaciones.

6.  **Solución de problemas:**  
    También revisó métodos para manejar problemas comunes de la
    interfaz, como gráficos que no se muestran o columnas numéricas sin
    el formato adecuado.
