# Laboratorio 09: Implement prompt action for a quiz generation agent's topic

**Objetivo:**

Las acciones de prompt son una de las formas de extender Microsoft
Copilots. Lo hacen mediante la creación de acciones en lenguaje natural
específicas del negocio. Estas acciones son interpretadas por el modelo
GPT para realizar la acción necesaria según lo indicado. Estas acciones
se encapsulan dentro de una definición de complemento de IA, que los
copilots pueden invocar en tiempo de ejecución cuando se detecta una
intención o expresión coincidente.

En este laboratorio, aprenderá a crear una acción de prompt para un tema
de generación de cuestionarios que generará preguntas de un quiz según
un tema determinado.

Duración estimada - 40 minutos

## Exercise 1: Use natural language to create an agent

1.  Abra un navegador e inicie sesión en
    +++https://copilotstudio.microsoft.com/+++ e inicie sesión con las
    siguientes credenciales.

- Username - +++@lab.CloudPortalCredential(User1).Username+++

- TAP - +++@lab.CloudPortalCredential(User1).TAP+++

2.  Desde la **página** **de** **inicio**, en el área de texto Start
    building by describing what your agent needs to do, ingrese +++I
    want you to be a question and answering assistant that can answer
    common questions from users using the content of a website+++ y
    seleccione **Send**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.png)

3.  El agente se crea según los requisitos.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image2.png)

4.  Desplácese hacia abajo y seleccione **+ Add knowledge** en la
    sección Knowledge.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image3.png)

5.  Seleccione la opción **Public websites**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image4.png)

6.  Ingrese +++www.microsoft.com+++ y seleccione **Add**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image5.png)

7.  Seleccione Add to agent.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image6.png)

8.  El sitio web se agrega como origen de conocimiento al agente.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image7.png)

9.  Seleccione el icono **Test** para probar el agente. Ingrese +++What
    is Copilot Studio?+++ y presione **Enter**.

![A screenshot of a phone AI-generated content may be
incorrect.](./media/image8.png)

10. Ingrese +++What is the latest xbox model?+++

![A screenshot of a chat AI-generated content may be
incorrect.](./media/image9.png)

Para ambas preguntas, obtendrá una respuesta del agente que será
genérica, ya que el agente utilizará su conocimiento general.

## Exercise 2: Create a Prompt action for a Topic for generative answers

Use **prompts** en **Copilot** **Studio** para crear acciones en
lenguaje natural como extensiones de copilot. Estas acciones utilizan
los modelos de IA generativa de AI Builder y el entendimiento del
lenguaje natural para abordar escenarios específicos para sus copilots.
Esto significa que puede extender las capacidades de sus copilots
simplemente creando acciones de prompt basadas en lenguaje natural.

En este ejercicio, aprenderá a agregar una acción de prompt a un nodo de
tema

1.  En su agente, seleccione la pestaña **Topics**, seleccione **+ Add a
    topic** y seleccione **From blank**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image10.png)

2.  Ingrese el nombre del tema como +++Generate questions for a quiz+++.
    Ingrese los siguientes detalles en la **Description** (seleccione la
    opción **Copy** y péguelos en el área **Description**).

> create a number of questions for a quiz based on a topic and format
> the quiz based on the instruction provided
>
> creates a quiz with a number of questions based on the topic provided
> and formats the quiz
>
> generate a quiz with a number of questions using the topic provide and
> format the questions
>
> creates questions for a quiz on a specific topic and format
>
> format a quiz by a number of questions based on the topic provided

Seleccione **Save** en la parte superior derecha para guardar el tema.

3.  Seleccione el símbolo **+** debajo del nodo Trigger. Seleccione la
    opción **Add a tool** y luego seleccione **New prompt**.

![Screens screenshot of a quiz AI-generated content may be
incorrect.](./media/image11.png)

4.  Aparecerá el cuadro de diálogo Prompt, y es posible que aparezca un
    panel guía que le ayudará a crear su prompt. Seleccione **Next**
    para avanzar por la guía.

