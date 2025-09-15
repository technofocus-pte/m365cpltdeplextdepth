# Laboratorio 6 - Amplíe Microsoft 365 Copilot Chat con un HR Agent construido mediante Microsoft Copilot Studio

**Objetivo**

En este laboratorio, aprenderá a ampliar el chat de Microsoft 365
Copilot con un agente declarativo creado con Microsoft Copilot Studio.
 También aprenderá a agregar una acción personalizada al agente que
realizó.

Duración estimada – 45 minutos

## Ejercicio 1: Cree un Power Platform environment

Con Power Platform, puede crear diferentes entornos y cambiar fácilmente
entre ellos de acuerdo con sus necesidades. Un entorno almacena
aplicaciones, flujos, datos, agentes, etc. y cada entorno está
completamente aislado de cualquier otro entorno. En este ejercicio,
creará un nuevo entorno dedicado en el que realizará los ejercicios y
tareas restantes.

1.  Abra un navegador y, utilizando sus credenciales de inicio de sesión
    desde la pestaña **Resources**, vaya
    a [https://admin.powerplatform.com](https://admin.powerplatform.com/).

![](./media/image1.png)

2.  Seleccione **Manage** y seleccione **+ New** en **Environments**.

![](./media/image2.png)

3.  Proporcione el nombre como +++**Dev env**+++, seleccione el **Type**
    como **Developer** y haga clic en **Next**. Seleccione **Save** en
    la pantalla **Add Dataverse**.

![](./media/image3.png)

![](./media/image4.png)

4.  El nuevo entorno se crea y cambia de **Preparing** a **Ready** una
    vez que esté listo.

![](./media/image5.png)

![](./media/image6.png)

## Ejercicio 2: Cree un agente para Microsoft 365 Copilot Chat

En este ejercicio va a crear un agente declarativo con Microsoft Copilot
Studio y alojarlo en Microsoft 365 Copilot Chat.

1.  Inicie sesión en <https://copilotstudio.microsoft.com/> con las
    credenciales en la pestaña **Resources**.

![](./media/image7.png)

2.  Seleccione el entorno **Dev env** que creamos en el ejercicio
    anterior.

![](./media/image8.png)

3.  Para crear un agente declarativo para Microsoft 365 Copilot Chat,
    primero debe examinar la lista de agentes en Copilot Studio y, a
    continuación, seleccionar el agente con nombre **Microsoft 365
    Copilot**.

4.  Seleccione **Agents** en la barra de navegación izquierda y
    seleccione **Copilot for Microsoft 365** desde la lista.

![](./media/image9.png)

5.  Se abrirá una nueva sección de Microsoft Copilot Studio. Desde allí,
    seleccione el comando **+ Add** para crear un nuevo agente para
    Microsoft 365 Copilot Chat.

![](./media/image10.png)

6.  Copilot Studio le pide que describa en lenguaje natural cuál es el
    propósito del agente. Puede definir los requisitos de su agente.
    Pegue el prompt a continuación para hacerlo

> **+++You are an agent helping employees to find information about HR
> policies and procedures, about how to improve their career, and about
> how to define learning pathways.+++**

![](./media/image11.png)

7.  Cuando Copilot Studio lo solicite, asigne el nombre "Agentic HR" a
    su agente personalizado. Utilice el siguiente prompt.

+++Name it as Agentic HR+++

![](./media/image12.png)

8.  A continuación, indique a Copilot Studio que tenga tareas u
    objetivos específicos con las siguientes instrucciones:

**+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++**

![](./media/image13.png)

9.  A continuación, defina un tono profesional para su agente,
    proporcionando la siguiente información:

**+++It should have a professional tone+++**

![](./media/image14.png)

10. Una vez que haya terminado de describir su agente, seleccione el
    comando **Create** para crear el agente real. 

![](./media/image15.png)

![](./media/image16.png)

## Ejercicio 3: Publique el agente en Microsoft 365 Copilot Chat

1.  Seleccione **Publish** desde la página de agent overview.

![](./media/image17.png)

2.  Seleccione **Publish** en la pantalla **Publish agent**.

![](./media/image18.png)

> ![](./media/image19.png)

3.  Seleccione **Copy** en **Share link** para copiar el vínculo y, a
    continuación, seleccione **Done**.

![](./media/image20.png)

4.  Abra una nueva pestaña y pegue la URL copiada. Seleccione **Add**
    para añadir el **Agentic HR** a su lista de agentes.

![](./media/image21.png)

![](./media/image22.png)

5.  Seleccione **Skip** en la pantalla de introducción.

![](./media/image23.png)

6.  Se ha agregado el agente **Agentic HR**.

![](./media/image24.png)

## Ejercicio 4: Cree un sitio SharePoint

1.  En un nuevo navegador, navegue a
    +++https://m365.cloud.microsoft/chat/+++ Seleccione **Apps** desde
    el panel de navegación y seleccione **SharePoint** una vez que se
    carga las Apps.

> ![](./media/image25.png)

2.  Seleccione el sitio **+ Create** desde la página de SharePoint.

![](./media/image26.png)

3.  Seleccione el sitio **Communication** desde la página **Select the
    site type**.

![](./media/image27.png)

4.  Seleccione una **plantilla** para usar.

![](./media/image28.png)

5.  Seleccione **Use template**.

![](./media/image29.png)

6.  Introduzca +++**Contoso site+++** como **Site name** y seleccione
    **Next.**

![](./media/image30.png)

7.  En la siguiente pantalla, seleccione **Create site**.

![](./media/image31.png)

8.  Una vez creado, anote la **URL** de este sitio.

![](./media/image32.png)

9.  Seleccione **Documents** en la barra de menús. Seleccione **Upload
    -\> Files**

![](./media/image33.png)

10. Seleccione el archivo **Sample-list-of-candidates.xlsx** desde
    **C:\LabFiles** para subir.

![](./media/image34.png)

## Ejercicio 5: Adición de una acción al agente

En este ejercicio, agregará una acción personalizada al agente que creó.
En Microsoft Copilot Studio, al crear agentes para Microsoft 365 Copilot
Chat, puede agregar cuatro tipos diferentes de acciones:

- New prompt: permite consumir una acción de IA construida a partir de
  un prompt escrito en lenguaje natural.

- New Power Automate flow: permite consumir un Power Automate flow.

- New custom connector: permite consumir un conector personalizado de
  Power Platform.

- New REST API: permite consumir una API REST externa.

1.  Para agregar una nueva acción, seleccione **+ Add action** en la
    sección **Actions** del panel de configuración del agente.

![](./media/image35.png)

2.  Seleccione la opción **List rows present in a table**(Excel online)
    y seleccione **Next.**

![](./media/image36.png)

![](./media/image37.png)

3.  En la pantalla **List rows present in a table**, proporcione los
    siguientes detalles y seleccione **Add action**.

Name - +++List HR candidates+++

Description – +++List candidates for HR role+++

![](./media/image38.png)

![](./media/image39.png)

4.  Una vez agregada la acción, haga clic en ella para abrirla y
    editarla.

![](./media/image40.png)

5.  Seleccione la sección **Inputs**.

![](./media/image41.png)

6.  Seleccione **Set as a value** en **How will the agent fill this
    input** para cada uno de los argumentos de entrada.

![](./media/image42.png)

7.  Seleccione **Confirm** en el cuadro de diálogo Change input
    settings.

![](./media/image43.png)

![](./media/image44.png)

8.  Proporcione los siguientes valores para cada entrada.

**Location** – La dirección URL del sitio de Contoso que guardó en el
ejercicio anterior.

Document Library – +++**Documents**+++

File – +++**Sample-list-of-candidates.xlsx**+++

Table – +++**Candidates_Table**+++

![](./media/image45.png)

![](./media/image46.png)

![](./media/image47.png)

9.  Una vez que se hayan realizado todas las actualizaciones, seleccione
    **Save**.

![](./media/image48.png)

![](./media/image49.png)

10. Seleccione **Publish** para publicar el agente.

![](./media/image50.png)

11. Seleccione **Publish** de nuevo.

![](./media/image51.png)

12. **Copie** el url y **ábralo** desde un navegador.

![](./media/image52.png)

13. Esta vez, dará una opción para **Update now** ya que ya está
    agregado. Selecciónalo.

![](./media/image53.png)

14. Seleccione **Open** una vez que se actualiza.

![](./media/image54.png)

15. En la pantalla del agente de Agentic HR, envíe el siguiente mensaje.

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image55.png)

16. En el mensaje Data to be shared with Agentic HR, seleccione la
    opción **Allow once**.

![](./media/image56.png)

17. Si le pide que inicie sesión, seleccione la opción **Sign in to
    Agentic HR** y seleccione **Connect** en la siguiente pantalla.

![](./media/image57.png)

![](./media/image58.png)

18. Seleccione **Submit** una vez conectado.

![](./media/image59.png)

![](./media/image60.png)

19. Ahora, vuelva a enviar el siguiente mensaje al agente.

+++Show me a list of candidates for HR with role “HR Director” or ”HR
Manager”+++

![](./media/image61.png)

20. A continuación, recibirá la lista solicitada

![](./media/image62.png)

![](./media/image63.png)

## Resumen

En este laboratorio, ha aprendido con éxito cómo usar conectores
personalizados en Copilot Studio.
