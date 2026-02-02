# Laboratorio 6 - Extender Microsoft 365 Copilot Chat con un HR Agent creado con Microsoft Copilot Studio

**Escenario**

Zava Ltd. es una empresa global de servicios profesionales y soluciones
tecnológicas con una fuerza laboral distribuida. La organización utiliza
Microsoft 365, SharePoint y Power Platform para administrar las
operaciones de RR. HH., el aprendizaje de los empleados y los datos de
reclutamiento.

Zava busca mejorar la experiencia de los empleados al permitir un acceso
rápido y conversacional a información relacionada con RR. HH.
directamente desde Microsoft 365 Copilot Chat. Los empleados preguntan
con frecuencia sobre políticas de RR. HH., oportunidades de crecimiento
profesional, rutas de aprendizaje y datos de reclutamiento almacenados
en sitios de SharePoint.

Para abordar esta necesidad, los equipos de TI y RR. HH. de Zava deciden
crear un HR agent dedicado mediante Microsoft Copilot Studio. Este
agente se definirá de forma declarativa, se hospedará dentro de
Microsoft 365 Copilot Chat y se enriquecerá con conocimiento
organizacional almacenado en SharePoint. La solución debe construirse en
un entorno seguro y aislado de Power Platform e integrarse de forma
fluida en la experiencia de Microsoft 365.

**Objetivo**

Al completar este laboratorio, usted aprenderá a:

- Crear y administrar un entorno dedicado de Power Platform para el
  desarrollo de agentes.

- Crear un agente declarativo con Microsoft Copilot Studio para
  Microsoft 365 Copilot Chat.

- Definir el propósito, el tono y los objetivos de comportamiento del
  agente mediante prompts en lenguaje natural.

- Publicar e implementar el agente en Microsoft 365 Copilot Chat.

- Crear y configurar un sitio de comunicación de SharePoint para
  hospedar datos de RR. HH.

- Agregar orígenes de conocimiento basados en SharePoint a un agente de
  Copilot Studio.

- Probar la capacidad del agente para recuperar y razonar sobre datos
  organizacionales estructurados dentro de Copilot Chat.

Duración estimada - 45 minutos

## Ejercicio 1: Crear un entorno de Power Platform

Con Power Platform, puede crear distintos entornos y cambiar entre ellos
según sus necesidades. Un entorno almacena aplicaciones, flujos, datos y
agentes, y cada entorno está completamente aislado de los demás. En este
ejercicio, creará un nuevo entorno dedicado en el que realizará los
ejercicios restantes.

1.  Abra un navegador y vaya a +++https://admin.powerplatform.com+++ e
    inicie sesión con las siguientes credenciales.

- Username - +++@lab.CloudPortalCredential(User1).Username+++

- Temporary Access Password
  - +++@lab.CloudPortalCredential(User1).TAP+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.png)

2.  Seleccione **Manage** y luego seleccione **+ New** en
    **Environments**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.png)

3.  Proporcione el **Name** como +++Dev env+++, seleccione el **Type**
    como **Developer** y seleccione **Next**. En la pantalla **Add
    Dataverse**, seleccione **Save**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.png)

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image4.png)

4.  El nuevo entorno se crea y cambia de estado **Preparing** a
    **Ready** cuando está listo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.png)

**Importante:** La creación del entorno tarda aproximadamente entre 10 y
15 minutos. Espere ese tiempo y luego actualice la pantalla para ver el
entorno creado en el Admin Center.

## Ejercicio 2 : Crear un agente para Microsoft 365 Copilot Chat

En este ejercicio, creará un agente declarativo con Microsoft Copilot
Studio y lo hospedará en Microsoft 365 Copilot Chat.

1.  Inicie sesión en +++https://copilotstudio.microsoft.com+++ con las
    siguientes credenciales (también disponibles en la pestaña
    **Resources**).

- Username - +++@lab.CloudPortalCredential(User1).Username+++

- Temporary Access Password
  - +++@lab.CloudPortalCredential(User1).TAP+++