5.  Cree un prompt que genere preguntas para un quiz. Ingrese el nombre
    del prompt como +++Quiz Generator+++.

6.  Pegue el siguiente contenido en el campo Prompt.

> +++Generate a quiz with \[number\] questions to cover this \[topic\].
> Decide on the format, such as multiple-choice questions or true/false
> statements. Use this \[format\]. Designate the correct answer within
> parentheses.+++
>
> Seleccione \[number\]**,** expanda + Add context y seleccione
> Text**.**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image12.png)

7.  Ingrese el nombre como +++number+++ e ingrese datos de ejemplo como
    +++5+++. Seleccione **Close**.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image13.png)

8.  Seleccione **\[topic\]**, expanda **+ Add context** y seleccione
    **Text**. Ingrese el nombre como +++topic+++ e ingrese datos de
    ejemplo como +++Science+++.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image14.png)

9.  Seleccione **\[format\]**, expanda **+ Add context** y seleccione
    **Text**. Ingrese el nombre como +++format+++ e ingrese datos de
    ejemplo como +++bullet points+++. Seleccione **Save** en la ventana
    del prompt.

![A screenshot of a test AI-generated content may be
incorrect.](./media/image15.png)

10. El nodo de acción de prompt ahora aparecerá en el lienzo de autoría
    del tema. A continuación, se deben definir los valores de los
    parámetros de entrada para que el agente pueda completarlos.
    Seleccione el icono **…**

![A screenshot of a quiz AI-generated content may be
incorrect.](./media/image16.png)

11. Seleccione la pestaña **System** y seleccione **Activity.Text** como
    el valor de entrada para que la acción utilice toda la respuesta del
    usuario e identifique el valor de formato.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image17.png)

12. Repita el mismo procedimiento para los parámetros de entrada
    restantes de la acción de prompt.

![A screenshot of a quiz AI-generated content may be
incorrect.](./media/image18.png)

13. A continuación, defina la variable de salida de la acción de prompt
    para que la respuesta pueda utilizarse más adelante en el tema.
    Seleccione el icono **\>** y, en la pestaña **Custom**, seleccione
    **Create new** y asigne el nombre +++VarQuizQuestionsResponse+++.

![A screenshot of a quiz AI-generated content may be
incorrect.](./media/image19.png)

![A screenshot of a browser window AI-generated content may be
incorrect.](./media/image20.png)

14. Debajo de la acción de prompt, seleccione el icono **+** para
    agregar un nuevo nodo y seleccione **Send a message**. Seleccione el
    icono de variable **{x}**.

![A screenshot of a quiz AI-generated content may be
incorrect.](./media/image21.png)

15. Seleccione la variable **VarQuizQuestionsResponse.text**. Esto
    agregará la propiedad text de la respuesta de la acción de prompt al
    nodo Send a message**.** Seleccione **Save** para guardar su tema.

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image22.png)

16. Actualice los detalles del tema, que serán utilizados por su agente
    para asociar el tema con la intención del usuario cuando el modo
    generativo esté habilitado. Seleccione **Details** e ingrese lo
    siguiente.

    - Display name - +++generate questions for a quiz+++

    - Description - +++This topic creates questions for a quiz based on
      the number of questions, the topic and format provided by the
      user+++

Seleccione **Save** para guardar su tema.

![A screenshot of a quiz AI-generated content may be
incorrect.](./media/image23.png)

17. Ahora está listo para probar el agente. Abra el panel Test, ingrese
    la siguiente pregunta y observe el resultado.

+++Create 5 questions for a quiz based on geography and format the quiz
as multi choice+++

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image24.png)

![A screenshot of a cell phone AI-generated content may be
incorrect.](./media/image25.png)

**Resumen**

En este laboratorio, aprendió a crear una acción de prompt para un tema
mediante la creación de un prompt personalizado y a probarlo.
