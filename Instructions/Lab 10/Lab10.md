# Laboratório 10: Implementar uma ação de prompt para gerar perguntas de quiz com base em um tópico

**Objetivo:**

Ações de prompts são uma das maneiras de estender os Microsoft Copilots.
Fazem isso criando ações em linguagem natural específicas para o
negócio. As ações são interpretadas pelo modelo GPT para executar a ação
necessária conforme as instruções. Essas ações são encapsuladas em uma
definição de plugin de AI, que os copilots podem invocar em tempo de
execução quando uma intenção ou expressão correspondente é encontrada.

Neste laboratório, você aprenderá a criar uma ação de prompt para um
tópico de geração de questionário que gerará perguntas com base em um
determinado tema..

## Exercício 1: Use linguagem natural para criar um agente

1.  Abra um navegador e faça login em +++
    <https://copilotstudio.microsoft.com/+++> e faça login com as
    credenciais da aba **Resources** caso ainda não esteja nessa página.

![](./media/image1.png)

2.  Se você já estiver na página do Copilot Studio, clique em
    **Home** para ir para a página inicial.

![](./media/image2.png)

3.  Na página inicial, na área de texto **Describe your agent to create
    it**, digite +++I want you to be a question and answering assistant
    that can answer common questions from users using the content of a
    website+++ e clique em **Send**.

![](./media/image3.png)

4.  Pode sugerir um nome para o agente. Aceite-o ou informe o seu
    próprio nome.

5.  Forneça outros detalhes sobre as funções do agente, como abaixo.

> +++help answer common product and support questions using the content
> of a website, and help answer HR questions from an uploaded file+++

