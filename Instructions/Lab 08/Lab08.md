# Laboratorio 8 - Cree un agente de SharePoint de guía de carreras

**Introducción:**

Cada día, se agregan alrededor de 2 mil millones de documentos a
Microsoft 365. Con el rápido crecimiento del volumen de contenido del
lugar de trabajo, necesita una forma rápida y precisa de examinarlo y
obtener la información que necesita. Microsoft SharePoint mejora la
seguridad y la eficiencia en el almacenamiento, la organización y el uso
compartido del contenido de su organización. Pero ofrece más allá de
eso. Puede usar agentes de SharePoint con tecnología de IA para
optimizar los flujos de trabajo y fomentar la colaboración que se adapte
a su equipo u organización. Los agentes de SharePoint pueden responder
preguntas sobre el contenido de cualquier sitio o biblioteca de
documentos de SharePoint con los que el solicitante tenga permisos. Si
tiene permisos de edición en un sitio de SharePoint, incluso puede crear
agentes para tareas específicas y compartirlos con su equipo.

Agentes de SharePoint

**Agente listo para usar**

Cada sitio de SharePoint viene con un "ready-made agent", que se limita
automáticamente al contenido de ese sitio. Estos agentes, cuyo ámbito se
encuentra en el sitio de SharePoint, no requieren ninguna creación por
parte de los administradores o propietarios del sitio. El agente listo
para usar aparece de forma predeterminada. 

**Agente personalizado**

¿No está satisfecho con el resultado del agente listo para usar? Con los
permisos de edición del sitio, puede crear agentes fácilmente cambiando
el alcance, la identidad y el comportamiento del contenido.

**Objetivo:**

En este laboratorio, creará un agente de SharePoint de orientación
profesional que use los documentos cargados en el sitio de SharePoint.

## Ejercicio 1: Cree un agente desde SharePoint Home

Creó un sitio de SharePoint en el laboratorio anterior. En este
ejercicio, creará un agente a partir de él.

Alerta: Esto funcionará como tal si está trabajando en los laboratorios
de forma continua desde el Laboratorio 6. De lo contrario, rehaga
el **Ejercicio 4 - Cree un sitio SharePoint del Laboratorio 6** y
continúe con los pasos de esta guía de laboratorio a continuación.

1.  Abra el sitio de SharePoint (use la dirección URL que anotó en el
    laboratorio anterior).

2.  Seleccione **Home**.

![](./media/image1.png)

3.  Seleccione **New** -\> **Agent** para crear un nuevo agente.

![](./media/image2.png)

4.  Se crea un nuevo agente y ahora seleccione: **Open agent**.

![](./media/image3.png)

5.  El agente creado aparece en el sitio.

![](./media/image4.png)

## Ejercicio 2: Cree un agente a partir de los documentos

En este ejercicio, cargará los documentos en el sitio de SharePoint y
creará un agente a partir de él.

1.  Seleccione **Documents**.

![](./media/image5.png)

2.  Seleccione el menú desplegable junto a **Upload** y seleccione
    **Files**.

![](./media/image6.png)

3.  Seleccione el **Career Path Options in the USA.pdf** y **Career Path
    Options.docx** desde **C:\LabFiles** y seleccione **Open**.

![](./media/image7.png)

![](./media/image8.png)

4.  Seleccione los documentos cargados y haga clic derecho sobre ellos y
    seleccione **Create an agent**.

![](./media/image9.png)

5.  Seleccione **Edit** en la ventana New agent para editar el nombre
    del agente.

![](./media/image10.png)

6.  Asigne un nombre al agente como +++Career Guidance Agent+++.
    Seleccione **Save and close**.

**Ojo:** El agente se puede personalizar desde Copilot Studio
seleccionando la opción Agregar personalización avanzada desde Copilot
Studio en la parte inferior izquierda.

![](./media/image11.png)

7.  El agente creado aparece en la lista **Documents**. Selecciónelo
    para abrirlo.

![](./media/image12.png)

8.  Pruébelo ingresando +++What are the Management career path available
    in the US?+++

![](./media/image13.png)

9.  Observe el resultado y las referencias.

![](./media/image14.png)

> ![](./media/image15.png)

10. Seleccione **Share -\> Copy link**

![](./media/image16.png)

11. Seleccione Allow en el pop up.

![](./media/image17.png)

![](./media/image18.png)

12. En Settings en el panel Copy, puede seleccionar con quién se puede
    compartir el agente.

![](./media/image19.png)

13. Acceda al agente desde un navegador mediante el enlace copiado.

## Resumen

En este laboratorio, ha aprendido a crear un agente de SharePoint desde
la página principal del sitio y desde los documentos cargados en el
sitio.
