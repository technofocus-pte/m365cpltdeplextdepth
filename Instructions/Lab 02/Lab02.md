# Laboratório 02 - Crie e configure um agente no chat do Microsoft 365 Copilot

**Objetivo**

Neste laboratório, você criará e configurará um agente Copilot usando as
abas Describe e Configure.

Você usará o Copilot Studio Agent Builder:

- Crie um agente usando as abas Descrever e Configurar no Copilot Studio
  Agent Builder

**Observação**: A disponibilidade da aba **Describe** depende da
[**geographic availability and language
support**](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/copilot-studio-agent-builder-build).
Se a aba **Describe** não for compatível com sua região ou idioma
preferido, você pode criar seu agente manualmente na aba **Configure**.

- Personalize instruções do agente, fonte de conhecimento e prompts
  iniciais.

- Teste e edite seu agente.

- Gerencie e compartilhe seu agente dentro de sua organização.

**Exercício 1: Crie um agente Copilot usando a aba Describe**

Neste exercício, você usará a aba **Describe** no Copilot Studio para
criar um agente básico.

1.  Abra um navegador Microsoft Edge e insira a seguinte URL:
    +++[https://m365.cloud.microsoft +++](https://m365.cloud.microsoft/)
    para acessar a página inicial **Microsoft 365 Copilot app** (antigo
    Office).

**Observação**: Você precisa fazer login (se solicitado) usando as
**credentials** fornecidas na aba **Resources** à direita.

2.  A página **Copilot Chat** será aberta.

3.  Se, por algum motivo, a mensagem “**Something went wrong”**
    aparecer, clique em **Try again** (duas vezes) para abrir o
    aplicativo Copilot.

![](./media/image1.png)

**Observação**: A interface do usuário do Copilot Chat pode parecer
diferente quando você estiver executando este laboratório (já que a
Microsoft lançou recursos novos e atualizados junto com alterações na
interface do usuário como parte do evento Microsoft
Build-2025).![](./media/image2.png)

![](./media/image3.png)

4.  Clique em **Create an agent**.

![](./media/image4.png)

5.  O Copilot Studio Agent Builder será aberto.

![](./media/image5.png)

6.  Na **aba Describe**, insira a descrição do propósito do agente em
    linguagem natural.

Neste exercício, você inserirá ++**An agent that assists users in
finding popular learning paths and modules from Microsoft**++.

![](./media/image6.png)

7.  Clique em **Submit** para visualizar o rascunho do agente.

8.  Um agente de rascunho com configurações iniciais definidas será
    salvo automaticamente. Revise os campos gerados automaticamente e
    faça os ajustes necessários. Neste exercício, você usará os campos
    gerados automaticamente como estão.

![](./media/image7.png)

9.  Você será solicitado a confirmar ou sugerir um nome para o agente.
    Neste exercício, atribua o nome **LearnAssist Buddy.**

![](./media/image8.png)

![](./media/image9.png)

10. Você acabou de criar um agente com detalhes básicos. Você será
    solicitado a refinar as instruções para o agente e fazer os ajustes
    necessários. Neste exercício, você usará as configurações padrão
    para agilizar o processo de criação.

![](./media/image10.png)

**Exercício 2: Configurar detalhes do agente usando a aba Configurar**

Neste exercício, você configurará as definições do agente para ajustar
seu comportamento.

**Observação**: Se você estiver criando um agente diretamente na aba
**Configure**, precisará definir o nome, a descrição e a finalidade do
agente.

1.  Alterne para a aba **Configure** no Agent Builder.

![](./media/image11.png)

2.  Comportamento do agente, incluindo o tom de resposta e o estilo de
    interação. Neste exercício, você seguirá as instruções padrão.

![](./media/image12.png)

3.  Agora, você configurará as fontes de conhecimento que o agente
    utilizará, como sites específicos do SharePoint, bibliotecas de
    documentos e sites. Neste exercício, você usará um site como fonte
    de conhecimento para fundamentar as respostas do agente.

Preencha +++<https://learn.microsoft.com/en-us/training+++> e pressione
Enter.

![](./media/image13.png)

![](./media/image14.png)

**Observação**: A URL do site não pode ter mais de dois níveis de
profundidade. Além disso, o agente pesquisará em sites públicos se você
não adicionar uma URL e ativar a pesquisa na web.

![](./media/image15.png)

4.  As alterações de configuração serão salvas automaticamente.

![](./media/image16.png)

5.  Você concluiu a configuração do agente com configurações
    personalizadas e adaptadas às necessidades da sua organização. Agora
    você garantirá que o agente funcione conforme o esperado e fará os
    ajustes necessários.

**Exercício 3: Testando e editando o agente**

Agora você testará se o agente responde com base nas definições de
configuração.

1.  Agora você inserirá o seguinte prompt para avaliar a resposta do
    agente.

++**List the popular learning paths and modules offered by
Microsoft**++.

![](./media/image17.png)

2.  Você pode verificar a resposta comparando-a com as informações
    disponíveis na URL inserida usada como fonte de conhecimento.

![](./media/image18.png)

3.  Você também pode testar a resposta inserindo algum prompt
    irrelevante.

++**Help me with instructions for baking cakes**++

![](./media/image19.png)

O agente evitou fornecer uma resposta com base na instrução “Avoid
discussing topics unrelated to Microsoft learning paths and modules”.

**Observação**: O conjunto de instruções padrão no seu caso pode ser
diferente. Certifique-se de que as instruções estejam configuradas
corretamente para evitar que o agente forneça a resposta.

4.  Retorne à **aba Configure** para editar as configurações, instruções
    ou fontes de conhecimento do agente, conforme necessário.

5.  Quando estiver satisfeito, clique em **Create** no canto superior
    direito para publicar o agente.

![](./media/image20.png)

![](./media/image21.png)

6.  Seu agente LearnAssist Buddy foi criado com sucesso.

![](./media/image22.png)

**Exercício 4: Gerenciando e Compartilhando o Agente**

Agora você implementará o agente em sua organização e gerenciará sua
acessibilidade.

1.  Compartilhe o agente com usuários ou grupos específicos definindo
    permissões apropriadas.

![](./media/image23.png)

![](./media/image24.png)

2.  Faça melhorias iterativas com base no feedback do usuário e nas
    métricas de desempenho.

**Experimente você mesmo:**

- Crie um agente “Product Buddy” para obter detalhes do produto.

- Mapeie a fonte de conhecimento para a biblioteca de documentos que
  você criou no “Lab 0 - Preparing for lab execution”

![](./media/image25.png)

![](./media/image26.png)

![](./media/image27.png)

![](./media/image28.png)

- Teste o agente fazendo perguntas relevantes relacionadas ao produto
  para verificar seu funcionamento.

**Resumo:**

Agora você concluiu a criação de agentes mapeados com diferentes fontes
de conhecimento e conjuntos de instruções para obter as respostas
esperadas dos agentes.



