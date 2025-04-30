# Laboratório 10: implementar ação imediata para um tópico de agente de geração de quiz

## Exercício 1: Use a linguagem natural para criar um agente

1.  Abra um navegador e faça login em
    +++https://copilotstudio.microsoft.com/+++ e faça login com as
    credenciais da guia Resources, caso ainda não esteja nessa página.

![](./media/image1.png)

2.  Se você já estiver na página do Copilot Studio, clique em **Home**
    para acessar a página inicial.

![](./media/image2.png)

3.  Na página inicial, na área de texto em Describe your agent to create
    it, digite +++I want you to be a question and answering assistant
    that can answer common questions from users using the content of a
    website+++ e clique em **Send.**

![](./media/image3.png)

4.  Ele pode sugerir um nome para o agente. Aceite-o ou forneça seu
    próprio nome.

5.  Forneça outros detalhes sobre as funções do agente, como abaixo.

> +++help answer common product and support questions using the content
> of a website, and help answer HR questions from an uploaded file+++ 

6.  Utilize o site +++www.microsoft.com+++ como a fonte de conhecimento
    oficial.

![](./media/image4.png)

7.  Após concluir a definição das instruções, clique em **Create** para
    criar seu agente.

![](./media/image5.png)

8.  O agente é criado e abre com os detalhes. Role pela página para
    entender que o agente foi criado com as instruções que você forneceu
    para ele.

![](./media/image6.png)

![](./media/image7.png)

9.  Clique no ícone **Test** para testar o agente. Digite +++What is
    Copilot Studio+++ e pressione **Enter**.

![](./media/image8.png)

10. Digite +++What is the latest xbox model?+++

![](./media/image9.png)

Em ambas as etapas acima, você obterá uma resposta do agente, que será
genérica, pois ele estará utilizando seu conhecimento geral.

## Exercício 2: Criar uma ação de Prompt para um Tópico para respostas generativas

As ações podem ser usadas para expandir as capacidades dos agentes. Você
pode adicionar vários tipos de ações aos seus agentes no Microsoft
Copilot Studio:

- **Ação de conector pré-construído**, que usa conectores do Power
  Platform para acessar dados de outros sistemas, como Salesforce,
  Zendesk, MailChimp e GitHub.

- **Ação do conector personalizado**, onde um conector pode ser criado
  para acessar dados de APIs públicas ou privadas.

- **Fluxo de nuvem do Power Automate**, que usam fluxos de nuvem do
  Power Automate para executar ações, recuperar e trabalhar com dados.

- **Prompts do AI Builder**, que usam o AI Builder e a compreensão de
  linguagem natural para direcionar os cenários e fluxos de trabalho
  específicos de sua empresa.

- **Habilidade da estrutura do bot**, que usam o manifesto da habilidade
  que descreve as ações que a habilidade pode executar, incluindo seus
  parâmetros de entrada e saída, os pontos de extremidade da habilidade
  e os modelos de despacho para a habilidade.

Neste exercício, você aprenderá a adicionar um prompt de ação a um nó de
tópico

1.  No seu agente, selecione a guia **Topics**, clique em **+ Add a
    topic** e selecione **From blank**.

![](./media/image10.png)

2.  Digite o nome do tópico como +++Generate questions for a quiz+++.
    Selecione o hiperlink **Edit** em Phrases no trigger. É necessário
    inserir um mínimo de 5 frases de acionamento.

> Adicione as frases abaixo, uma a uma. Adicione cada frase e selecione
> a opção + para adicionar o trigger.
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
> Selecione **Save** no canto superior direito para salvar o tópico.

![](./media/image11.png)

3.  Clique no símbolo **+** abaixo do nó de acionamento. Selecione a
    opção **Add an action** e selecione a opção **New prompt (default AI
    model)** abaixo dela.

![](./media/image12.png)

![](./media/image13.png)

4.  A caixa de diálogo de Prompt aparecerá e você poderá ver um guia
    lateral que ajudará a criar seu prompt. Selecione **Next** para
    seguir a instrução.

5.  Vamos criar um prompt que gerará perguntas para um quiz. Insira o
    nome do prompt como +++Quiz Generator+++.

6.  Cole o seguinte conteúdo no campo Prompt:

