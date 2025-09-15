# Laboratorio 02 - Cree y configure un agente en el chat de Microsoft 365 Copilot

**Objetivo**

En este laboratorio, creará y configurará un agente de Copilot con las
pestañas Describe y Configure.

Usará Copilot Studio Agent Builder:

- Cree un agente con las pestañas Describe y Configure en Copilot Studio
  Agent Builder

**Ojo**: la disponibilidad de la pestaña **Describe** se basa
en [**disponibilidad geográfica y soporte
lingüístico**](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/copilot-studio-agent-builder-build).
Si la pestaña **Describe** no se admite en su región o su idioma
preferido, puede construir su agente de forma manual a través de la
pestaña **Configure**.

- Personalice las instrucciones del agente, la fuente de conocimientos y
  las indicaciones de inicio.

- Pruebe y edite su agente.

- Administre y comparta su agente dentro de su organización.

**Ejercicio 1: Cree un agente de Copilot mediante Describe**

En este ejercicio, usará Describe en Copilot Studio para crear un agente
básico.

1.  Abra un navegador Microsoft Edge e introduzca la siguiente URL:
    +++[https://m365.cloud.microsoft+++](https://m365.cloud.microsoft+++/) para
    ir a la página de inicio de **Microsoft 365 Copilot
    app** (anteriormente conocido como office).

**Ojo**: Nececita iniciar sesión (si le pide) mediante las
credenciales **Credenciales** proporcionadas en la
pestaña **Resources** en la parte derecha.

2.  Se abrirá la página **Copilot Chat**.

3.  Si, por razón alguna, aparece el mensaje “**Something went wrong”**,
    haga clic en **Try again** (dos veces) para abrir la aplicación.

![](./media/image1.png)

**Ojo**: el interfaz del usuario de Copilot Chat puede parecer diferente
al ejecutar este laboratorio (ya que Microsoft ha implementado
características nuevas y actualizadas junto con cambios en la interfaz
de usuario como parte del evento Microsoft Build-2025).  
![](./media/image2.png)

![](./media/image3.png)

4.  Haga clic en **Create an agent**.

![](./media/image4.png)

5.  Se abrirá Copilot Studio Agent Builder.

![](./media/image5.png)

6.  En la pestaña **Describe**, introduzca la descripción del propósito
    del agente en la descripción en lenguaje natural.

En este ejercicio introducirá ++**An agent that assists users in finding
popular learning paths and modules from Microsoft**++.

![](./media/image6.png)

7.  Haga clic en Submit para obtener una vista previa del agente de
    borrador.

8.  Un agente de borrador con configuraciones iniciales establecidas se
    guardará automáticamente. Revise los campos generados
    automáticamente y realice los ajustes necesarios. En este ejercicio,
    utilizará los campos generados automáticamente tal cual.

![](./media/image7.png)

9.  Se le pedirá confirmar o sugerir un nuevo nombre para este agente.
    En este ejercicio, asignar a un nombre **LearnAssist Buddy.**

![](./media/image8.png)

![](./media/image9.png)

10. Ahora ha creado un agente con detalles básicos. Se le pedirá que
    perfeccione las instrucciones para el agente y realice los ajustes
    necesarios. En este ejercicio, utilizará la configuración
    predeterminada para acelerar el proceso de creación.

![](./media/image10.png)

**Ejercicio 2: Configure los detalles del agente en la pestaña
Configure**

En este ejercicio, configurará el agente para hacer un ajuste fino de su
comportamiento.

**Ojo**: si crea un agente directamente desde la pestaña Configure,
necesitará definir el nombre del agente, descripción y su propósito.

1.  Cambie a la pestaña Configure en el Agent Builder.

![](./media/image11.png)

2.  Puede configurar los ajustes de comportamiento del agente, incluido
    el tono de respuesta y el estilo de interacción. En este ejercicio,
    procederá con las instrucciones predeterminadas.

![](./media/image12.png)

3.  Ahora configurará las fuentes de conocimiento que usará el agente,
    como sitios específicos de SharePoint, bibliotecas de documentos y
    sitios web. En este ejercicio, utilizará un sitio web como fuente de
    conocimiento para fundamentar las respuestas de los agentes.

Popule +++<https://learn.microsoft.com/en-us/training+++> y haga clic en
enter.

![](./media/image13.png)

![](./media/image14.png)

**Ojo**: La URL del sitio web no puede tener más de dos niveles de
profundidad. Además, el agente buscará en sitios web públicos si no
agregas una URL y activarás la búsqueda web.

![](./media/image15.png)

4.  Los cambios de configuración se guardarán automáticamente.

![](./media/image16.png)

5.  Ahora ha completado la configuración del agente con ajustes
    personalizados adaptados a las necesidades de su organización. Ahora
    se asegurará de que el agente funcione según lo previsto y realizará
    los ajustes necesarios.

**Ejercicio 3: Probar y editar el agente**

Ahora probará si el agente responde en función de los ajustes de
configuración.

1.  Ahora introducirá el siguiente prompt para evaluar la respuesta del
    agente.

++**List the popular learning paths and modules offered by
Microsoft**++.

![](./media/image17.png)

2.  Puede comprobar la respuesta comparándola con la información
    disponible en la URL introducida como fuente de conocimiento.

![](./media/image18.png)

3.  También puede probar la respuesta ingresando algún prompt
    irrelevante.

++**Help me with instructions for baking cakes**++

![](./media/image19.png)

El agente evitó dar una respuesta basada en la instrucción “Avoid
discussing topics unrelated to Microsoft learning paths and modules”.

**Ojo**: El conjunto de instrucciones predeterminado en su caso puede
ser diferente. Asegúrese de que las instrucciones estén configuradas
correctamente para que el agente evite proporcionar la respuesta.

4.  Vuelva a la pestaña **Configure** para editar las configuraciones
    del agente, instrucciones,o fuentes de conocimiento según sea
    necesario.

5.  Una vez que esté satisfecho, haga clic en **Create** en la parte
    superior derecha para publicar el agente.

![](./media/image20.png)

![](./media/image21.png)

6.  Su agente LearnAssist Buddy se crea de forma exitosa.

![](./media/image22.png)

**Ejercicio 4: gestione y comparta el agente**

Ahora implementará el agente dentro de su organización y administrará su
accesibilidad.

1.  Comparta el agente con usuarios o grupos específicos mediante la
    configuración de los permisos adecuados.

![](./media/image23.png)

![](./media/image24.png)

2.  Realice mejoras iterativas basadas en los comentarios de los
    usuarios y las métricas de rendimiento.

**Pruébelo usted mismo:**

- Cree un agente “Product Buddy” para obtener los detalles del producto.

- Asigne el origen de conocimiento a la biblioteca de documentos que
  creó en “Lab 0 - Preparing for lab execution”

![](./media/image25.png)

![](./media/image26.png)

![](./media/image27.png)

![](./media/image28.png)

- Pruebe el agente preguntando prompts relevantes relacionadas con el
  producto para verificar su funcionamiento.

**Resumen:**

Ahora ha completado la creación de agentes asignados con diferentes
fuentes de conocimiento y conjuntos de instrucciones para obtener las
respuestas esperadas de los agentes.