2.  Seleccione **Get Started** en la pantalla **Welcome to Microsoft
    Copilot Studio**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.png)

3.  Seleccione **Skip** en la pantalla de bienvenida.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image8.png)

4.  Seleccione el entorno **Dev env** que se creó en el ejercicio
    anterior.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image9.png)

**Importante:** Si Copilot Studio no muestra la opción para seleccionar
el **entorno** como en la captura, realice los siguientes pasoss.

> ![A screenshot of a chat AI-generated content may be
> incorrect.](./media/image10.png)

Abra +++https://admin.powerplatform.microsoft.com/+++.
Seleccione **Manage** -\> **Environments** -\> **Dev env** y copie el
valor de **Environment ID**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image11.png)

Regrese a la pestaña de Copilot Studio y abra: 
+++https://copilotstudio.microsoft.com/environments/\< EnvironmentID
\>+++  (reemplazando **\< EnvironmentID \>** con el valor obtenido)

5.  Para crear un agente declarativo para Microsoft 365 Copilot Chat,
    primero explore la lista de agentes en Copilot Studio y luego
    seleccione el agente llamado **Microsoft 365 Copilot**. Seleccione
    **Got it** en la ventana emergente de actualización de versión.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.png)

6.  Seleccione **Agents** en la barra de navegación izquierda.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.png)

7.  Seleccione **Microsoft 365 Copilot** de la lista.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.png)

8.  e abrirá una nueva sección de Microsoft Copilot Studio. Desde ahí,
    seleccione **+ Add** para crear un nuevo agente para Microsoft 365
    Copilot Chat.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image15.png)

9.  Copilot Studio le pedirá que describa en lenguaje natural el
    propósito del agente. Pegue el siguiente prompt y seleccione
    **Send**:

+++You are an agent helping employees to find information about HR
policies and procedures, about how to improve their career, and about
how to define learning pathways.+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image16.png)

10. Cuando Copilot Studio lo solicite, asigne el nombre **Agentic HR** a
    su agente personalizado usando el siguiente prompt.

+++Name it as Agentic HR+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.png)

11. Luego, indique tareas u objetivos específicos con la siguiente
    instrucción:

+++Emphasize everything that helps team building, inclusion, and the
growth mindset+++

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image18.png)

12. Defina un tono profesional para el agente proporcionando la
    siguiente entrada:

+++It should have a professional tone+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image19.png)

13. Una vez que termine de describir el agente, seleccione **Create**
    para crear el agente.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image20.png)

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image21.png)

## Ejercicio 3: Publicar el agente en Microsoft 365 Copilot Chat

1.  Seleccione **Publish** desde la página de resumen del agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image22.png)

2.  Seleccione **Publish** en la pantalla **Publish agent**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image23.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image24.png)

3.  Seleccione **Copy** debajo de **Share link** para copiar el vínculo
    y luego seleccione **Done**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image25.png)

4.  Abra una nueva pestaña, pegue el URL copiado y seleccione Add para
    agregar Agentic HR a su lista de agentes.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image26.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image27.png)

5.  Seleccione **Skip** en la pantalla de introducción.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image28.png)

6.  El agente **Agentic** **HR** ya está agregado. Seleccione
    **Agentic** **HR** en el panel de navegación izquierdo.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image29.png)

## Ejercicio 4: Crear un sitio de SharePoint

1.  En un nuevo navegador, vaya
    a +++https://m365.cloud.microsoft/chat/+++ Seleccione **Apps** en el
    panel izquierdo y luego seleccione **SharePoint** cuando las
    aplicaciones se carguen.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image30.png)

2.  Seleccione **+ Create site** en la página de SharePoint.

![A screenshot of a browser AI-generated content may be
incorrect.](./media/image31.png)

3.  Seleccione **Communication** **site** en la página **Select the site
    type**.

![A screenshot of a web page AI-generated content may be
incorrect.](./media/image32.png)

4.  Seleccione una plantilla (template) para usarla.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image33.png)

5.  Seleccione **Use template**.