6.  Forneça +++[www.microsoft.com+++](http://www.microsoft.com+++/) para
    o site que será usado como fonte de conhecimento.

![](./media/image4.png)

7.  Após concluir as instruções, clique em **Create** para criar seu
    agente.

![](./media/image5.png)

8.  O agente é criado e abre com os detalhes. Role a página para ver que
    o agente foi criado com as instruções que você forneceu.

![](./media/image6.png)

![](./media/image7.png)

9.  Clique no ícone **Test** para testar o agente. Digite +++What is
    Copilot Studio+++ e pressione **Enter**.

![](./media/image8.png)

10. Entrar +++What is the latest xbox model?+++

![](./media/image9.png)

> Para ambas as etapas acima, você receberá uma resposta do agente que
> será genérica, pois o agente usará seu conhecimento geral.

## Exercício 2: Crie uma ação de prompt para um tópico com respostas generativas

As ações podem ser usadas para ampliar os recursos dos agentes. Você
pode adicionar vários tipos de ações aos seus agentes no Microsoft
Copilot Studio:

- **Prebuilt connector action**, que usa conectores do Power Platform
  para acessar dados de outros sistemas, como produtos empresariais
  populares como Salesforce, Zendesk, MailChimp e GitHub.

- **Custom connector action**, onde um conector pode ser criado para
  acessar dados de APIs públicas ou privadas.

- **Power Automate cloud flow**, que usa fluxos de nuvem do Power
  Automate para executar ações, recuperar e trabalhar com dados.

- **AI Builder prompts**, que usam o AI Builder e a compreensão de
  linguagem natural para atingir cenários e fluxos de trabalho
  específicos dentro do seu negócio.

- **Bot Framework skill**, que usa o manifesto de habilidades que
  descreve as ações que a habilidade pode realizar, incluindo seus
  parâmetros de entrada e saída, endpoints da capacidade e modelos de
  despacho para a habilidade.

Neste exercício, você aprenderá como adicionar um prompt de ação a um nó
de tópico

1.  No seu agente, selecione a aba **Topics**, selecione **+ Add a
    topic** e selecione **From blank**

![](./media/image10.png)

2.  Insira o nome do tópico como +++Generate questions for a quiz+++.
    Selecione o hiperlink **Edit** em **Phrases in the trigger**. É
    necessário inserir no mínimo 5 frases de acionamento.

> Adicione as frases abaixo uma por uma. Adicione cada frase e selecione
> a opção + para adicionar o acionamento.
>
> +++create a number of questions for a quiz based on a topic and format
> the quiz based on the instruction provided+++
>
> +++creates a quiz with a number of questions based on the topic
> provided and formats the quiz+++
>
> +++generate a quiz with a number of questions using the topic provide
> and format the questions+++
>
> +++creates questions for a quiz on a specific topic and format+++
>
> +++format a quiz by a number of questions based on the topic
> provided+++
>
> Selecione **Save** no canto superior direito para salvar o tópico.

![](./media/image11.png)

3.  Clique no símbolo **+** abaixo do nó **Trigger**. Selecione a opção
    **Add an action,** em seguida, selecione a opção **New prompt
    (default AI model).**

![](./media/image12.png)

![](./media/image13.png)

4.  A caixa de diálogo Prompt será exibida, e você poderá ver um menu
    suspenso que o orientará sobre como criar seu prompt. Selecione
    **Next** para prosseguir com o guia.

5.  Criaremos um prompt que gerará perguntas para um quiz. Digite o nome
    do prompt como +++Quiz Generator+++.

6.  Cole o conteúdo abaixo no campo Prompt.

7.  +++Generate a quiz with \[number\] questions to cover this
    \[topic\]. Decide on the format, such as multiple-choice questions
    or true/false statements. Use this \[format\]. Designate the correct
    answer within parentheses.+++

> Expanda a seção **Input** e selecione **+ Add input**.

![](./media/image14.png)

8.  Selecione **Text** na opção **Add input**.

![](./media/image15.png)

9.  Insira o nome +++number+++ e insira dados de exemplo, como +++5+++.
    Selecione **+ Add input** -\> **Text** para adicionar a próxima
    entrada.

![](./media/image16.png)

10. Digite o nome como +++topic+++ e insira dados de exemplo, como
    +++Science+++ e então selecione **+ Add input** -\> **Text** para
    adicionar a próxima entrada.

\![\](./media/image16.png)

11. Digite o nome como +++format+++ e insira dados de exemplo, como
    +++bullet points+++

![](./media/image17.png)

12. Agora que adicionamos os nomes dos campos de entrada e os dados de
    exemplo, o próximo passo é inserir essas entradas no prompt. No
    campo *Prompt*, destaque **\[number\]**, e clique em **+ Add** e
    selecione **number** em ***In your prompt***. A entrada **number**
    agora foi adicionada ao prompt como uma entrada.

![](./media/image18.png)

![](./media/image19.png)

13. Repita os mesmos passos para as entradas restantes.

14. Depois que todas as entradas forem adicionadas ao prompt, clique em
    **Test prompt** e observe a resposta do prompt.

![](./media/image20.png)

15. Selecione **Save** para salvar o prompt.

![](./media/image21.png)

16. O nó de ação de prompt agora aparecerá na tela de criação do Tópico.
    Em seguida, os valores do parâmetro de entrada precisam ser
    definidos para que o agente os preencha. Selecione o ícone **\>**

![](./media/image22.png)

17. Selecione a aba **System** e selecione **Activity.Text** como o
    valor de entrada para a ação, a fim de utilizar toda a resposta do
    usuário e identificar o valor de formato.

![](./media/image23.png)

18. Repita o mesmo para os demais parâmetros de entrada da ação do
    prompt.

![](./media/image24.png)

19. Em seguida, precisamos definir a variável de saída da ação do
    prompt. Isso permite que a resposta seja referenciada posteriormente
    no tópico. Selecione o ícone **\>** e, na aba **Custom**, selecione
    **Create new** e nomeie a variável como
    +++**VarQuizQuestionsResponse**+++.

![](./media/image25.png)

![](./media/image26.png)

20. Abaixo da ação de Prompt, selecione o ícone **+** para adicionar um
    novo nó e selecione **Send a message**. Selecione o ícone da
    variável **{x}.**

![](./media/image27.png)

21. Selecione a variável **VarQuizQuestionsResponse.text**. Isso
    adicionará a propriedade de texto da resposta da ação de prompt ao
    nó Enviar uma mensagem. Selecione **Save** para salvar seu tópico.

![](./media/image28.png)

22. Os detalhes do tópico precisam ser atualizados em seguida, e serão
    usados pelo seu agente para associar o tópico à intenção do usuário
    quando o Modo Generativo estiver ativado. Selecione **Details** e
    insira o seguinte.

    - Display name - +++generate questions for a quiz+++

    - Description - +++This topic creates questions for a quiz based on
      the number of questions, the topic and format provided by the
      user+++

Selecione **Save** para salvar seu tópico.

![](./media/image29.png)

23. Agora, a configuração do **Generative mode** precisa ser habilitada
    para que o agente chame o tópico com a ação de prompt. Selecione
    **Settings** para o seu agente.

![](./media/image30.png)

24. Selecione a configuração **Generative AI** e selecione **Generate
    (preview)** e, em seguida, selecione **Save**.

![](./media/image31.png)

25. Agora estamos prontos para testar o agente. No painel de testes,
    selecione o ícone de **refresh**. Em seguida, insira a seguinte
    pergunta e observe o resultado.

+++ Create 5 questions for a quiz based on geography and format the quiz
as multi choice+++

> ![](./media/image32.png)
>
> ![](./media/image33.png)

**Summary**

Neste laboratório, aprendemos como criar uma ação de prompt para um
tópico criando um prompt personalizado e testando-o.

m365cpltdeplextdepth/Instructions/Lab 10/Lab10.md at
m365cpltdeplextdepth-Dec2K24 · technofocus-pte/m365cpltdeplextdepth 
