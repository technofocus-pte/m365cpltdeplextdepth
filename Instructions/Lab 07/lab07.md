# Construya un agente declarativo poético usando Microsoft 365 Agents Toolkit

**Objetivo**

Un agente declarativo es una versión personalizada de Microsoft 365
Copilot que permite a los usuarios crear experiencias personalizadas
mediante la declaración de instrucciones, acciones y conocimientos
específicos. En esta guía se proporciona información sobre cómo crear un
agente declarativo mediante el kit de herramientas de agentes de
Microsoft 365 (una evolución del kit de herramientas de Teams).

En este laboratorio, creará un agente declarativo poético.

## Ejercicio 1: Cree un declarative agent

En este ejercicio, comenzará con la creación de un agente declarativo
básico a partir de Visual Studio Code.

1.  Desde el VM, abra **Visual Studio Code**.

2.  Seleccione **Extensions** en el panel izquierdo y escriba
    +++Microsoft 365 Agents Toolkit+++

![](./media/image1.png)

3.  Seleccione el **Microsoft 365 Agents Toolkit** y seleccione
    **Install** para instalar la extensión.

![](./media/image2.png)

4.  Seleccione **Declarative Agent**.

![](./media/image3.png)

5.  Seleccione **No Action** Para crear un agente declarativo básico.

![](./media/image4.png)

6.  Seleccione **Default folder** para almacenar la carpeta root del
    proyecto en la ubicación predeterminada.

![](./media/image5.png)

7.  Introduzca +++My Agent+++ como **Application Name** y haga clic
    en **Enter**.

![](./media/image6.png)

8.  En la nueva ventana Visual Studio Code que abre,
    seleccione **Microsoft 365 Agents Toolkit**.

![](./media/image7.png)

9.  Seleccione **Provision** en el panel **Lifecycle** y seleccione
    **Sign in** en el popup que aparece, para iniciar sesión en la
    cuenta de Microsoft 365.

![](./media/image8.png)

10. **Inicie sesión** con las credenciales desde la pestaña Resources y
    cierre la ventana una vez hecho.

![](./media/image9.png)

11. Ahora, se realiza la creación básica del agente declarativo.

### Tarea 1: Pruebe el agente

En esta tarea, probaremos el agente declarativo que hemos creado.

1.  Vaya a la aplicación Copilot con la
    URL <https://m365.cloud.microsoft/chat>.

2.  En la parte superior izquierda, **seleccione el icono**
    **conversation drawer**.

> ![](./media/image10.png)

3.  Seleccione el declarative agent **My Agent**.

> ![](./media/image11.png)

4.  Introduzca una pregunta +++Hello! How can you help me?+++ para su
    agente declarativo y asegúrese de que responda con "Thanks for using
    Microsoft 365 Agents Toolkit to create your declarative agent!"

> ![](./media/image12.png)
>
> En este ejercicio, hemos creado un agente declarativo básico y hemos
> probado su funcionalidad.

## Ejercicio 2: Agregue instrucciones

En este ejercicio, comenzaremos a agregar instrucciones al agente
declarativo que creamos en el ejercicio anterior y lo mejoraremos

1.  Desde Visual Studio Code, abra el
    archivo **appPackage/instructions.txt** y sustitúyase su contenido
    por el texto siguiente.

> <span class="mark">You are a declarative agent and were created with
> Microsoft 365 Agents Toolkit. You are an expert at creating
> poems.</span>
>
> <span class="mark">Every time a user asks a question, you **must**
> turn the answer into a poem. The poem **must** not use the quote
> markdown and use regular text.</span>
>
> ![](./media/image13.png)

El contenido de este archivo se inserta en la propiedad instructions del
manifiesto del agente durante el aprovisionamiento.

2.  Seleccione **Provision** en el panel **Lifecycle** del Agents
    Toolkit.

![](./media/image14.png)

3.  Compruebe que el **aprovisionamiento** se ha completado
    **correctamente**. Puede ver un mensaje en la parte inferior derecha
    de la Visual Studio Code.

> ![](./media/image15.png)

4.  El agente declarativo usará las instrucciones actualizadas después
    de volver a cargar la página.

5.  Actualice la página de chat, seleccione **My Agent** y tecle +++Do
    we have chocolate in our food catalog?+++

![](./media/image16.png)

6.  Obsérvese que el agente da una respuesta poética.

![](./media/image17.png)

7.  Ahora, agregue iniciadores de conversación al agente.

8.  Abra el archivo **appPackage/declarativeAgent.json** y justo después
    del nodo de instrucciones, agregue una **coma** , presione Enter y
    pegue el código debajo.

"conversation_starters": \[

        {

            "title": "Getting Started",

            "text": "How can I get started with Agents Toolkit?"

        },

        {

            "title": "Getting Help",

            "text": "How can I get help with Agents Toolkit?"

        }

    \]

![](./media/image18.png)

9.  Seleccione **Provision** en el panel Lifecycle del **Microsoft 365
    Agents Toolkit** y asegúrese de que el aprovisionamiento se complete
    correctamente.

10. Los iniciadores de conversación actualizados estarán disponibles en
    el agente declarativo después **de actualizar** la página.

11. **Actualice** la página de chat para comprobar lo mismo.

![](./media/image19.png)

## Ejercicio 3: Agregue contenido web

En este ejercicio, agregará la capacidad al agente para buscar el
contenido web.

1.  Abra el archivo **appPackage/declarativeAgent.json** y agregue la
    matriz capabilities con el siguiente contenido.

> "capabilities": \[
>
> {
>
> "name": "WebSearch"
>
> }
>
> \]
>
> ![](./media/image20.png)

2.  Seleccione **Provision** en el panel Lifecycle del **Microsoft 365
    Agents Toolkit** y asegúrese de que el aprovisionamiento se complete
    correctamente.

> ![](./media/image21.png)
>
> El agente declarativo tendrá acceso al contenido web para generar sus
> respuestas después de volver a cargar la página.

3.  Pregúntele al agente, +++How can I build a declarative agent?+++ y
    observe que el agente responde desde la web.

> ![](./media/image22.png)

## Resumen

Ha aprendido a crear el agente declarativo para Microsoft 365 Copilot.
También ha aprendido a mejorar el agente creado con instrucciones y
contenido web y a probarlo en cada etapa.