![A screenshot of a website AI-generated content may be
incorrect.](./media/image34.png)

6.  Ingrese +++Contoso site2-@lab.LabInstance.Id+++ como **Site name** y
    seleccione **Next.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image35.png)

7.  En la siguiente pantalla, seleccione **Create site**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image36.png)

8.  Una vez creado, anote el **URL** del sitio.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image37.png)

9.  Seleccione Documents en la barra de menú. Seleccione **+ Create or
    upload → Files upload.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image38.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image39.png)

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image40.png)

10. Seleccione el archivo **Sample-list-of-candidates.xlsx** desde
    **C:\LabFiles** para cargarlo. Una vez **cargado**, seleccione los
    **tres** **puntos** junto al **documento**, seleccione **Copy**
    **link** y guarde el vínculo en un **bloc** **de** **notas**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image41.png)

## Ejercicio 5: Agregar conocimiento al agente

En este ejercicio, agregará conocimiento desde el sitio de SharePoint al
agente que creó.

1.  De vuelta en Copilot Studio, desde la página principal del
    **agente**, seleccione **+ Add knowledge** en la sección Knowledge.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image42.png)

2.  Seleccione **SharePoint**, ingrese el URL del archivo cargado en el
    ejercicio anterior y seleccione **Add**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image43.png)

3.  Seleccione **Add to agent** en la siguiente pantalla.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image44.png)

4.  Seleccione **Publish** para publicar el agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image45.png)

5.  Seleccione **Publish** nuevamente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image46.png)

6.  **Copie** el URL y **ábralo** en un navegador.

![A screenshot of a computer program AI-generated content may be
incorrect.](./media/image47.png)

7.  Esta vez, aparecerá la opción **Update now** ya que el agente ya
    está agregado. Selecciónela.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image48.png)

8.  Seleccione **Open** una vez que se haya actualizado.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image49.png)

**Alerta:** Es posible que deba interactuar con la conversación de
Copilot para obtener los resultados esperados.

9.  En la pantalla del agente **Agentic** **HR**, envíe el siguiente
    mensaje.

+++Show me a list of candidates for HR with role "HR Director" or "HR
Manager"+++

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image50.png)

**Importante:** Si se le solicita aprobación, realice los siguientes
pasos. De lo contrario, puede omitirlos y revisar el resultado.

> En el mensaje Data to be shared with Agentic HR, seleccione **Allow**
> **once** (si se muestra).![A screenshot of a computer AI-generated
> content may be incorrect.](./media/image51.png)
>
> Si se le solicita iniciar sesión, seleccione Sign in to Agentic HR y
> luego Connect en la siguiente pantalla. ![A screenshot of a computer
> AI-generated content may be incorrect.](./media/image52.png)
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image53.png)

Seleccione **Submit** una vez conectado. 

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image54.png)

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image55.png)

Vuelva a enviar el siguiente mensaje al agente.

> +++Show me a list of candidates for HR with role "HR Director" or "HR
> Manager"+++ ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image56.png)

10. Recibirá la lista solicitada.

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image57.png)

> ![A screenshot of a computer AI-generated content may be
> incorrect.](./media/image58.png)

**Resumen**

En este laboratorio, usted **extendió Microsoft 365 Copilot Chat**
creando un **agente** **declarativo** **Agentic HR** mediante Microsoft
Copilot Studio. Configuró un entorno dedicado de Power Platform, diseñó
y publicó un agente enfocado en RR. HH., y lo integró en la experiencia
de Microsoft 365 Copilot.

También creó un sitio de comunicación de SharePoint, cargó contenido
relacionado con RR. HH. y lo conectó como origen de conocimiento para el
agente. Finalmente, validó la solución consultando al agente en Copilot
Chat y recibiendo respuestas contextualizadas basadas en SharePoint.

Este laboratorio **demuestra** cómo **Copilot** **Studio** permite a las
organizaciones crear agentes especializados por dominio que aprovechan
de forma segura el conocimiento empresarial y mejoran la productividad
mediante IA conversacional dentro de Microsoft 365

.


