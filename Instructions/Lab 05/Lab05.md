# Laboratorio 05: Crear un Copilot Agent en SharePoint

Duración del laboratorio: 10-15 minutos

## Introducción

A medida que las organizaciones dependen cada vez más de SharePoint para
administrar el conocimiento, los proyectos y los recursos de los
equipos, la capacidad de crear agentes inteligentes que interactúen con
este contenido se convierte en un potente impulsor de productividad.
Microsoft 365 Copilot permite crear un Copilot agent basado en
SharePoint que puede mostrar información rápidamente, responder
preguntas y ayudar a los usuarios a navegar por contenido complejo del
sitio.

## Objetivo

En este laboratorio, aprenderá a:

1.  Crear un Copilot Agent en SharePoint.

2.  Personalizar **el** **nombre, el icono y el propósito del agente**.

3.  Agregar **orígenes** **de** **conocimiento** como sitios de
    SharePoint, bibliotecas o archivos.

4.  Configurar el comportamiento del agente, incluido el **mensaje de
    bienvenida,** los **starter prompts** y las **instrucciones**.

5.  **Publicar y probar** su agente.

## Requisitos previos

1.  Debe tener acceso a un sitio de SharePoint con **permisos de Edit o
    superiores**.

2.  Asegúrese de que **Microsoft Copilot for Microsoft 365** esté
    habilitado en su tenant.

3.  Y Debe haber iniciado sesión en su sitio de **SharePoint Online** a
    través de **Microsoft** **365**.

## Ejercicio 1: Acceder a la herramienta de creación de Copilot Agent

Debe comenzar identificando un sitio de SharePoint al que ya tenga
acceso.

1.  Inicie sesión en el **sitio** **de** **SharePoint**.

- Seleccione el enlace proporcionado y abra la página de inicio de
  sesión de Microsoft SharePoint

> https://www.microsoft.com/en/microsoft-365/sharepoint/collaboration?market=af

![](./media/image1.png)

2.  Seleccione **Sign** **in** y proporcione las credenciales de usuario
    indicadas en su entorno, en la pestaña **Resources**, para iniciar
    sesión en el sitio de SharePoint

> ![](./media/image2.png)
>
> ![](./media/image3.png)

- Haga clic en **Yes** para permanecer con la sesión iniciada.

> ![](./media/image4.png)
>
> ![](./media/image5.png)

3.  En el sitio de SharePoint, abra un sitio existente. Si no tiene un
    sitio existente, cree uno nuevo.

4.  Seleccione **Create** **site** en la esquina superior izquierda de
    la página principal del sitio de SharePoint para crear un nuevo
    sitio.

> ![](./media/image6.png)

5.  En este caso, se selecciona el sitio de comunicación existente de
    SharePoint llamado **ContosoSite**.

![](./media/image7.png)

## Ejercicio 2: Crear su nuevo agente

1.  Crear un nuevo agente para **ContosoSite**

- En la **página** **principal** de ContosoSite, seleccione + **New**
  **→** **Agent**.

![](./media/image8.png)

2.  **Abrir la página de creación del agente**  
    Verá tres pestañas principales en la parte superior: **Overview**,
    **Sources** y **Behavior**. Estas pestañas le ayudan a definir la
    configuración y la funcionalidad del agente.

### Ejercicio 2.1: Configurar la pestaña Overview del agente

1.  En la pestaña **Overview**:

    - Ingrese el **Agent Name** : Project Knowledge Assistant

![](./media/image9.png)

- Proporcione una **Description**: Helps users find project documents
  and summaries

![](./media/image10.png)

- (Opcional) Seleccione **Change** **icon** y cargue un archivo .png
  (tamaño máximo: 1 MB).

![](./media/image11.png)

### Ejercicio 2.2: Agregar orígenes de conocimiento

1.  Navegue a la pestaña **Source** en la ventana Create new agent.

> ![](./media/image12.png)

2.  Elija una de las siguientes opciones:

    - **Source from entire site** (predeterminado)

    - **Sourced from document libraries, folders, or files**

**Nota:** En este ejercicio se utiliza el origen predeterminado.