> +++Generate a quiz with \[number\] questions to cover this \[topic\].
> Decide on the format, such as multiple-choice questions or true/false
> statements. Use this \[format\]. Designate the correct answer within
> parentheses.+++
>
> Expanda a seção **Input** e selecione **+ Add input**.

![](./media/image14.png)

7.  Selecione **Text** na opção **Add input**.

![](./media/image15.png)

8.  Digite o nome como +++number+++ e insira dados de amostra como
    +++5+++. Selecione **+ Add input** -\> **Text** para adicionar a
    próxima entrada.

![](./media/image16.png)

9.  Digite o nome como +++topic+++ e insira dados de amostra como
    +++Science+++ e, em seguida, selecione **+ Add input** -\> **Text**
    para adicionar a próxima entrada. \![\](./media/image16.png) 

<!-- -->

11. Digite o nome como +++format+++ e insira dados de amostra, como
    +++bullet points+++

![](./media/image17.png)

12. Agora que adicionamos os nomes dos inputs e os dados de exemplo. Em
    seguida, os inputs precisam ser inseridos no prompt. No prompt,
    destaque **\[number\]** e selecione **+ Add** e selecione **number**
    em **In your prompt**. A entrada de número agora foi adicionada ao
    prompt como um input.

![](./media/image18.png)

![](./media/image19.png)

13. Repita as mesmas etapas para os demais inputs.

14. Depois que todos os inputs forem adicionados ao prompt, clique em
    **Testar prompt** e observe a resposta do prompt.

![](./media/image20.png)

15. Selecione **Save** para salvar o prompt.

![](./media/image21.png)

16. O nó de ação de prompt aparecerá agora na tela de criação do tópico.
    Em seguida, os valores do parâmetro de entrada precisam ser
    definidos para que o agente os preencha. Selecione o ícone **\>**

![](./media/image22.png)

17. Selecione a guia **System** e selecione **Acivity.Text** como o
    valor de entrada da ação para usar toda a resposta do usuário e
    identificar o valor do formato.

![](./media/image23.png)

18. Repita o mesmo processo para os parâmetros de entrada restantes da
    ação de prompt.

![](./media/image24.png)

19. Em seguida, precisamos definir a variável de saída da ação de
    prompt. Isso serve para que a resposta possa ser referenciada
    posteriormente no tópico. Selecione o ícone **\>** e, na guia
    **Custom**, selecione **Create new** e nomeie a variável como
    **+++VarQuizQuestionsResponse**+++.

![](./media/image25.png)

![](./media/image26.png)

20. Abaixo da ação Prompt, selecione o ícone **+** para adicionar um
    novo nó e selecione **Send a message**. Selecione o ícone da
    variável **{x}**.

![](./media/image27.png)

21. Selecione a variável**VarQuizQuestionsResponse.text**. Isso
    adicionará a propriedade text da resposta da ação de prompt ao nó
    enviar uma mensagem. Selecione **Save** para salvar o tópico.

![](./media/image28.png)

22. Os detalhes do tópico precisam ser atualizados em seguida, o que
    será usado pelo seu agente para associar o tópico à intenção do
    usuário quando o modo generativo estiver ativado. Selecione
    **Details** e digite o seguinte.

    - Display name - +++generate questions for a quiz+++

    - Description - +++This topic creates questions for a quiz based on
      the number of questions, the topic and format provided by the
      user+++

> Selecione **Save** para salvar esse tópico.

![](./media/image29.png)

23. Agora, a configuração do **Generative mode** precisa ser ativada
    para que o agente chame o tópico com a ação imediata. Selecione
    **Settings** para seu agente.

![](./media/image30.png)

24. Selecione a configuração **Generative AI** e selecione **Generate
    (preview)** e, em seguida, selecione **Save**.

![](./media/image31.png)

25. Agora estamos prontos para testar o agente. No painel de teste,
    selecione o ícone **refresh.** Em seguida, digite a pergunta a
    seguir e observe o resultado.

+++Create 5 questions for a quiz based on geography and format the quiz
as multi choice+++

> ![](./media/image32.png)

![](./media/image33.png)

**Resumo**

Neste laboratório, aprendemos a criar uma ação de prompt para um tópico,
criando um prompt personalizado e testando-o.