3.  Si selecciona Sourced from document libraries, folders, or files:

    - Haga clic en + Add document libraries, folders, or files.

    - En la ventana Pick items, elija:

    - La biblioteca Documents completa, o

    - Carpetas/archivos específicos (seleccione las casillas
      correspondientes).

    - Seleccione Select.

![](./media/image13.png)

**Nota**: Puede agregar hasta 20 orígenes para un solo agente.

### Ejercicio 2.3: Definir el comportamiento del agente

1.  Navegue a la pestaña **Behavior** en la ventana Create new agent.

> ![](./media/image14.png)

2.  Configure lo siguiente:

- Welcome Message:  
  *+++*Hi! I can help you locate project documents and summarize
  updates*+++*

- Starter Prompts (máx. 3):

  1.  +++Summarize the latest project updates.+++

  2.  +++Find budget-related documents.+++

  3.  +++Who authored the project plan?+++

> ![](./media/image15.png)

- **Instructions:**  
  +++Provide concise answers using only verified information from
  included SharePoint sources.+++

![](./media/image16.png)

3.  Seleccione **Save** **and** **close** para guardar todas las
    configuraciones.

## Ejercicio 3: Probar su agente

1.  Después de guardar, abra el **panel de chat de Copilot**.

- Seleccione **Chat** **with** **agent** para abrir la ventana de chat
  del agente en **ContosoSite**.

> ![](./media/image17.png)

- Ahora verá el panel del agente **Project** **Knowledge** **Assistant**
  en el lado derecho de **ContosoSite**.

- También puede cambiar entre agentes desde el menú desplegable de
  agentes.

> ![](./media/image18.png)
>
> ![](./media/image19.png)

2.  Ingrese uno de los starter prompts en el campo de chat del agente:

> **Prompt**: +++Summarize the project plan+++
>
> ![](./media/image20.png)

3.  Observe la respuesta.

- Como se muestra en la imagen, el agente **Project Knowledge
  Assistant** no devuelve detalles específicos de informes del proyecto.

- Esto ocurre porque el origen de **ContosoSite** actualmente **no
  contiene archivos de informes del proyecto ni datos relacionados**.

> ![](./media/image21.png)
>
> **Nota**: Puede cargar un documento o un informe de proyecto en la
> biblioteca de ContosoSite.

4.  Cargue un documento en la biblioteca de **ContosoSite**.

- Vaya a la página principal de ContosoSite y seleccione **Toggle**
  **navigation** **pane.**

- Seleccione la opción Seleccione la opción **Documents** en el menú
  desplegable en el menú desplegable.

![](./media/image22.png)

- Verá la biblioteca documents vacía de ContosoSite.

- Haga clic en **Upload** y seleccione el **archivo**, **carpeta** o
  **plantilla** que desea cargar en la biblioteca del sitio.

> ![](./media/image23.png)
>
> ![](./media/image24.png)

- Seleccione el archivo desde su **OneDrive** y seleccione **Open** para
  cargarlo.

> ![](./media/image25.png)
>
> ![](./media/image26.png)

- Su archivo de **resultados** **de la** **encuesta** **Project Nexus**
  se carga correctamente en la biblioteca documents de **ContosoSite**.

> ![](./media/image27.png)

5.  Pruebe su agente con el nuevo origen predeterminado Project Nexus
    Survey results.

- ngrese el prompt en el panel de chat del agente y valide la respuesta.

Prompt: +++**Summarise the latest project updates**+++ .

- El agente responde con información precisa basada únicamente en el
  contenido de SharePoint incluido como origen.

> ![](./media/image28.png)
>
> ![](./media/image29.png)

## Resumen

En este laboratorio, usted:

- Creó un nuevo **Copilot Agent** en SharePoint.

- Personalizó **su nombre, descripción e icono**.

- Definió los **orígenes de conocimiento** y la **configuración de
  comportamiento**.

- Publicó y probó su agente.

Ahora comprende cómo los SharePoint Copilot Agents ayudan a optimizar la
**recuperación de información, la colaboración y la automatización de
flujos de trabajo** utilizando los datos que ya están disponibles en su
entorno de SharePoint.
